## User Compromise in Microsoft 365




##### Searching for MFA prompts for *user*
```KQL
SigninLogs
| where TimeGenerated > ago (30d)
| where UserPrincipalName == “user@whatever.com”
| where ResultType == 50074
| project TimeGenerated, UserPrincipalName, AppDisplayName, ResultType, IPAddress, UserAgent, Location
```

##### Searches for MFA prompts for *user* with additional risk
```KQL
SigninLogs
| where TimeGenerated > ago (30d)
| where UserPrincipalName == "user@whatever.com"
| where ResultType == 50074
| where RiskLevelDuringSignIn != "none"
| project TimeGenerated, UserPrincipalName, AppDisplayName, ResultType, IPAddress, UserAgent, Location, RiskLevelDuringSignIn
```

##### Searches for sign ins from *user* from a malicious IP, to OfficeHome or from Nigeria
```KQL
SigninLogs
| where TimeGenerated > ago (30d)
| where UserPrincipalName == "user@whatever.com"
| where AppDisplayName == "OfficeHome" or IPAddress == "10.10.10.10" or Location == "NG"
| project TimeGenerated, UserPrincipalName, AppDisplayName, ResultType, IPAddress, UserAgent, Location, RiskLevelDuringSignIn
```

##### Summarizes sign in data from *user* from a malicious IP address
```KQL
SigninLogs
| where TimeGenerated > ago (30d)
| where UserPrincipalName == "user@whatever.com"
| where ResultType == 0
| where IPAddress == "10.10.10.10" 
| project TimeGenerated, UserPrincipalName, AppDisplayName, ResultType, IPAddress, UserAgent, Location, RiskLevelDuringSignIn
| summarize TotalCount=count(), FirstEvent=min(TimeGenerated), LastEvent=max(TimeGenerated), AppsAccessed=make_set(AppDisplayName)
```

##### Summarizes sign in data from all users from a malicious IP address
```KQL
SigninLogs
| where TimeGenerated > ago (30d)
| where ResultType == 0
| where IPAddress == "10.10.10.10" 
| project TimeGenerated, UserPrincipalName, AppDisplayName, ResultType, IPAddress, UserAgent, Location, RiskLevelDuringSignIn
| summarize TotalCount=count(), FirstEvent=min(TimeGenerated), LastEvent=max(TimeGenerated), AppsAccessed=make_set(AppDisplayName) by UserPrincipalName
```

##### Searches for Microsoft Entra ID audit events from *user1* or *user2*
```KQL
AuditLogs
| where InitiatedBy has_any ("user1@whatever.com","user2@whatever.com") or TargetResources has_any ("user1@whatever.com","user2@whatever.com")
| project TimeGenerated, OperationName, Result, InitiatedBy, TargetResources
```

##### Searches for Cloud App Events belonging to *user1*, *user2*, a suspicious phone number, workstation and from a malicious IP address
```KQL
CloudAppEvents
| where TimeGenerated > ago (30d)
| where RawEventData has_any("user1@whatever.com","user2@whatever.com","555555555","DESKTOP-WHATEVER")
  and RawEventData has "10.10.10.10"


