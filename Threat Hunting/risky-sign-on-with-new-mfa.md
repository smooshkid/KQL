##### Risky Sign on with new MFA Method
```KQL
// Looks for a new MFA method added to an account that was preceded by medium or high risk sign-in session for the same user within maximum 6h timeframe 
let mfaMethodAdded=CloudAppEvents
| where ActionType =~ "Update user." 
| where RawEventData has "StrongAuthenticationPhoneAppDetail"
| where isnotempty(RawEventData.ObjectId) and isnotempty(RawEventData.Target[1].ID)
| extend AccountUpn = tostring(RawEventData.ObjectId)
| extend AccountObjectId = tostring(RawEventData.Target[1].ID)
| project MfaAddedTimestamp=Timestamp,AccountUpn,AccountObjectId;
let usersWithNewMFAMethod=mfaMethodAdded
| distinct AccountObjectId;
let hasusersWithNewMFAMethod = isnotempty(toscalar(usersWithNewMFAMethod));
let riskySignins=AADSignInEventsBeta
| where hasusersWithNewMFAMethod
| where AccountObjectId in (usersWithNewMFAMethod)
| where RiskLevelDuringSignIn in ("50","100") //Medium and High sign-in risk level.
| where RiskEventTypes has_any ("107", "210")
| where Application in ("Office 365 Exchange Online", "OfficeHome")
| where isnotempty(SessionId)
| project SignInTimestamp=Timestamp, Application, SessionId, AccountObjectId, IPAddress,RiskLevelDuringSignIn
| summarize SignInTimestamp=argmin(SignInTimestamp,*) by Application,SessionId, AccountObjectId, IPAddress,RiskLevelDuringSignIn;
mfaMethodAdded
| join riskySignins on AccountObjectId
| where MfaAddedTimestamp - SignInTimestamp < 30d //Timebetween risky sign-in and device registration
| project-away AccountObjectId1
```
