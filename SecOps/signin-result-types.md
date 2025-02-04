# Azure SigninLogs result types

##### All are unchanged except code 0, which is not an error code. 
##### Live data for error codes can be obtained here: https://login.microsoftonline.com/error
##### This list is an enumeration of that web resource (i.e. brute forcing all values between 0 and 9000000)
```
Error Code|||||Message|||||Remediation
0|||||No specific error message for this error code|||||No Remediation Provided
16000|||||Either multiple user identities are available for the current request or selected account is not supported for the scenario.|||||This is not an error scenario, but is handled like one by Azure AD to handle certain authentication flows.  This is not an indication that anything went wrong.
16001|||||Active accounts must be logged out first.|||||No Remediation Provided
16002|||||Application requested to sign out of a user session which does not exist.|||||No Remediation Provided
16003|||||The user account does not exist in the directory or the user hasn't been explicitly added to the tenant. To sign into this application, the account must be added to the directory.|||||Invite the user to the tenant, or ignore this error if the user isn't supposed to be a member of the tenant. This can be the case when someone is sent to a login URL for your tenant without being a member, or picks the wrong user account.
17001|||||Protected credential key can not be decoded.|||||No Remediation Provided
17002|||||Credential key can not be protected.|||||No Remediation Provided
17003|||||User key ({keyType}) could not be provisioned.|||||No Remediation Provided
17004|||||Protected credential key can not be decoded.|||||No Remediation Provided
18000|||||Cannot decrypt auth ticket with key version '{version}'.|||||No Remediation Provided
18001|||||Cannot decrypt buffer because of a HMAC mismatch.|||||No Remediation Provided
20001|||||The sign-in response message does not contain an issued token.|||||There's an issue with your federated identity provider. The WS-Federation response acquired from a federated identity provider has been successfully parsed, but it did not contain SAML 1.1 assertion issued for the user. Please contact your identity provider to resolve this issue.
20002|||||An error occurred while attempting to export Federation Metadata.|||||No Remediation Provided
20012|||||An error occurred when we tried to process a WS-Federation message. The message was invalid.|||||There is an issue with your federated identity provider. Contact your identity provider to resolve this issue.
20024|||||Federation metadata retrieval failed after multiple retries.|||||No Remediation Provided
20033|||||The actual message content is runtime specific. Please see returned exception message for details.|||||Actual message content is runtime specific. Please see returned exception message for details.
20034|||||Non-retryable error has occurred.|||||No Remediation Provided
25008|||||Unable to parse assertion.|||||No Remediation Provided
26000|||||The provided access grant requires interaction.|||||No Remediation Provided
27000|||||Error when processing DeviceAuthRedirect request.|||||No Remediation Provided
28000|||||Provided value for the input parameter scope is not valid because it contains more than one resource. Scope {scope} is not valid.|||||No Remediation Provided
28001|||||Provided request must include a 'scope' input parameter.|||||No Remediation Provided
28002|||||Provided value for the input parameter scope '{scope}' is not valid when requesting an access token. Please specify a valid scope.|||||No Remediation Provided
28003|||||Provided value for the input parameter scope cannot be empty when requesting an access token using the provided authorization code. Please specify a valid scope.|||||No Remediation Provided
28004|||||The provided value for the input parameter 'scope' exceeded the number of scopes allowed. The scope {scope} is not valid.|||||No Remediation Provided
28005|||||The provided value for the input parameter 'actionid' was invalid.|||||No Remediation Provided
28006|||||The provided value for the input parameter 'pageid' was invalid.|||||No Remediation Provided
28007|||||The parameters provided in the request are incorrect or missing.|||||No Remediation Provided
29000|||||Invalid signing key for SSH certificate|||||No Remediation Provided
29001|||||User is missing UPN or email|||||No Remediation Provided
29002|||||Missing Proof of Possession key|||||No Remediation Provided
29003|||||Proof of Possession key is invalid|||||No Remediation Provided
29004|||||Proof of Possession key type is not supported|||||No Remediation Provided
29005|||||The token scenario {tokenScenario} is invalid.|||||No Remediation Provided
29006|||||Client is missing application principal ID (Client ID) in tenant {tenantId}|||||No Remediation Provided
29007|||||The permission (scope) list {scopeListString} is missing user_impersonation|||||No Remediation Provided
29008|||||The resource 'Microsoft Azure Linux Virtual Machine Sign-In' ({resourceUrl}) is required for SSH certificate token request|||||No Remediation Provided
29100|||||A transient error has occurred. Please try again.|||||No Remediation Provided
29200|||||QR Code requested. Generate QR code and display on UX page for interactive sign-ins.|||||No Remediation Provided
29201|||||Invalid QR Code request. Client Id ({clientId}) or target client Id ({targetClientId}) is invalid.|||||No Remediation Provided
29202|||||Invalid scope and response_type request parameters. scope=qrcode can only be used with response_type=none.|||||No Remediation Provided
29203|||||Invalid target_client_id '{targetClientId}' argument value.|||||No Remediation Provided
29204|||||Failed to write QR Code token to Store.|||||No Remediation Provided
29205|||||Generated QR Code string has exceeded maximum supported length.|||||No Remediation Provided
29206|||||Invalid QR Code redemption request. Client Id ({clientId}) is invalid.|||||No Remediation Provided
29207|||||Error processing session data. QR Code is either invalid or expired.|||||No Remediation Provided
29208|||||Error processing session data. QR Code was already redeemed.|||||No Remediation Provided
29210|||||QR Code sign-in is disabled via user credential policy.|||||No Remediation Provided
29211|||||QR Code sign-in is not supported for passthrough users.|||||No Remediation Provided
29212|||||QR Code sign-in is not supported for consumer user scenarios.|||||No Remediation Provided
40002|||||The identity provider returned an error. The status returned was '{status}' and the message was '{message}'.|||||No Remediation Provided
40003|||||A required token was not emitted by an external Identity Provider.|||||No Remediation Provided
40004|||||A required token was not emitted by an external Identity Provider.|||||No Remediation Provided
40005|||||Invalid token received from external Identity Provider. Current time: {curTime}, expiry time of assertion {expTime}.|||||No Remediation Provided
40008|||||There was an unexpected error from the external identity provider.|||||There is an issue with your federated identity provider. Contact your identity provider to resolve this issue.
40009|||||The identity provider returned an error.|||||There is an issue with your federated identity provider. Contact your identity provider to resolve this issue.
40010|||||The identity provider has failed with a transient error.|||||The application should retry the request. If there is still an issue, contact your identity provider.
40013|||||Social IDP MicroService Federation disabled.|||||No Remediation Provided
40014|||||Federated Identity Provider is unavailable.|||||There is an issue with your federated identity provider. Contact your identity provider to resolve this issue.
40015|||||The identity provider returned an error.|||||There is an issue with your federated identity provider. Contact your identity provider to resolve this issue.
40016|||||The Identity Provider returned an error.|||||There is an issue with your federated identity provider. Contact your identity provider to resolve this issue.
50000|||||There was an error issuing a token or an issue with our sign-in service.|||||If this persists, open a support ticket to resolve this issue: https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-troubleshooting-support-howto
50001|||||The resource is disabled or the resource named could not be found. This can happen if the application has not been installed by the administrator of the tenant, or if the resource principal was not found in the directory or is invalid due to a typo.|||||Check your app's code to ensure that you have specified the exact and correct resource URL for the resource you are trying to access. Please see the returned exception message for details.
50002|||||This tenant isn't supported for this authentication method yet.|||||No Remediation Provided
50003|||||Certificate roll is in progress. Please retry the operation later.|||||Check the resolutions outlined at https://docs.microsoft.com/azure/active-directory/application-sign-in-problem-federated-sso-gallery#certificate-or-key-not-configured. If you still see issues, contact the app owner or an app admin.
50004|||||A transient error has occurred. Please try again.|||||No Remediation Provided
50005|||||User tried to log in to a device from a platform ({platform}) that's currently not supported through Conditional Access policy. Supported device platforms are: iOS, Android, Mac, and Windows flavors.|||||No Remediation Provided
50006|||||Signature verification failed because of an invalid signature.|||||Check out the resolution outlined at https://docs.microsoft.com/azure/active-directory/application-sign-in-problem-federated-sso-gallery. If the issue persists, contact the application owner or application administrator.
50007|||||Encryption certificate was not found in the directory.|||||No Remediation Provided
50008|||||The SAML token is invalid.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
50010|||||Audience URI validation failed since no token audiences were configured.|||||Contact the application owner for resolution.
50011|||||The reply URL specified in the request does not match the reply URLs configured for the application: '{identifier}'. {detail}|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
50012|||||Authentication failed.|||||Ensure that the request is sent with the correct credentials and claims.
50013|||||Assertion failed signature validation. Possibly because the token issuer doesn't match the API version within its valid time range, it's expired or malformed, or the refresh token in the assertion is not a primary refresh token.|||||Application error. Contact the app developer and ask them to debug this issue.
50014|||||The user's redemption is in a pending state. The guest user account is not fully created yet.|||||No Remediation Provided
50015|||||The user requires legal age group consent.|||||This user was asked to provide their age due to legal requirements.
50016|||||Invalid Argument Redirect ErrorCode value.|||||No Remediation Provided
50017|||||Validation of given certificate for certificate based authentication failed.|||||Contact the tenant admin. Possible reasons for this error include: cannot find issuing certificate in trusted certificates list, unable to find expected CrlSegment, cannot find issuing certificate in trusted certificates list, delta CRL distribution point is configured without a corresponding CRL distribution point, unable to retrieve valid CRL segments because of a timeout issue, or unable to download CRL.
50020|||||User account '{email}' from identity provider '{idp}' does not exist in tenant '{tenant}' and cannot access the application '{appId}'({appName}) in that tenant. The account needs to be added as an external user in the tenant first. Sign out and sign in again with a different Azure Active Directory user account.|||||A user was sent to a tenanted endpoint, and signed into an AAD account that doesn't exist in your tenant. If this user should be a member of the tenant, they should be invited via the B2B system. See here for details: https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator
50023|||||ClaimType '{claimType}' is reserved for system use.|||||No Remediation Provided
50024|||||Unable to decrypt client state.|||||No Remediation Provided
50025|||||The issuer name must be specified.|||||No Remediation Provided
50027|||||JWT token is invalid or malformed.|||||Contact the application owner to fix the JWT their app is creating for authentication. This can occur for a variety of reasons: doesn't contain nonce claim or sub claim, subject identifier mismatch, duplicate claim in idToken claims, unexpected issuer, unexpected audience, not within its valid time range, or a token format issue.
50029|||||The reply URI specified in the request contains invalid characters. Domain names of this form are not supported.|||||Contact the developer to update their app and app registration to use a different URI.
50030|||||One of forwardableOnBehalfOfOriginsAcceptedAudiencesList or ForwardableOnBehalfOfOriginsAcceptedPrecedingAppsList is not set. Both fields need to be filled for PFT OBO to be successful. These must be filled for multi-hop PFT OBO to be succesful.|||||The application owner must update the app registration and provide both the app that sent the PFT and the original resource.
50032|||||RSA key size {actualSize} is less than the minimum required {minSize} bits.|||||No Remediation Provided
50033|||||A transient error has occurred. Please try again.|||||No Remediation Provided
50034|||||The user account {identifier} does not exist in the {tenant} directory. To sign into this application, the account must be added to the directory.|||||The user that attempted to sign in doesn't exist in this tenant. This can occur because the user mis-typed their username, or isn't in the tenant. An application may have chosen the wrong tenant to sign into, and the currently logged in user was prevented from doing so since they did not exist in your tenant. If this user should be able to log in, add them as a guest. See docs here: https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator
50038|||||The API version isn't supported.|||||No Remediation Provided
50042|||||The salt required to generate a pairwise identifier is missing in the principal.|||||If this application has been recently registered, please wait for some time for the configuration to take effect, and then try again.
50043|||||Unable to generate a pairwise identifier with more than one salt in principal.|||||No Remediation Provided
50045|||||The salt required to generate a pairwise identifier is malformed in principal.|||||No Remediation Provided
50048|||||Subject must match the issuer claim in the client assertion.|||||Contact the developer to ensure that the JWT they generated for authentication has correct sub and iss claims. https://docs.microsoft.com/azure/active-directory/develop/active-directory-certificate-credentials
50049|||||Unknown or invalid instance.|||||Application error - the login request was malformed and could not be matched with an existing authentication endpoint or instance.
50050|||||The request is malformed: invalid format for '{name}' value.|||||Contact the application owner.
50052|||||The password entered exceeds the maximum length. Please reach out to your admin to reset the password.|||||The user is unable to login because their password exceeds the permitted maximum length. They should contact their admin to reset the password. If SSPR is enabled for their tenant, they can reset their password by following the "Forgot your password" link.
50053|||||The account is locked, you've tried to sign in too many times with an incorrect user ID or password.|||||This error can be returned for two reasons - the sign in could have come from a malicious IP address, or the account was locked due to repeated sign-in attempts. Only one error code is used to prevent an attacker from distinguishing between the states. In your Azure AD tenant, you can distinguish between these states by looking at the specific sign-in log entry for this request. For accounts locked for too many attempts, see https://docs.microsoft.com/azure/active-directory/identity-protection/howto-unblock-user
50054|||||Looks like you entered your old password. Try again with your new one.|||||The user needs to enter a new password, not one they previously used.
50055|||||The password is expired.|||||The user's password is expired, and therefore their login or session was ended. They will be offered the opportunity to reset it, or may ask an admin to reset it via https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-reset-password-azure-portal
50056|||||Invalid or missing password: password does not exist in the directory for this user.|||||The user should be asked to enter their password again.
50057|||||The user account is disabled.|||||The user object in Active Directory backing this account has been disabled. An admin can re-enable this account through Powershell: https://docs.microsoft.com/powershell/module/addsadministration/enable-adaccount?view=win10-ps
50058|||||Session information is not sufficient for single-sign-on.|||||This means that a user is not signed in. This is a common error that's expected when a user is unauthenticated and has not yet signed in. If this error is encountered in an SSO context where the user has previously signed in, this means that the SSO session was either not found or invalid. This error may be returned to the application if prompt=none is specified.
50059|||||No tenant-identifying information found in either the request or implied by any provided credentials.|||||No Remediation Provided
50060|||||Unable to sign out.|||||No Remediation Provided
50061|||||Unable to complete signout. The request was invalid.|||||No Remediation Provided
50062|||||Signout request is unauthorized.|||||No Remediation Provided
50068|||||Signout failed. The initiating application is not a participant in the current session.|||||No Remediation Provided
50069|||||Signout failed. The request specified a name identifier of '{identifier}' which did not match the existing session(s).|||||No Remediation Provided
50070|||||Signout failed. The request specified session indexes '{identifier}' which did not match the existing session(s).|||||No Remediation Provided
50071|||||Signout request has expired.|||||No Remediation Provided
50072|||||Due to a configuration change made by your administrator, or because you moved to a new location, you must enroll in multi-factor authentication to access '{identifier}'.|||||The user was presented options to provide contact options so that they can do MFA.
50074|||||Strong Authentication is required.|||||User needs to perform multi-factor authentication. There could be multiple things requiring multi-factor, e.g. Conditional Access policies, per-user enforcement, requested by client, among others.
50076|||||Due to a configuration change made by your administrator, or because you moved to a new location, you must use multi-factor authentication to access '{resource}'.|||||User needs to perform multi-factor authentication. There could be multiple things requiring multi-factor, e.g. Conditional Access policies, per-user enforcement, requested by client, among others.
50077|||||The administrator created a conditional access policy that requires the authenticator to be used to provide GPS location.|||||No Remediation Provided
50078|||||Presented multi-factor authentication has expired due to policies configured by your administrator, you must refresh your multi-factor authentication to access '{resource}'.|||||No Remediation Provided
50079|||||Due to a configuration change made by your administrator, or because you moved to a new location, you must enroll in multi-factor authentication to access '{identifier}'.|||||Either a managed user needs to register security info to complete multi-factor authentication, or a federated user needs to get the multi-factor claim from the federated identity provider. There could be multiple things requiring multi-factor, e.g. Conditional Access policies, per-user enforcement, requested by client, among others.
50080|||||Bad request received.|||||No Remediation Provided
50081|||||The administrator created a conditional access policy that requires GPS location.|||||No Remediation Provided
50085|||||Refresh token needs a social identity provider login.|||||The user is being redirected to another IDP for reauthentication.
50087|||||A transient error has occurred during strong authentication. Please try again.|||||No Remediation Provided
50088|||||Limit on telecom MFA calls reached. Please try again in a few minutes.|||||No Remediation Provided
50089|||||Authentication failed due to flow token expired.|||||Expected - auth codes, refresh tokens, and sessions expire over time or are revoked by the user or an admin. The app will request a new login from the user.
50091|||||Passed query string length exceeds supported limit.|||||No Remediation Provided
50093|||||Missing value for the SAML NameID.|||||No Remediation Provided
50094|||||Unknown source configured on the audience for the SAML NameID.|||||No Remediation Provided
50095|||||Unknown source configured on the audience for the SAML email claim.|||||No Remediation Provided
50096|||||Source configured on the audience for the SAML NameID is not compatible with the requested format.|||||No Remediation Provided
50097|||||Device authentication is required.|||||This is not an error - this is an interrupt that triggers device authentication when required due to a Conditional Access policy or because the application or resource requested the device ID in a token. This code alone does not indicate a failure on your users part to sign in. The sign in logs may indicate that the device authentication challenge was passed succesfully or failed.
50098|||||JWT body must contain '{field}'.|||||No Remediation Provided
50099|||||Invalid nonce.|||||No Remediation Provided
50100|||||There was an error transforming the claims for the token.|||||No Remediation Provided
50101|||||Unknown claims transformer '{name}' was specified for principal '{principalId}'.|||||No Remediation Provided
50102|||||Unable to load CustomClaimsTransformer '{type}' was specified for principal '{principalId}'.|||||No Remediation Provided
50103|||||There was an error transforming the claims for the token: {errorMessage}|||||No Remediation Provided
50105|||||Your administrator has configured the application {appName} ('{appId}') to block users unless they are specifically granted ('assigned') access to the application.  The signed in user '{user}' is blocked because they are not a direct member of a group with access, nor had access directly assigned by an administrator. Please contact your administrator to assign access to this application.|||||Assign the user to the app. See https://docs.microsoft.com/azure/active-directory/manage-apps/methods-for-assigning-users-and-groups and https://docs.microsoft.com/azure/active-directory/manage-apps/application-sign-in-problem-federated-sso-gallery#user-not-assigned-a-role
50107|||||The requested federation realm object '{name}' does not exist.|||||Application error - the login request was malformed and could not be matched with an existing authentication endpoint or instance.
50108|||||Claims transformation configuration could not be retrieved.|||||No Remediation Provided
50109|||||Claim transformation is unknown from configuration.|||||No Remediation Provided
50111|||||Unknown claim transformation was asked to be applied.|||||No Remediation Provided
50117|||||Failed to deserialize policy specified in the request's claim parameter.|||||No Remediation Provided
50120|||||Unknown credential type, issue with the JWT header.|||||No Remediation Provided
50123|||||Unknown claims transformation method '{method}' was specified for principal '{principalId}'.|||||No Remediation Provided
50124|||||Invalid regular expression configured for claims transformation for this application.|||||Contact your tenant admin to fix the claims mapping configuration. See https://docs.microsoft.com/azure/active-directory/develop/active-directory-saml-claims-customization
50125|||||Sign-in was interrupted due to a password reset or password registration entry.|||||User authentication was blocked because they need to provide password reset information. Their next interactive sign in will ask them for this, which the app should trigger next.
50126|||||Error validating credentials due to invalid username or password.|||||The user didn't enter the right credentials.  It's expected to see some number of these errors in your logs due to users making mistakes.
50127|||||Client app is a MAM app and device is not registered.|||||The user needs to install the broker app and work place join using the broker app in order to register the device.
50128|||||No tenant-identifying information found in either the request or implied by any provided credentials.|||||No Remediation Provided
50129|||||The device is not workplace joined. Workplace join is required to register the device.|||||No Remediation Provided
50130|||||The claim value(s) '{value}' cannot be interpreted as known auth method(s).|||||No Remediation Provided
50131|||||Device is not in required device state: {state}. Or, the request was blocked due to suspicious activity, access policy, or security policy decisions.|||||No Remediation Provided
50132|||||The session is not valid due the following reasons: password expiration or recent password change, SSO Artifact is invalid or expired, session is not fresh enough for application, or a silent sign-in request was sent but the user's session with Azure AD is invalid or has expired.|||||Expected - auth codes, refresh tokens, and sessions expire over time or are revoked by the user or an admin. The app will request a new login from the user.
50133|||||The session is not valid due to password expiration or recent password change.|||||Expected - auth codes, refresh tokens, and sessions expire over time or are revoked by the user or an admin. The app will request a new login from the user.
50134|||||Wrong data center. To authorize a request that was initiated by an app in the OAuth 2.0 device flow, the authorizing party must be in the same data center where the original request resides.|||||No Remediation Provided
50135|||||Password change is required due to account risk.|||||No Remediation Provided
50136|||||Single MSA session detected when requesting an MSA ticket.|||||No Remediation Provided
50137|||||Password needs to be changed due to security policy rule.|||||No Remediation Provided
50138|||||Invalid encryption key environment.|||||No Remediation Provided
50139|||||Session is invalid due to missing an external refresh token.|||||No Remediation Provided
50140|||||This occurred due to 'Keep me signed in' interrupt when the user was signing in.|||||This is an expected part of the login flow, where a user is asked if they want to remain signed into this browser to make further logins easier. For more details, see https://techcommunity.microsoft.com/t5/Azure-Active-Directory/The-new-Azure-AD-sign-in-and-Keep-me-signed-in-experiences/td-p/128267
50141|||||Protected key is not intended for the authenticated user.|||||No Remediation Provided
50142|||||Password change is required due to a conditional access policy.|||||No Remediation Provided
50143|||||Session mismatch. The session is invalid because user tenant does not match the domain hint.|||||The app attempted to sign in a user to the wrong tenant. They need to correctly track the tenant that they have signed the user into.
50144|||||The user's Active Directory password has expired.|||||Generate a new password for the user or have the user use the self-service reset tool to reset their password.
50146|||||This application is required to be configured with an application-specific signing key. It is either not configured with one, or the key has expired or is not yet valid.|||||Please contact the owner of the application.
50147|||||Invalid size of the code challenge parameter.|||||Contact the application owner to correct their use of the PKCE parameters.
50148|||||The code_verifier does not match the code_challenge supplied in the authorization request for PKCE.|||||Contact the application owner to correct their use of the PKCE parameters.
50149|||||Invalid Code_Challenge_method parameter.|||||No Remediation Provided
50150|||||The provided credentials does not have a valid user consent approval information.|||||No Remediation Provided
50155|||||Device authentication failed.|||||No Remediation Provided
50156|||||Device tokens are not supported for V2 resource.|||||No Remediation Provided
50157|||||User redirection required for routing.|||||No Remediation Provided
50158|||||External security challenge not satisfied. User will be redirected to another page or authentication provider to satisfy additional authentication challenges.|||||The user is required to satisfy additional requirements before finishing authentication, and was redirected to another page (such as terms of use or a third party MFA provider). This code alone does not indicate a failure on your users part to sign in. The sign in logs may indicate that this challenge was succesfully passed or failed.
50159|||||Claims sent by external provider are not enough.|||||No Remediation Provided
50161|||||Failed to validate authorization url of external claims provider.|||||No Remediation Provided
50162|||||Claims transformation has timed out. This indicates too many or too complex transformations may have been configured for this application. A retry of the request may succeed. Otherwise, please contact your admin to fix the configuration.|||||No Remediation Provided
50163|||||Regular expression replacement for claims transformation has resulted in a claim which exceeds the size limit. Please contact your admin to fix the configuration.|||||No Remediation Provided
50164|||||The supplied access token was not issued for the purpose for which it is being used. Expected a token with purpose '{name}'.|||||No Remediation Provided
50165|||||The token encrypting algorithm '{algorithm}' requested by the application is not supported for this type of token. This indicates the application is misconfigured.|||||No Remediation Provided
50166|||||Request to External OIDC endpoint failed.|||||No Remediation Provided
50167|||||Invalid pop_jwk key.|||||No Remediation Provided
50168|||||The client is capable of utilizing the Windows 10 Accounts extension to perform SSO but no SSO token was found in the request or the token was expired. Request has been interrupted to attempt to pull an SSO token.|||||No Remediation Provided
50169|||||The realm '{realm}' is not a configured realm of the current service namespace.|||||No Remediation Provided
50170|||||The external controls mapping is missing.|||||No Remediation Provided
50172|||||External claims provider {provider} is not approved.|||||No Remediation Provided
50173|||||The provided grant has expired due to it being revoked, a fresh auth token is needed. The user might have changed or reset their password. The grant was issued on '{authTime}' and the TokensValidFrom date (before which tokens are not valid) for this user is '{validDate}'.|||||Expected part of the token lifecycle - either an admin or a user revoked the tokens for this user, causing subsequent token refreshes to fail and require re-authentication. Have the user sign-in again.
50176|||||Missing definition of external control: {controlId}.|||||No Remediation Provided
50177|||||User account '{user}' from identity provider '{idp}' does not exist in tenant '{tenant}' and cannot access the application '{appId}'({appName}) in that tenant. The account needs to be added as an external user in the tenant first. Sign out and sign in again with a different Azure Active Directory user account.|||||The account needs to be added as an external user in the tenant first. Sign out and sign in again with a different Azure Active Directory user account.
50178|||||User account '{user}' from identity provider '{idp}' does not exist in tenant '{tenant}' and cannot access the application '{appId}'({appName}) in that tenant. The account needs to be added as an external user in the tenant first. Sign out and sign in again with a different Azure Active Directory user account.|||||The account needs to be added as an external user in the tenant first. Sign out and sign in again with a different Azure Active Directory user account.
50179|||||Client_info is not supported for this user.|||||No Remediation Provided
50180|||||Integrated Windows Authentication is needed. Enable the tenant '{name}' for Seamless SSO.|||||No Remediation Provided
50181|||||Unable to validate the otp.|||||No Remediation Provided
50182|||||OTP is already expired.|||||No Remediation Provided
50183|||||Cannot lookup otp due to cache error.|||||No Remediation Provided
50184|||||No cache entry exist for the tenant/user.|||||No Remediation Provided
50185|||||Email OTP notification delivery failed.|||||No Remediation Provided
50186|||||Unpermitted realm.|||||No Remediation Provided
50187|||||Failed to perform device authentication.|||||No Remediation Provided
50189|||||The device code is not correctly formatted.|||||No Remediation Provided
50190|||||Region prefix to connection string mapping returned from settings is null.|||||No Remediation Provided
50192|||||Invalid request.|||||No Remediation Provided
50193|||||Internal use|||||No Remediation Provided
50194|||||Application '{appId}'({appName}) is not configured as a multi-tenant application. Usage of the /common endpoint is not supported for such applications created after '{time}'. Use a tenant-specific endpoint or configure the application to be multi-tenant.|||||No Remediation Provided
50196|||||The server terminated an operation because it encountered a client request loop. Please contact your app vendor.|||||Application error - the app is requesting too many tokens, indicating that it is not correctly coded. Ensure that the app is correctly caching refresh and access tokens to preserve bandwidth and reduce latency.
50197|||||Sorry, we could not find the user, please sign-in again.|||||No Remediation Provided
50199|||||For security reasons, user confirmation is required for this request. Please repeat the request allowing user interaction.|||||No Remediation Provided
50200|||||Unpermitted external trusted realm.|||||No Remediation Provided
50201|||||This message prompt interrupt will be shown to the user during login when additional information should be provided to user.|||||No Remediation Provided
50202|||||User is not registered in the organization and must explicitly consent to the sign-in.|||||No Remediation Provided
50203|||||User has not registered the authenticator app and must register or snooze this notification.|||||No Remediation Provided
50204|||||External user has not consented to the privacy statement.|||||No Remediation Provided
50205|||||External user has consented to the privacy statement.|||||No Remediation Provided
50206|||||The user or administrator has not consented connecting to the target-device: '{identifier}'. Send an interactive authorization request for this user and target-machine.|||||No Remediation Provided
51000|||||{feature} is/are disabled.|||||No Remediation Provided
51001|||||Domain Hint must be present with On-Premises Security Identifier/ On-Premises UPN.|||||No Remediation Provided
51002|||||Access denied due to it's in deny user access block list.|||||No Remediation Provided
51004|||||The user account {identifier} does not exist in the {tenant} directory. To sign into this application, the account must be added to the directory.|||||An application likely chose the wrong tenant to sign into, and the currently logged in user was prevented from doing so since they did not exist in your tenant. If this user should be able to log in, add them as a guest. See docs here: https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator
51005|||||Initiate gateway redirect.|||||This is not an error scenario, but is handled like one by Azure AD to handle certain authentication flows.  This is not an indication that anything went wrong.
51006|||||Integrated Windows Authentication is needed. The user signed in using session token that is missing wia claim. Prompt the user to sign in again.|||||No Remediation Provided
51007|||||The user account {identifier} does not exist in the {tenant} directory. The user will be added to the directory to sign into this application.|||||No Remediation Provided
51008|||||JIT user creation of {userType} is disabled.|||||No Remediation Provided
52001|||||LinkedIn AppFamily Service Principal is disabled.|||||No Remediation Provided
52002|||||Non-retryable error has occurred.|||||No Remediation Provided
52003|||||Non-retryable error has occurred.|||||No Remediation Provided
52004|||||The user or administrator has not consented to use the application with ID '{identifier}'{namePhrase}. Send an interactive authorization request for this user and resource.|||||No Remediation Provided
52050|||||Multiple users with same email have been found.|||||No Remediation Provided
52051|||||Timed-out while parsing extension property name.|||||No Remediation Provided
53000|||||Device is not in required device state: {state}. Conditional Access policy requires a compliant device, and the device is not compliant. The user must enroll their device with an approved MDM provider like Intune.|||||Your administrator might have configured a conditional access policy that allows access to your organization's resources only from compliant devices. To be compliant, your device must be either joined to your on-premises Active Directory or joined to your Azure Active Directory.            More details available at https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-device-remediation
53001|||||Device is not in required device state: {state}. Conditional Access policy requires a domain joined device, and the device is not domain joined.|||||Have the user use a domain joined device.
53002|||||Device is not in required device state: {state}. The app used is not an approved app for Conditional Access.|||||User needs to use one of the apps from the list of approved apps to use in order to get access.
53003|||||Access has been blocked by Conditional Access policies. The access policy does not allow token issuance.|||||If this is unexpected, see the conditional access policy that applied to this request in the Azure Portal.
53004|||||Cannot configure multi-factor authentication methods due to suspicious activity.|||||No Remediation Provided
53005|||||Application needs to enforce Intune protection policies.|||||No Remediation Provided
53006|||||Authentication required from federated idP.|||||No Remediation Provided
53007|||||Authentication required from federated IDP.|||||User was blocked from authentication because they need to be sent to the federated identity provider (ADFS, for example) to perform multi-factor authentication. On interactive sign-in requests, they will be sent to the federation provider to perform MFA.
53008|||||Browser not supported.|||||No Remediation Provided
53009|||||Application needs to enforce Intune protection policies.|||||No Remediation Provided
53010|||||Cannot configure multi-factor authentication methods because the organization requires this information to be set from specific locations or devices.|||||No Remediation Provided
53011|||||User blocked due to risk on home tenant.|||||No Remediation Provided
54000|||||User is not allowed to access application {appName} due to Legal Age Group Requirement of application {audience}.|||||No Remediation Provided
54005|||||OAuth2 Authorization code was already redeemed, please retry with a new valid code or use an existing refresh token.|||||No Remediation Provided
54006|||||Unencrypted v2 access tokens are not supported for first party applications that support consumer accounts. The resource must add a certificate to the onboarding portal to encrypt tokens.|||||No Remediation Provided
54007|||||Method not supported for IDP OAuth2 Federation.|||||No Remediation Provided
54008|||||Multi-Factor authentication is required and the credential used ({credentialName}) is not supported as a First Factor. Contact your administrator for more information.|||||No Remediation Provided
60007|||||X509Certificate does not expose a private key or isn't an RSA private key.|||||No Remediation Provided
65001|||||The user or administrator has not consented to use the application with ID '{identifier}'{namePhrase}. Send an interactive authorization request for this user and resource.|||||No Remediation Provided
65002|||||Consent between first party application '{applicationId}' and first party resource '{resourceId}' must be configured via preauthorization - applications owned and operated by Microsoft must get approval from the API owner before requesting tokens for that API.|||||A developer in your tenant may be attempting to reuse an App ID owned by Microsoft. This error prevents them from impersonating a Microsoft application to call other APIs. They must move to another app ID they register in portal.azure.com.
65003|||||Consent for first party token-to-self must be configured via preauthorization. If preauthorization has already been configured, update the request to use a URI identifier for the resource instead of '{resourceId}' to work around this error.|||||The application developer needs to modify how the resource is specified in the authentication request to work around an implementation limitation.
65004|||||User declined to consent to access the app.|||||Have the user retry the sign-in and consent to the app.
65005|||||The application '{name}' asked for scope '{scope}' that doesn't exist.|||||No Remediation Provided
65006|||||Resource '{resourceId}' had no entitlements matching required permissions configured on the required resource access for client '{clientId}'. Requested permission IDs: '{permissionId}'. This is a problem with one or more invalid permission ids on the client RRA configuration or the resource entitlement configuration.|||||No Remediation Provided
65007|||||Client '{clientId}' required resource access configuration has changed and therefore the request could not be completed. Please try again.|||||No Remediation Provided
67001|||||The resource '{resourceId}' is not a valid protected resource.|||||No Remediation Provided
67002|||||User consent is required to create a new delegation or extend an expired delegation. NameId: {claimId} IdentityProvider: {idp} Actor: {resourceId} RequestorPrincipal: {appId}({appName}).|||||No Remediation Provided
67003|||||The client '{appId}'({appName}) is not a valid service identity.|||||No Remediation Provided
67006|||||The service identity '{appId}'({appName}) is not trusted for delegation.|||||No Remediation Provided
67007|||||Unknown consent value '{value}'. Valid values are 'AdministratorConsentProvided', 'UseExistingUserConsent', and 'UserConsentProvided'.|||||No Remediation Provided
69998|||||OfficeS2S delegation redemption scenarios are not supported for resource '{resourceId}'.|||||No Remediation Provided
70000|||||Provided grant is invalid or malformed.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
70001|||||Application identifier is not provided.|||||No Remediation Provided
70002|||||Client application name '{appName}' is not valid or the credentials used to authenticate the client could not be understood by the server.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
70003|||||The app requested an unsupported grant type '{type}'.|||||No Remediation Provided
70004|||||The app requested an invalid redirect URI '{uri}'. The redirect address specified by the client does not match any configured addresses.|||||No Remediation Provided
70005|||||'The application requested an unsupported response type '{type}' when requesting a token.|||||Contact the application owner.
70006|||||Internal use|||||No Remediation Provided
70007|||||The application requested an unsupported mode '{mode}' when requesting a token.|||||Contact the application owner.
70008|||||The provided authorization code or refresh token has expired due to inactivity. Send a new interactive authorization request for this user and resource.|||||Expected - auth codes, refresh tokens, and sessions expire over time or are revoked by the user or an admin. The app will request a new login from the user.
70009|||||Unable to complete OAuth2 IdP's sign in. The 'state' parameter could not be validated.|||||No Remediation Provided
70010|||||Unable to complete OAuth2 IdP's sign in. The 'state' parameter does not match the expected value.|||||No Remediation Provided
70011|||||The provided request must include a 'scope' input parameter. The provided value for the input parameter 'scope' is not valid. The scope {scope} is not valid.{detailsPhrase}|||||No Remediation Provided
70012|||||A server error occurred while authenticating an MSA (consumer) user.|||||Try again. If it continues to fail, open a support ticket: https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-troubleshooting-support-howto
70013|||||The '{paramName}' request parameter is not supported.|||||No Remediation Provided
70014|||||The '{paramName}' request parameter is not supported.|||||No Remediation Provided
70015|||||The '{paramName}' request parameter is not supported.|||||No Remediation Provided
70016|||||OAuth 2.0 device flow error. Authorization is pending. Continue polling.|||||This is not an error scenario, but is handled like one by Azure AD to handle certain authentication flows.  This is not an indication that anything went wrong.
70017|||||Authorization declined.|||||No Remediation Provided
70018|||||Invalid verification code.|||||No Remediation Provided
70019|||||Verification code expired.|||||Verification code expired. Have the user retry the sign-in
70020|||||The provided value for the input parameter 'device_code' is not valid. This device code has expired.|||||Please make a new Device Authorization Request.
70021|||||No matching federated identity record found for presented assertion. Assertion Issuer: '{issuer}'. Assertion Subject: '{subject}'. Assertion Audience: '{audience}'. https://docs.microsoft.com/en-us/azure/active-directory/develop/workload-identity-federation|||||Application configuration issue. Ensure that the federated credential policy on the application registration is correct, and ensure that the developer is correctly submitting a token that complies with the policy requirements. See documentation at https://docs.microsoft.com/en-us/azure/active-directory/develop/workload-identity-federation.
70022|||||Federated Identity Credential issuer must use HTTPS scheme, must not be loopback address, and may not include a query-string or fragment. Token issuer: {issuer}.|||||Ensure that the OpenID Connect metadata for this federated credential is hosted on an HTTPS endpoint, does not point to loopback (127.0.0.1, localhost, etc.), and does not include a query-string or fragment.
70023|||||External OIDC Provider token must have a lifetime of less than or equal to {maxTime}. Token issued at {issuedAt}. Token expires on {expires}.|||||Supply tokens that have lifetime of less than or equal to the maximum allowed time.
70024|||||OIDC Provider Metadata missing required field '{fieldName}'.|||||Ensure that the OpenID Connect metadata sets all required fields.
70030|||||Remote authentication failed to read session from storage.|||||No Remediation Provided
70031|||||Remote authentication session is in a bad state.|||||No Remediation Provided
70033|||||The remote auth session with this device code has already been approved.|||||No Remediation Provided
70034|||||The remote auth session with this device code has already been denied.|||||No Remediation Provided
70035|||||Remote auth session with this device code doesn't exist.|||||No Remediation Provided
70036|||||Unsupported remote auth session state.|||||No Remediation Provided
70037|||||Incorrect challenge response provided. Remote auth session denied.|||||Incorrect challenge response provided. Remote auth session denied
70039|||||The remote auth session with this device code has expired.|||||No Remediation Provided
70041|||||Unable to complete OAuth2 IdP's sign in. The 'nonce' claim does not match the expected value.|||||No Remediation Provided
70043|||||The refresh token has expired or is invalid due to sign-in frequency checks by conditional access. The token was issued on {issueDate} and the maximum allowed lifetime for this request is {time}.|||||No Remediation Provided
70044|||||The session has expired or is invalid due to sign-in frequency checks by conditional access.|||||No Remediation Provided
70045|||||The refresh token is invalid due to sign-in frequency checks by conditional access. Additionally, since the sign-in frequency policy applies to all applications, the token will never be usable, and should be deleted. The token was issued on {issueDate} and the maximum allowed lifetime for this request is {time}.|||||No Remediation Provided
70046|||||The session has expired or is invalid due to re-authentication checks by conditional access.|||||No Remediation Provided
70071|||||Invalid requested token type: {type}.|||||No Remediation Provided
70101|||||Internal use|||||No Remediation Provided
75001|||||An exception occurred while parsing a SAML binding message.|||||No Remediation Provided
75005|||||The request is not a valid SAML 2.0 protocol message.|||||No Remediation Provided
75008|||||Received SAML request with an unexpected destination '{actualDest}'. Expected one of '{validDests}'.|||||The request from the application was denied since the SAML request had an unexpected destination. Contact the application owner
75011|||||Authentication method '{usedMethod}' by which the user authenticated with the service doesn't match requested authentication method '{requestedMethod}'. Contact the {appName} application owner.|||||Authentication method by which the user authenticated with the service doesn't match requested authentication method. Contact the application owner
75016|||||The SP name qualifier '{name}' is not valid.|||||No Remediation Provided
75019|||||A domain hint can be specified either in the AuthnRequest or as a query string parameter, but not both.|||||Contact the application owner.
75020|||||Non-retryable error has occurred.|||||No Remediation Provided
76020|||||Application configured to use only protocols with signed requests|||||No Remediation Provided
76021|||||The request sent by client is not signed while the application requires signed requests|||||No Remediation Provided
76022|||||Cannot verify the signature of received authentication request since there is no certificate for verification configured in the application.|||||No Remediation Provided
76023|||||The signature of the received authentication request is invalid, please contact the administrator to resolve the issue.|||||No Remediation Provided
76024|||||The request has no information about the public certificate for signature validation, while the {certsLimit} most recent certificates did not verify the signature.|||||No Remediation Provided
76025|||||The request has no information about the signature algorithm used for signing.|||||No Remediation Provided
76026|||||The request has expired. Try to submit new request.|||||No Remediation Provided
76027|||||No certificate matching provided KeyInfo. Check that app is configured correctly.|||||No Remediation Provided
76028|||||Signature algorithm used to sign data is not supported.|||||No Remediation Provided
76029|||||The request signature could not be validated while it's required by application settings|||||No Remediation Provided
76030|||||The request signature has incorrect format|||||No Remediation Provided
76031|||||This endpoint does not support SAML request signing.|||||No Remediation Provided
76032|||||This service principal ID is not a GUID.|||||No Remediation Provided
80001|||||No Microsoft Azure AD Connect Authentication Agent was found. Make sure that your environment is configured correctly. If your directory is set for pass-through authentication, make sure that your Microsoft Azure AD Connect Authentication Agent is online.|||||Authentication Agent unable to connect to Active Directory. Make sure the authentication agent is installed on a domain-joined machine that has line of sight to a data center that can serve the user's login request
80002|||||Internal error. Password validation request timed out. We were unable to either send the authentication request to the internal Hybrid Identity Service.|||||Make sure that your on-premises Active Directory instance is available and responding to requests from the agents.
80003|||||Unknown status returned from on-prem password validator.|||||Invalid response received by Authentication Agent. An unknown error occurred while attempting to authentication against Active Directory on-premises.
80005|||||An unknown error occurred while processing the response from the Authentication Agent.|||||Retry the request and ensure that your on-premises AD instance is operating correctly. If it continues to fail, open a support ticket to get more details on the error: https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-troubleshooting-support-howto
80006|||||Invalid on-prem password validation configuration: request URL must be secure over https.|||||No Remediation Provided
80007|||||The Authentication Agent is unable to validate user's password. Check the agent logs for more info and verify that Active Directory is operating as expected.|||||Contact your administrator for more information.
80010|||||Cannot encrypt with key identifier '{key}'. The Authentication Agent is unable to decrypt password.|||||No Remediation Provided
80011|||||Unexpected error retrieving password encryption keys.|||||No Remediation Provided
80012|||||Your account has time restrictions that keep you from signing in right now.|||||The users attempted to log on outside of the allowed hours (this is specified in AD)
80013|||||The authentication attempt could not be completed due to time skew (time/date difference) between the machine running the authentication agent and AD.|||||Fix time sync issues
80014|||||Validation request responded after maximum elapsed time exceeded.|||||Authentication agent timed out. Open a support ticket with the error code, correlation ID, and timestamp to get more details on this error
80015|||||Validation request budget exceeded.|||||No Remediation Provided
80016|||||Validation request failed - unable to signal Authentication Agent.|||||No Remediation Provided
80017|||||An error occurred while decrypting user credentials. Check your Microsoft Azure AD Connect Authentication Agent logs for more information.|||||No Remediation Provided
80018|||||Unauthorized or forbidden access of encryption keys.|||||No Remediation Provided
81001|||||Service ticket size exceeded the maximum allowed.|||||User's Kerberos ticket is too large. This can happen if the user is in too many groups and thus the Kerberos ticket contains too many group memberships. Reduce the user's group memberships and try again
81004|||||Kerberos authentication failed.|||||No Remediation Provided
81005|||||Authentication package is not supported.|||||No Remediation Provided
81006|||||No authorization header was found, returning 401 WWW-Authenticate.|||||No Remediation Provided
81007|||||Tenant is not enabled for DesktopSSO.|||||No Remediation Provided
81008|||||Failed to validate Kerberos ticket.|||||No Remediation Provided
81009|||||Unable to validate the user's Kerberos ticket, the authorization header value is not formatted correctly.|||||No Remediation Provided
81010|||||Seamless SSO failed because the user's Kerberos ticket has expired or is invalid.|||||No Remediation Provided
81011|||||Failed to find user by on-premise SID in the user's Kerberos ticket.|||||No Remediation Provided
81012|||||The user trying to sign in to Azure AD is different from the user signed into the device.|||||This is not an error condition. It indicates that user trying to sign in to AzureAD is different from the user signed into the device. You can safely ignore this code in the logs
81013|||||Failed to lookup the user whose kerberos ticket was used to login.|||||No Remediation Provided
81014|||||The DesktopSSO auth token has expired.|||||No Remediation Provided
81015|||||Rejecting DesktopSSO Kerberos ticket as it was obtained through delegation. Delegated Kerberos ticket does not originate from user directly. Please contact your tenant administrator to disable delegation on the AZUREADSSOACC account.|||||No Remediation Provided
81016|||||Invalid STS request.|||||No Remediation Provided
90000|||||Internal use|||||No Remediation Provided
90002|||||Tenant '{tenant_name}' not found. Check to make sure you have the correct tenant ID and are signing into the correct cloud. Check with your subscription administrator, this may happen if there are no active subscriptions for the tenant.|||||The application developer will recieve this error if their app attempts to sign into a tenant that we cannot find. Often, this is because a cross-cloud app was used against the wrong cloud, or the developer attempted to sign in to a tenant derived from an email address, byut the domain isn't registered.
90004|||||The request is not properly formatted.|||||No Remediation Provided
90005|||||Unable to complete request. The request was invalid since SID and login_hint cannot be used together.|||||No Remediation Provided
90006|||||A transient error has occurred. Please try again.|||||No Remediation Provided
90007|||||Bad Request. The passed session ID cannot be parsed.|||||No Remediation Provided
90008|||||The user or administrator has not consented to use the application with ID '{appId}'({appName}). This happened because application is misconfigured: it must require access to Microsoft Graph by specifying at least 'Sign in and read user profile' permission.|||||This happened because application is misconfigured: it must require access to Microsoft Graph by specifying at least 'Sign in and read user profile' permission.
90009|||||Application '{appId}'({appName}) is requesting a token for itself. This scenario is supported only if resource is specified using the GUID based App Identifier.|||||No Remediation Provided
90010|||||Unable to create {algoName} algorithm.|||||Contact the application developer. The request is not supported for various reasons. For example, the request is made using an unsupported request method (only POST method is supported) or the token signing algorithm that was requested is not supported.
90012|||||This request has timed out.|||||No Remediation Provided
90013|||||Invalid input received from the user.|||||No Remediation Provided
90014|||||The required field '{name}' is missing from the credential. Ensure that you have all the necessary parameters for the login request.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
90015|||||Requested query string is too long.|||||No Remediation Provided
90016|||||Invalid access token. Required claim is missing.|||||No Remediation Provided
90017|||||Unexpected field '{fieldName}'.|||||No Remediation Provided
90019|||||No tenant-identifying information found in either the request or implied by any provided credentials.|||||Application error - the request can't be routed to a tenant, but needs to be.
90020|||||The SAML 1.1 Assertion is missing ImmutableID of the user.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
90022|||||Principal name format is invalid for '{name}'. Expected format: name[/instance][@realm]. The principal name is required, host and realm are optional and may be set to null.|||||No Remediation Provided
90023|||||Invalid STS request.|||||No Remediation Provided
90024|||||A transient error has occurred. Please try again.|||||No Remediation Provided
90025|||||Request processing has exceeded gateway allowance.|||||No Remediation Provided
90026|||||Hostname contains an invalid wildcard '*' character.|||||No Remediation Provided
90027|||||We are unable to issue tokens from this API version on the MSA tenant. Please contact the application vendor as they need to use version 2.0 of the protocol to support this.|||||No Remediation Provided
90028|||||Principal name format is invalid for name '{name}'. Primary component of the name is required.|||||No Remediation Provided
90029|||||The realm '{name}' is a Unicode domain name. Domain names of this form are not supported.|||||No Remediation Provided
90030|||||A transient error has occurred. Try again after some time.|||||No Remediation Provided
90031|||||A transient error has occurred. Try again after some time.|||||No Remediation Provided
90032|||||A transient error has occurred. Try again after some time.|||||No Remediation Provided
90033|||||A transient error has occurred. Please try again.|||||No Remediation Provided
90035|||||Service is temporarily unavailable. Please retry later.|||||No Remediation Provided
90036|||||An unexpected, non-retryable error stemming from the directory service has occurred.|||||If you see this consistently, open a support ticket to get more details on the error: https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-troubleshooting-support-howto
90037|||||Non-retryable error has occurred.|||||No Remediation Provided
90038|||||Tenant '{tenant_name}' request is being redirected to the National Cloud '{cloud}'.|||||No Remediation Provided
90039|||||Service is temporarily unavailable. Please retry later.|||||No Remediation Provided
90040|||||A non-retryable error has occurred.|||||No Remediation Provided
90041|||||A transient error has occurred. Please try again.|||||No Remediation Provided
90042|||||National Cloud Name is missing in the postback request.|||||No Remediation Provided
90043|||||OAuth2 grant was issued by National Cloud STS.|||||This is not an error scenario, but is handled like one by Azure AD to handle certain authentication flows.  This is not an indication that anything went wrong.
90044|||||National Cloud Request Process Switched off.|||||No Remediation Provided
90045|||||Service is too busy. Please try again later.|||||No Remediation Provided
90046|||||Internal use|||||No Remediation Provided
90047|||||Internal use|||||No Remediation Provided
90049|||||Application could not be found.|||||No Remediation Provided
90050|||||Response content length from external IdP exceeds supported limit.|||||No Remediation Provided
90051|||||Invalid Delegation Token. Invalid national Cloud ID ({cloudId}) is specified.|||||No Remediation Provided
90052|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
90053|||||Internal use|||||No Remediation Provided
90055|||||The server has terminated the request due to excessive request rate. Please wait a few seconds and try again.|||||Your tenant has sent too many requests to AAD, triggering anti-abuse throttling measures. Please check to see if there are any misbehaving applications that are sending too many requests to AAD.
90056|||||Requested resource cannot be found.|||||No Remediation Provided
90057|||||Server encountered an internal problem.|||||No Remediation Provided
90058|||||Service is temporarily unavailable. Please retry later.|||||No Remediation Provided
90059|||||HealthInfoController Failed with the following Exception: {ex}|||||No Remediation Provided
90061|||||Request to External OIDC endpoint failed.|||||No Remediation Provided
90071|||||An admin from {tenant} must update their access settings to accept inbound multifactor authentication.|||||No Remediation Provided
90072|||||User account '{user}' from identity provider '{idp}' does not exist in tenant '{tenant}' and cannot access the application '{application}'({appName}) in that tenant. The account needs to be added as an external user in the tenant first. Sign out and sign in again with a different Azure Active Directory user account|||||The account needs to be added as an external user in the tenant first. Sign out and sign in again with a different Azure Active Directory user account
90073|||||Invalid Fairfax Gateway Redirect.|||||No Remediation Provided
90081|||||An error occurred when the service tried to process a WS-Federation message. The message was invalid.|||||No Remediation Provided
90082|||||Authentication policy '{name}' selected for the request is not currently supported.|||||No Remediation Provided
90083|||||Request is unsupported.|||||No Remediation Provided
90084|||||Guest accounts are not allowed for this site.|||||No Remediation Provided
90085|||||The service is unable to issue a token because the company object hasn't been provisioned yet.|||||No Remediation Provided
90086|||||The user DA token is expired.|||||No Remediation Provided
90087|||||An error occurred while creating the WS-Federation message from the URI.|||||No Remediation Provided
90088|||||Authentication failed due to email address domain is not in allowed domains list for identity provider.|||||The email address domain is not in the application's whitelisted domains.
90089|||||User token should not be used in App on behalf of flow.|||||No Remediation Provided
90090|||||A transient error has occurred. Please try again.|||||No Remediation Provided
90091|||||A transient error has occurred. Please try again.|||||No Remediation Provided
90092|||||Non-retryable error has occurred.|||||No Remediation Provided
90093|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
90094|||||Admin consent is required for the permissions requested by this application.|||||Ask your tenant administrator to provide consent for this application.
90095|||||Admin consent is required for the permissions requested by this application. An admin consent request may be sent to the admin.|||||No Remediation Provided
90096|||||Admin consent is required for the permissions requested by this application. Admin consent request sent for processing.|||||No Remediation Provided
90097|||||An error has occured during admin consent processing.|||||No Remediation Provided
90098|||||An unexpected approval request ID was provided.|||||No Remediation Provided
90099|||||The application '{appId}' ({appName}) has not been authorized in the tenant '{tenant}'. Applications must be authorized to access the customer tenant before partner delegated administrators can use them.|||||Provide pre-consent or execute the appropriate Partner Center API to authorize the application.
90100|||||{name} parameter is empty or not valid.|||||No Remediation Provided
90101|||||The supplied data isn't a valid email address. Please provide it in the format someone@example.com|||||Application or user error - if this persists, reach out to the impacted user or developer for more details.
90102|||||'{name}' value must be a valid absolute URI.|||||No Remediation Provided
90107|||||The request is not valid. Make sure your data doesn't have invalid characters.|||||No Remediation Provided
90112|||||Application identifier is expected to be a GUID.|||||No Remediation Provided
90114|||||The specified bulk AADJ token expiration timestamp will cause an expired token to be issued.|||||No Remediation Provided
90115|||||Code/npotc parameter is not allowed together with password.|||||No Remediation Provided
90116|||||{method} request is made, while POST is the only supported verb.|||||No Remediation Provided
90117|||||Invalid request.|||||No Remediation Provided
90119|||||The user code is null or missing.|||||No Remediation Provided
90120|||||This request was already authorized or declined.|||||No Remediation Provided
90121|||||Invalid empty request.|||||No Remediation Provided
90122|||||User identifier is not present.|||||No Remediation Provided
90123|||||The token can't be issued because the identity or claim issuance provider denied the request. Response code: {errorCode}.|||||No Remediation Provided
90124|||||{resConstant} '{resourceId}' {resourceName} is not supported over the /common or /consumers endpoints. Please use the /organizations or tenant-specific endpoint.|||||Use the /organizations or tenant-specific endpoint.
90125|||||{userName} isn't in our system. Make sure you entered the user name correctly.|||||No Remediation Provided
90126|||||User Type is not supported on this endpoint. The system can't infer the user's tenant from the user name: {userName}|||||No Remediation Provided
90128|||||Unable to load OptIn store for user.|||||No Remediation Provided
90129|||||{resConstant} '{resourceId}' {resourceName} has a configured token version of '1' and is not supported over the /common or /consumers endpoints.|||||No Remediation Provided
90130|||||{appConstant} '{appId}' {appName} is not supported over the /common or /consumers endpoints. Please use the /organizations or tenant-specific endpoint.|||||No Remediation Provided
90131|||||Invalid ambiguous request. sid cannot be used with prompt {prompt}.|||||No Remediation Provided
90132|||||The provided value for the input parameter 'device_code' is not valid. Device codes supporting the personal Microsoft Account sign-in audience can only be used for v2 common or consumers tenants.|||||No Remediation Provided
90133|||||Device Code flow is not supported under /common or /consumers endpoint.|||||No Remediation Provided
90134|||||Retrieving claims from identity provider '{idp}' failed.|||||No Remediation Provided
90135|||||The user decided not to continue the authentication. No remediation is required.|||||No Remediation Provided
90136|||||Device Code flow is not supported for Confidential Clients.|||||No Remediation Provided
90137|||||Token issuance cannot proceed because user declined consent approval to release their profile information.|||||No Remediation Provided
90138|||||Invalid ambiguous request. sid cannot be used with login_hint.|||||No Remediation Provided
90150|||||Failed to read request.|||||No Remediation Provided
90160|||||An internal error occurred while attempting to remediate the user.|||||No Remediation Provided
90170|||||An internal error occured while attempting to proxy binding redirect request|||||No Remediation Provided
90171|||||An internal error occured for cell based fallback|||||No Remediation Provided
90201|||||Non-retryable error has occurred.|||||No Remediation Provided
90202|||||A transient error has occurred. Please try again.|||||No Remediation Provided
90401|||||Access denied.|||||No Remediation Provided
90500|||||Tenant belongs to fault domain {domain}.|||||This is not an error scenario, but is handled like one by Azure AD to handle certain authentication flows.  This is not an indication that anything went wrong.
90501|||||Tenant ({name} ({identifier})) request is being redirected to USGov.|||||No Remediation Provided
100000|||||The Regional Cache Auth Service does not have the encrypted global signing key.|||||No Remediation Provided
100001|||||The Regional Cache Auth Service fails to retrieve the global signing key.|||||No Remediation Provided
100002|||||Non-retryable error has occurred in regional cache.|||||No Remediation Provided
100003|||||Timeout occurred in request to global sts.|||||No Remediation Provided
100004|||||Empty or Error response from Global Sts when called in by Regional Cache Auth instance.|||||No Remediation Provided
100005|||||Regional Cache Auth instance is not allowed to issue a token for this environment.|||||No Remediation Provided
100006|||||Regional Cache Auth Service token requests for audience App that requires custom signing keys or that has claims mapping policy are forbidden.|||||No Remediation Provided
100007|||||AAD Regional ONLY supports auth either for MSIs OR for requests from MSAL using SN+I for 1P apps or 3P apps in Microsoft infrastructure tenants.|||||No Remediation Provided
100008|||||Regional Cache Auth Service token requests for audience App that has opted in for a PFT token is forbidden.|||||No Remediation Provided
100009|||||Regional Cache Auth Service token requests for flows that require encrypted tokens are forbidden.|||||No Remediation Provided
100010|||||App specific discovery requests for Regional Cache Auth Service are forbidden.|||||No Remediation Provided
100011|||||Tenant Domain Name specific discovery requests for Regional Cache Auth Service are forbidden.|||||No Remediation Provided
100012|||||MSAonly tenant specific discovery requests for MSA tenant for Regional Cache Auth Service are forbidden.|||||No Remediation Provided
100013|||||The current discovery keys requests scenarios for Regional Cache Auth Service are forbidden.|||||No Remediation Provided
100014|||||Force cache flow parameter was specified as true but no cached response was found|||||No Remediation Provided
100015|||||Regional Cache Auth Pipeline miss StsTenant|||||No Remediation Provided
100016|||||Regional Cache Auth Pipeline missing Signing credentials|||||No Remediation Provided
100017|||||There was an error issuing a token or an issue with our sign-in service.|||||If this persists, open a support ticket to resolve this issue: https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-troubleshooting-support-howto
100018|||||The regional cache auth requests that expects confirmation (cnf) claim in the token response are forbidden.|||||No Remediation Provided
100019|||||The regional cache auth requests from tenants with token lifetime policy defined are forbidden.|||||No Remediation Provided
100020|||||Regional key discovery endpoint is forbidden.|||||No Remediation Provided
100021|||||The regional cache auth requests that reach max hop count are dropped.|||||No Remediation Provided
100022|||||The request was failed due to AAD outage simulation for a participating tenant.|||||No Remediation Provided
100023|||||Regional endpoints are not yet supported in sovereign clouds.|||||No Remediation Provided
100024|||||AAD Regional ONLY supports auth either for MSIs OR for requests from supported MSAL using SN+I for 1P apps or 3P apps in Microsoft infrastructure tenants. This request is forbidden because it comes from neither 1P app nor 3P apps in Microsoft infrastructure tenants.|||||No Remediation Provided
100026|||||AAD Regional ONLY supports auth either for MSIs OR for requests from supported MSAL using SN+I for 1P apps or 3P apps in Microsoft infrastructure tenants. This request is forbidden because it does not use SN+I.|||||No Remediation Provided
100027|||||AAD Regional does not support traffic from client application {clientId} at this time.|||||No Remediation Provided
120000|||||Incorrect password.|||||No Remediation Provided
120001|||||New password doesn't meet complexity requirements. Passwords can't contain user ID, and need to be 8-16 characters long, with at least 3 of the following: uppercase letters, lowercase letters, numbers, and symbols.|||||No Remediation Provided
120002|||||New password doesn't meet complexity requirements. Passwords can't contain user ID, and need to be 8-16 characters long, with at least 3 of the following: uppercase letters, lowercase letters, numbers, and symbols.|||||No Remediation Provided
120003|||||New password doesn't meet complexity requirements. Passwords can't contain user ID, and need to be 8-16 characters long, with at least 3 of the following: uppercase letters, lowercase letters, numbers, and symbols.|||||No Remediation Provided
120004|||||New password doesn't match the password complexity requirements of the user's company's OnPrem Active Directory.|||||No Remediation Provided
120005|||||Password was successfully updated, but servers take time to catch up. Please try signing in again in a few minutes.|||||No Remediation Provided
120006|||||Password change request got interrupted. Check if the password got updated, else try again.|||||No Remediation Provided
120012|||||User's organization does not allow them to change their password themselves through AAD.|||||No Remediation Provided
120013|||||Password change failed due to connectivity issues trying to write to user's onprem AD. Try again in a few minutes.|||||No Remediation Provided
120014|||||User account is either disabled or temporarily locked by user's organization.|||||No Remediation Provided
120015|||||Password change failed due to user account misconfiguration.|||||No Remediation Provided
120016|||||User not found.|||||No Remediation Provided
120017|||||Operation not supported.|||||No Remediation Provided
120018|||||New password does not comply with the policy. The password is too common.|||||No Remediation Provided
120019|||||New password contains a word, phrase, or pattern that is banned by a policy in user's organization.|||||No Remediation Provided
120020|||||Change user password operation failed.|||||No Remediation Provided
121000|||||Non-retryable error has occurred.|||||No Remediation Provided
121003|||||User's organization does not allow them to change their password themselves through AAD.|||||No Remediation Provided
130001|||||Signature key ID is not provided.|||||No Remediation Provided
130004|||||UserPrincipal doesn't have the NGC key configured.|||||No Remediation Provided
130005|||||NGC key signature verification failed.|||||No Remediation Provided
130006|||||The NGC transport key isn't configured on the device.|||||No Remediation Provided
130007|||||The device is disabled.|||||No Remediation Provided
130008|||||Device referenced by the NGC key is not found.|||||No Remediation Provided
130009|||||Device key was found weak.|||||No Remediation Provided
130500|||||Phone sign in was blocked due to User Credential Policy.|||||No Remediation Provided
130501|||||Sign in was blocked due to User Credential Policy.|||||No Remediation Provided
130502|||||Temporary Access Pass sign in was blocked due to User Credential Policy.|||||No Remediation Provided
130503|||||Your Temporary Access Pass is incorrect. If you don't know your pass, contact your administrator.|||||No Remediation Provided
130504|||||Your Temporary Access Pass has expired. Contact your administrator to obtain a new pass.|||||No Remediation Provided
130505|||||Your one-time Temporary Access Pass has been redeemed. Contact your admin to get a new pass.|||||No Remediation Provided
130506|||||Access Pass must be used for Web Sign In. Contact your admin to get an Access Pass.|||||No Remediation Provided
130507|||||An access pass could not be found or verified for the user.|||||No Remediation Provided
131000|||||PublicIdentifier has an invalid GUID.|||||No Remediation Provided
131001|||||A transient error has occurred. Please try again.|||||No Remediation Provided
131002|||||Non-retryable error has occurred.|||||No Remediation Provided
131003|||||A transient error has occurred. Please try again.|||||No Remediation Provided
131005|||||Phone Entry not found during GetOneTimeCode request.|||||No Remediation Provided
131006|||||Public Identifier SAS Authentication has encountered a problem.|||||No Remediation Provided
131008|||||Trying to create credential from unvalidated PIA data.|||||No Remediation Provided
131009|||||Phone Number signin is not enabled for this tenant.|||||No Remediation Provided
131010|||||User not allowed by policy conditions.|||||No Remediation Provided
131011|||||A invalid input was entered.|||||No Remediation Provided
131012|||||This attempt to sign in has been throttled.|||||No Remediation Provided
131100|||||User account has to be a resource account to request a 'resource_account' grant type.|||||No Remediation Provided
131101|||||Resource Account key is malformed.|||||No Remediation Provided
131102|||||Resource Account key signature verification failed.|||||No Remediation Provided
135000|||||Fido signature verification failed.|||||No Remediation Provided
135001|||||UserPrincipal doesn't have the key ID configured.|||||No Remediation Provided
135002|||||Fido key does not have authenticator data.|||||No Remediation Provided
135003|||||Fido assertion verification failed. Invalid gesture provided.|||||No Remediation Provided
135004|||||Invalid postBackUrl parameter.|||||No Remediation Provided
135005|||||Invalid cancelUrl parameter.|||||No Remediation Provided
135006|||||Invalid resumeUrl parameter.|||||No Remediation Provided
135007|||||Client data type is not valid.|||||No Remediation Provided
135008|||||Relying Party Origin is not valid.|||||No Remediation Provided
135009|||||Flow Token Scenario must be login scenario.|||||No Remediation Provided
135010|||||UserPrincipal doesn't have the key ID configured.|||||No Remediation Provided
135011|||||Device used during the authentication is disabled.|||||No Remediation Provided
135012|||||UserObjectId from the UserHandle does not match with UserPrincipal UserObjectId.|||||No Remediation Provided
135013|||||Invalid UserHandle prefix.|||||No Remediation Provided
135014|||||Invalid UserHandle length.|||||No Remediation Provided
135015|||||The FIDO exclude list was not a valid JSON blob.|||||No Remediation Provided
135016|||||FIDO sign-in is disabled via policy.|||||No Remediation Provided
135017|||||Unexpected Signature Counter received from authenticator.|||||No Remediation Provided
135018|||||Invalid challenge received from fido assertion.|||||No Remediation Provided
135019|||||Expired Challenge received from Fido assertion.|||||No Remediation Provided
135020|||||Invalid Fido assertion.|||||No Remediation Provided
135021|||||Invalid UserHandle prefix.|||||No Remediation Provided
135022|||||Redirect uri provided by MSA is not valid.|||||No Remediation Provided
140000|||||Request nonce is expired. Current time: {curTime}, expiry time of assertion {expTime}.|||||No Remediation Provided
140001|||||The session key is not valid.|||||No Remediation Provided
140002|||||Key not found|||||No Remediation Provided
140003|||||Nonce purpose not supported|||||No Remediation Provided
140004|||||Invalid Ticket Granting Ticket request.|||||No Remediation Provided
140005|||||Invalid Ticket Granting Ticket request.|||||No Remediation Provided
140006|||||Invalid Ticket Granting Ticket request.|||||No Remediation Provided
140007|||||Invalid Ticket Granting Service request.|||||No Remediation Provided
140008|||||Invalid ApReq assertion provided.|||||No Remediation Provided
160011|||||Selected user account was invalid.|||||No Remediation Provided
160021|||||Application requested a user session which does not exist.|||||No Remediation Provided
165000|||||Actual message content is runtime specific. Please see returned exception message for details.|||||Actual message content is runtime specific. Please see returned exception message for details.
165001|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
165002|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
165003|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
165004|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
165900|||||Invalid request.|||||No Remediation Provided
180001|||||Cannot encrypt auth ticket with key version '{version}'.|||||No Remediation Provided
180002|||||Cannot decrypt buffer with key version '{version}'.|||||No Remediation Provided
200000|||||User object type ('{type}') not expected.|||||No Remediation Provided
200001|||||Authorization code redemption cannot be forked.|||||No Remediation Provided
200121|||||Unsupported WS-Federation message of type '{messageType}'.|||||No Remediation Provided
200122|||||Invalid WS-Federation message. {paramName} parameter is required.|||||No Remediation Provided
219000|||||Cannot open pfx. Pfx bytes or password is wrong.|||||No Remediation Provided
220000|||||Authenc: cache value is expired. Date: {expectedTime}, Now: {currentTime}.|||||No Remediation Provided
220025|||||Encryption key {version} not found.|||||No Remediation Provided
220050|||||The specified encryption key version override {num} was not found in the list of keys.|||||No Remediation Provided
220100|||||Authenc decryption failed.|||||No Remediation Provided
220200|||||Authenc incorrect version.|||||No Remediation Provided
220450|||||The Chrome WebView version is not supported.|||||Developer issue - they should ensure that their app is using appropriate and supported webviews when signing in the user.
220501|||||Unable to download CRL. Invalid or no response from CRL source {source}.|||||No Remediation Provided
221000|||||The resource is not configured to accept device-only tokens.|||||No Remediation Provided
230000|||||Internal use|||||No Remediation Provided
230002|||||Internal use|||||No Remediation Provided
230003|||||Internal use|||||No Remediation Provided
230004|||||Internal use|||||No Remediation Provided
230005|||||Internal use|||||No Remediation Provided
230006|||||Internal use|||||No Remediation Provided
230007|||||Internal use|||||No Remediation Provided
230008|||||Internal use|||||No Remediation Provided
230009|||||Internal use|||||No Remediation Provided
230010|||||Internal use|||||No Remediation Provided
230011|||||Internal use|||||No Remediation Provided
230012|||||Internal use|||||No Remediation Provided
230013|||||Internal use|||||No Remediation Provided
230014|||||Internal use|||||No Remediation Provided
230015|||||Internal use|||||No Remediation Provided
230016|||||Internal use|||||No Remediation Provided
230017|||||CCS couldn't find valid user data. Data could be missing, expired or invalid.|||||No Remediation Provided
230018|||||Internal use|||||No Remediation Provided
230019|||||Internal use|||||No Remediation Provided
230020|||||Internal use|||||No Remediation Provided
230021|||||Internal use|||||No Remediation Provided
230022|||||Internal use|||||No Remediation Provided
230023|||||Internal use|||||No Remediation Provided
230024|||||Empty cached credential cert list or failed to find valid cached credential cert.|||||No Remediation Provided
230025|||||Internal use|||||No Remediation Provided
230026|||||Internal use|||||No Remediation Provided
230027|||||Internal use|||||No Remediation Provided
230028|||||Internal use|||||No Remediation Provided
230029|||||Internal use|||||No Remediation Provided
230030|||||Internal use|||||No Remediation Provided
230031|||||Internal use|||||No Remediation Provided
230032|||||User's mailbox has exceeded maximum mailbox size.|||||No Remediation Provided
230033|||||Internal use|||||No Remediation Provided
230034|||||Internal use|||||No Remediation Provided
230035|||||Internal use|||||No Remediation Provided
230036|||||Internal use|||||No Remediation Provided
230037|||||Required auth methods from cached token are not satisfied.|||||No Remediation Provided
230038|||||Retrieved token with unsupported auth methods (amr).|||||No Remediation Provided
230039|||||Exchange Api Error.|||||No Remediation Provided
230040|||||Failed to load key from Torus.|||||No Remediation Provided
230041|||||Failed to load cert from machine.|||||No Remediation Provided
230042|||||Cannot find Service Key in cache.|||||No Remediation Provided
230043|||||Cannot find public cert shared by partners in cache.|||||No Remediation Provided
230044|||||Cannot find private cert owned by CCS in cache.|||||No Remediation Provided
230045|||||Password Cred not retrieved.|||||No Remediation Provided
230046|||||SDS BEToBEMisroute error|||||No Remediation Provided
230047|||||SDS ErrorInternalServerError error|||||No Remediation Provided
230048|||||SDS ApplicationThrottled error|||||No Remediation Provided
230049|||||SDS ErrorADUnavailable error|||||No Remediation Provided
230050|||||SDS ResourceUnhealthy error|||||No Remediation Provided
230051|||||SDS ErrorItemNotFound error|||||No Remediation Provided
230052|||||SDS ErrorTooManyObjectsOpened error|||||No Remediation Provided
230053|||||SDS ErrorMailboxQuotaExceeded error|||||No Remediation Provided
230054|||||SDS MailboxNotEnabledForRESTAPI error|||||No Remediation Provided
230055|||||SDS ErrorConnectionFailed error|||||No Remediation Provided
230056|||||SDS RequestBroker--ParseUri error|||||No Remediation Provided
230057|||||SDS ErrorADOperation error|||||No Remediation Provided
230058|||||SDS ErrorDataSourceOperation error|||||No Remediation Provided
230059|||||SDS ErrorInternalServerTransientError error|||||No Remediation Provided
230060|||||SDS ErrorInvalidProperty error|||||No Remediation Provided
230061|||||Could not get enforcement event successfully|||||No Remediation Provided
230062|||||Presented or requested primary refresh token could not be supported.|||||No Remediation Provided
230063|||||Remote forest discovery is not supported on restricted forests.|||||No Remediation Provided
230064|||||Exchange Api Error returned by SDS when tenant guid not found while storing tokens.|||||No Remediation Provided
230065|||||Exchange Api request timed out.|||||No Remediation Provided
230066|||||Exchange SDS requests timed out.|||||No Remediation Provided
230067|||||Exchange Auth Api requests timed out.|||||No Remediation Provided
230068|||||Exchange DsApi request timed out.|||||No Remediation Provided
230069|||||The Exchange Service returned a 503 Service Unavailable.|||||No Remediation Provided
230070|||||The Exchange SDS returned a 503 Service Unavailable.|||||No Remediation Provided
230071|||||The Exchange Auth Api returned a 503 Service Unavailable.|||||No Remediation Provided
230072|||||The Exchange DsApi returned a 503 Service Unavailable.|||||No Remediation Provided
230073|||||An Exchange Api error not defined in CCS|||||No Remediation Provided
230074|||||An Exchange SDS Api error indicating invalid serialized access token|||||No Remediation Provided
230075|||||An Exchange SDS Api error indicating mailbox or account cannot be accessed|||||No Remediation Provided
230076|||||An Exchange SDS Api error indicating mailbox cannot be opened.|||||No Remediation Provided
230077|||||Error due to AD Topology Endpoint not found in CCS.|||||No Remediation Provided
230078|||||Error due to Collection not found in CCS.|||||No Remediation Provided
230079|||||Error due to not enough memory in CCS.|||||No Remediation Provided
230080|||||Skip cached credential storage.|||||No Remediation Provided
230081|||||CCS StoreProxy Returned Internal Server Error|||||No Remediation Provided
230082|||||CCS StoreProxy Timed out|||||No Remediation Provided
230083|||||There is insufficient Cafe Routing Info to forward call|||||No Remediation Provided
230084|||||KVCache call failed with RPC error|||||No Remediation Provided
230085|||||KVCacheClient failed to process request|||||No Remediation Provided
230086|||||Call to KVCache timed out|||||No Remediation Provided
230087|||||Call to KVCache timed out|||||No Remediation Provided
230088|||||Key not found in KVCache|||||No Remediation Provided
230089|||||Request is blocked by custom policy evaluation.|||||No Remediation Provided
230090|||||Request is blocked by resiliency defaults disablement.|||||No Remediation Provided
230091|||||Token posted from ESTS can not be validated by CCS|||||No Remediation Provided
230092|||||SDS Error due to corrupt data.|||||No Remediation Provided
230093|||||SDS Error due to invalid decryption key.|||||No Remediation Provided
230094|||||SDS Error due to relocation of tenant to different forest than expected.|||||No Remediation Provided
230095|||||SDS Error due to collection creation progress.|||||No Remediation Provided
230096|||||SDS Error indicating that mailbox was quarantined and unable to be accessed.|||||No Remediation Provided
230097|||||SDS Error due to duplicate secondary key.|||||No Remediation Provided
230098|||||SDS Error indicating that CollectionId could not be found.|||||No Remediation Provided
230099|||||Lookup User Mailbox Id from DsApi failed with Not Found.|||||No Remediation Provided
230100|||||Lookup User Mailbox Id from DsApi timed out.|||||No Remediation Provided
230101|||||Attempt to access data at KVCache failed indicating issue with service.|||||No Remediation Provided
230102|||||Attempt to access data at KVCache failed due to invalid Key or Value data format.|||||No Remediation Provided
240000|||||Limit for BulkAADJ tokens is reached for the tenant.|||||No Remediation Provided
240001|||||User is not authorized to register devices in Azure AD.|||||No Remediation Provided
240002|||||Input id_token cannot be used as 'urn:ietf:params:oauth:grant-type:jwt-bearer' grant.|||||No Remediation Provided
240003|||||Unexpected result from authorize endpoint call.|||||No Remediation Provided
240004|||||Authorization code not received from authorize endpoint call. Error: {errorInfo}|||||No Remediation Provided
250001|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
250002|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
250003|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
250004|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
250005|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
250006|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
293001|||||Invalid target-machine. RDP connection was initiated to a different target-machine.|||||No Remediation Provided
293002|||||Proof-of-possesion validation failed.|||||No Remediation Provided
293003|||||RDP protocol is not supported for the requested client or resource application.|||||No Remediation Provided
293004|||||The target-device identifier in the request {targetDeviceId} was not found in the tenant {tenantId}.|||||No Remediation Provided
392100|||||Unable to locate a user using the provided user information.|||||No Remediation Provided
392101|||||User has not set up remote sign-in with the Authenticator app.|||||No Remediation Provided
392102|||||The session tracking token has expired.|||||No Remediation Provided
392103|||||The user has not yet addressed the request in the Authenticator app. Continue polling.|||||No Remediation Provided
392104|||||The authorization state is in an unexpected state.|||||No Remediation Provided
392105|||||The 'auth_req_id' provided is invalid.|||||No Remediation Provided
392106|||||The 'client_id' provided does not match the client ID provided to the /bc-authorize endpoint.|||||No Remediation Provided
400051|||||Malformed token received from external Identity Provider.|||||No Remediation Provided
400131|||||Claims Provider Federation disabled.|||||No Remediation Provided
500011|||||The resource principal named {name} was not found in the tenant named {tenant}. This can happen if the application has not been installed by the administrator of the tenant or consented to by any user in the tenant. You might have sent your authentication request to the wrong tenant.|||||Developer error - the app requested access to a resource (application) that isn't installed in your tenant. If you expect the app to be installed, you may need to provide administrator permissions to add it. Check with the developers of the resource and application to understand what the right setup for your tenant is.
500012|||||Resource application name '{name}' is not valid.|||||No Remediation Provided
500013|||||Resource identifier is not provided.|||||No Remediation Provided
500014|||||The service principal for resource '{identifier}' is disabled. This indicate that a subscription within the tenant has lapsed, or that the administrator for this tenant has disabled the application, preventing tokens from being issued for it.|||||No Remediation Provided
500015|||||MSA provisioned resources are not supported in the tenant named {tenant}.|||||No Remediation Provided
500021|||||Access to '{tenant}' tenant is denied.|||||Please contact your IT department.
500022|||||Access to '{tenant}' tenant is denied.|||||Please contact your IT department.
500023|||||'{headerFromCredential}' is not the same as '{headerFromRequest}'.|||||A refresh token was received that was controlled under a different tenant restrictions policy than what was received on the request header. To prevent data leakage and bypass of security controls, the request was blocked. Users will need to sign out and sign back in to reset the tenant restrictions policy in their refresh token. This may not be possible if their device enforces one restriction, but the network they're on enforces another.
500024|||||Conflicting tenant restrictions signals received by the server on the login request. The header indicated '{headerFromRequest}' while the application added a claims request for '{headerFromClaims}'. This can indicate conflicting network and device policies, which Azure AD does not support.|||||No Remediation Provided
500025|||||Conflicting tenant restrictions signals received by the server from a claims request. The header from the Id Token '{headerFromIdToken}' is different than the header from the access token '{headerFromAccessToken}'.|||||No Remediation Provided
500031|||||Cannot find signing certificate configured.|||||No Remediation Provided
500032|||||Cannot find signing certificate/private key to issue a certificate.|||||No Remediation Provided
500061|||||Assertion failed signature validation.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
500062|||||Enveloped Signature Transform cannot be the last transform in the chain. The last transform must compute the digest which Enveloped Signature transform is not capable of.|||||No Remediation Provided
500063|||||The '{type}' input type is not supported for the transform.|||||No Remediation Provided
500064|||||The required attribute Algorithm in the element '{name}' is missing.|||||No Remediation Provided
500065|||||Enveloped Signature Transform does not support the algorithm '{algo}'.|||||No Remediation Provided
500066|||||Cannot resolve the '{uri}' URI in the signature to compute the digest.|||||No Remediation Provided
500067|||||Invalid signature. Cannot create a hash or a keyed hash algorithm using the '{method}' signature method.|||||No Remediation Provided
500068|||||Invalid signature. Cannot create a signature deformatter for the '{method}' signature method.|||||No Remediation Provided
500069|||||The element with ID '{id}' was either unsigned or the signature was invalid.|||||No Remediation Provided
500081|||||SAML assertion validation failed: no supported token signature is provided.|||||No Remediation Provided
500082|||||SAML assertion is not present in the token.|||||No Remediation Provided
500083|||||Unable to verify token signature. No trusted realm was found with identifier '{issuer}'.|||||No Remediation Provided
500084|||||Cannot read SecurityToken. Expected element is ({expectedName}, {expectedNamespace}) the actual element is ({localName}, {actualNamespace}).|||||No Remediation Provided
500085|||||SAML Assertion with MajorVersion '{actualMajor}' and MinorVersion '{actualMinor}' is not supported. The supported version is MajorVersion '{major}' and MinorVersion '{minor}'.|||||No Remediation Provided
500086|||||SAML Assertion AssertionId '{id}' is not a valid xsd:ID value.|||||No Remediation Provided
500087|||||SAML Assertion does not have any SAML Statement elements. SAML Assertion must have at least one SAML Statement element.|||||No Remediation Provided
500088|||||SAML Assertion is missing the required '{name}' Attribute.|||||No Remediation Provided
500089|||||SAML 2.0 assertion validation failed: {details}|||||No Remediation Provided
500101|||||Audience URI validation failed. No token audiences were found.|||||No Remediation Provided
500102|||||Audience URI validation failed. No allowed audiences are configured.|||||No Remediation Provided
500103|||||Validation of Audience URI(s) {uri} failed. No match was found with allowed audience(s) {audience}.|||||No Remediation Provided
500111|||||The reply uri specified in the request has an invalid scheme.|||||No Remediation Provided
500112|||||The reply address '{actual}' does not match the reply address '{provided}' provided when requesting Authorization code.|||||No Remediation Provided
500113|||||No reply address is registered for the application{idPhrase}.|||||No Remediation Provided
500114|||||Protocol not specified for reply address validation.|||||No Remediation Provided
500115|||||The reply uri specified in the request is missing or not a valid URL.|||||No Remediation Provided
500116|||||The reply uri specified in the request is not a valid URL. Allowed schemes: '{schemes}'.|||||No Remediation Provided
500117|||||The reply uri specified in the request isn't using a secure scheme.|||||No Remediation Provided
500118|||||The reply uri specified in the request failed validation. The reply uri host must match one of the registered DNS host names '{host}' for site with ID '{id}'.|||||No Remediation Provided
500119|||||Redirect URIs with urn: schemes are prohibited. Use a different scheme, or https://login.microsoftonline.com/common/oauth2/nativeclient|||||No Remediation Provided
500121|||||Authentication failed during strong authentication request.|||||The user didn't complete the MFA prompt. They may have decided not to authenticate, timed out while doing other work, or has an issue with their authentication setup.
500122|||||SWT assertion failed signature validation. Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
500123|||||SWT assertion failed signature validation. Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
500124|||||No device secret is provisioned in the store.|||||No Remediation Provided
500125|||||Invalid device secret is provided.|||||No Remediation Provided
500126|||||External ID token from issuer '{issuer}' failed signature verification. KeyID of token is '{identifier}'.|||||No Remediation Provided
500127|||||No authenticated credentials found in request.|||||No Remediation Provided
500128|||||No session key found.|||||No Remediation Provided
500129|||||No NGC transport key found.|||||No Remediation Provided
500131|||||Assertion audience does not match the Client app presenting the assertion. The audience in the assertion was '{tokenAudience}' and the expected audience is '{expectedAudience}' or one of the Application Uris of this application with App ID '{appId}'({appName}). The downstream client must request a token for the expected audience (the application that made the OBO request) and this application should use that token as the assertion.|||||Assertion is invalid because of various reasons:      - The token issuer doesn't match the api version within its valid time range      - Expired      - Malformed      - Refresh token in the assertion is not a primary refresh token
500132|||||Assertion is malformed and cannot be read.|||||Assertion is invalid because of various reasons:      - The token issuer doesn't match the api version within its valid time range      - Expired      - Malformed      - Refresh token in the assertion is not a primary refresh token
500133|||||Assertion is not within its valid time range. Ensure that the access token is not expired before using it for user assertion, or request a new token. Current time: {curTime}, expiry time of assertion {expTime}.|||||Assertion is invalid because of various reasons:      - The token issuer doesn't match the api version within its valid time range      - Expired      - Malformed      - Refresh token in the assertion is not a primary refresh token
500135|||||Authentication code is missing in the assertion.|||||No Remediation Provided
500136|||||The token issuer doesn't match the api version: A version 2 token can only be used with the v2 endpoint.|||||No Remediation Provided
500137|||||The token issuer doesn't match the api version: A version 1 token cannot be used with the v2 endpoint.|||||No Remediation Provided
500138|||||No Refresh Token claim provided in the assertion.|||||No Remediation Provided
500139|||||Refresh token in the assertion is not a primary refresh token.|||||No Remediation Provided
500171|||||Certificate has been revoked.|||||No Remediation Provided
500172|||||Certificate '{name}' issued by '{issuer}' is not valid. Current time: '{curTime}'. Certificate NotBefore: '{startTime}'. Certificate NotAfter: '{endTime}'.|||||No Remediation Provided
500173|||||Unable to download CRL. Invalid status code {code} from CRL distribution point.|||||No Remediation Provided
500174|||||Unable to construct valid CRL from response.|||||No Remediation Provided
500175|||||Unable to find expected CrlSegment.|||||No Remediation Provided
500176|||||Cannot find issuing certificate in trusted certificates list.|||||No Remediation Provided
500177|||||Delta CRL distribution point is configured without a corresponding CRL distribution point.|||||No Remediation Provided
500178|||||Unable to retrieve valid CRL segments for {type}. Please try again later.|||||No Remediation Provided
500179|||||CRL validation timed out. Please try again later.|||||No Remediation Provided
500180|||||No TLS certificate was provided.|||||No Remediation Provided
500181|||||The TLS certificate provided does not match the certificate in the assertion.|||||No Remediation Provided
500182|||||The issuing certificate authority failed to validate because it is missing the required subject key identifier extension.|||||No Remediation Provided
500183|||||Certificate has been revoked.|||||No Remediation Provided
500200|||||User account '{email}' is a consumer account. Consumer guest accounts cannot sign in using the /common authority of the v1 endpoint - the app must specify which tenant authority to sign the user into.|||||No Remediation Provided
500201|||||We are unable to issue tokens from this API version for a Microsoft account. Please contact the application vendor as they need to use version 2.0 of the protocol to support this.|||||No Remediation Provided
500202|||||User account '{email}' from external identity provider '{idp}' is not supported for API version '{version}'. Microsoft account pass-thru users and guests are not supported by the tenant-independent endpoint.|||||No Remediation Provided
500204|||||Microsoft account '{email}' can’t be used to log in to application {appName}. Please get this user invited to {tenant} directory or sign out and sign in again with a Work or School account.|||||No Remediation Provided
500205|||||A consumer (B2C) account can't be used to log into non consumer applications.|||||No Remediation Provided
500212|||||The user's administrator has set an outbound access policy that does not allow access to the resource tenant.|||||The user's administrator must update their cross-tenant access policy to allow access to the resource tenant.
500213|||||The resource tenant's cross-tenant access policy does not allow this user to access this tenant.|||||This block occurred due to the resource tenant's cross-tenant access policy. Contact that tenant's administrator to ensure that these users are allowed access.
500241|||||The reader is not positioned on an EncryptedKey element that can be read.|||||No Remediation Provided
500242|||||A ReferenceList must contain at least one reference, none were found.|||||No Remediation Provided
500243|||||The reader is not positioned on a KeyReference. XmlEnc specifies that once a KeyReference is found only a KeyReference must exist.|||||No Remediation Provided
500244|||||The reader is not positioned on a DataReference. XmlEnc specifies that once a DataReference is found only a DataReference must exist.|||||No Remediation Provided
500245|||||The key identifier must be set before writing the encrypted data element.|||||No Remediation Provided
500246|||||The reader is not positioned on an EncryptedData element that can be read.|||||No Remediation Provided
500247|||||No CipherData present in EncryptedData element.|||||No Remediation Provided
500248|||||The reader is not positioned on a CipherData element that can be read.|||||No Remediation Provided
500251|||||The issuer name cannot be {name}.|||||No Remediation Provided
500252|||||The issuer name is too long, maximum length is {length}.|||||No Remediation Provided
500271|||||ID Token doesn't contain nonce claim.|||||No Remediation Provided
500272|||||ID Token doesn't contain sub claim.|||||No Remediation Provided
500273|||||Invalid JWT token. Subject identifier mismatch.|||||No Remediation Provided
500274|||||ID Token doesn't contain expected claim: {claim}.|||||No Remediation Provided
500275|||||Duplicated claim found in ID Token claims.|||||No Remediation Provided
500276|||||Token presented by external Identity Provider has failed signature validation.|||||No Remediation Provided
500277|||||External ID Token has unexpected issuer: {issuer}.|||||No Remediation Provided
500278|||||External ID Token issued to unexpected audience: {audience}.|||||No Remediation Provided
500279|||||External ID Token is not within its valid time range. Current time: {curTime}, expiry time of assertion {expTime}.|||||No Remediation Provided
500301|||||The audience {audience} in assertion is not included in forwardableOnBehalfOfOriginsAcceptedAudiencesList for PFT OBO flow.|||||The application owner must update their app registration to indicate that this is an expected audience.
500302|||||The client id {appId} in subassertion (actor token) is not included in forwardableOnBehalfOfOriginsAcceptedPrecedingAppsList for PFT OBO flow.|||||The app owner must update the app registration to include the appid as an expected sender of PFTs.
500303|||||The Audience {audience} in Jwt Subassertion does not match the client.|||||No Remediation Provided
500331|||||An error occurred while attempting to create a certificate from bytes.|||||No Remediation Provided
500341|||||The user account {identifier} has been deleted from the {tenant} directory. To sign into this application, the account must be added to the directory.|||||To sign into this application, the account must be added to the directory. If the user account is deleted from the tenant, see these docs to restore the user: https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-restore
500342|||||User account is not configured for remote NGC.|||||No Remediation Provided
500343|||||Could not create remote sign-in session.|||||No Remediation Provided
500344|||||User Account is not found for Fido Sign in flow.|||||No Remediation Provided
500346|||||E-Mail OTP user cannot sign in with local password.|||||No Remediation Provided
500501|||||Invalid value for '{apiVersion}'.|||||No Remediation Provided
500502|||||Expected exactly one of '{issuer}' and '{authEndpoint}'.|||||No Remediation Provided
500531|||||The sign-in was blocked because it came from an IP blocked for legal reasons.|||||The sign-in was blocked because it came from an IP blocked for legal reasons.
500571|||||The guest user account is disabled.|||||The guest user object in Active Directory backing this account has been disabled. An admin can re-enable this account through Powershell: https://docs.microsoft.com/powershell/module/addsadministration/enable-adaccount?view=win10-ps
500581|||||Rendering JavaScript. Fetching sessions for single-sign-on on V2 with prompt=none requires javascript to verify if any MSA accounts are signed in.|||||Intermediate step during SSO, and does not represent an error
500582|||||Microsoft Account session_id with prompt=none not supported on AAD tenant.|||||No Remediation Provided
500583|||||Storage Access required.|||||No Remediation Provided
500761|||||Due to a configuration change made by your administrator, or because you moved to a new location, the service principal '{servicePrincipal}' must use a certificate for authentication to access '{resource}'.|||||Service principal needs to perform multi-factor authentication by using certificate.
500881|||||Limit on telecom MFA calls reached. Please retry with PhoneAppNotification or try again in a few minutes.|||||No Remediation Provided
500882|||||Limit on telecom MFA calls reached. Please retry with PhoneAppCode or try again in a few minutes.|||||No Remediation Provided
500981|||||Malformed JWT token.|||||No Remediation Provided
500982|||||Unexpected field '{field}' in JWT header.|||||No Remediation Provided
500983|||||JWT header must contain '{field}'.|||||No Remediation Provided
500984|||||Unsupported signing algorithm.|||||No Remediation Provided
500985|||||Unexpected JWT token header type.|||||No Remediation Provided
500986|||||Unexpected field '{field}' in JWT body.|||||No Remediation Provided
500991|||||Unexpected AuthToken audience. Expected token audience: '{expected}', Actual token audience: '{actual}'.|||||No Remediation Provided
500992|||||Public Key Authentication assertion signature is invalid.|||||No Remediation Provided
501051|||||Application '{appId}'({appName}) is not assigned to a role for the application '{resourceId}'({resourceName}).|||||No Remediation Provided
501111|||||JWT tokens are not supported by FederatedAppsClaimsTransformer.|||||No Remediation Provided
501201|||||Unexpected claim(s) in JWT: {claims}.|||||No Remediation Provided
501202|||||Unexpected grant type in JWT.|||||No Remediation Provided
501203|||||Nonce is required in JWT.|||||No Remediation Provided
501204|||||Malformed JWT.|||||No Remediation Provided
501205|||||Unexpected field '{name}' in JWT header.|||||No Remediation Provided
501206|||||JWT header must contain '{name}'.|||||No Remediation Provided
501207|||||Unsupported algorithm.|||||No Remediation Provided
501208|||||Unexpected JWT token type.|||||No Remediation Provided
501209|||||JWT signature is invalid.|||||No Remediation Provided
501210|||||Assertion is null or empty.|||||No Remediation Provided
501241|||||Mandatory Input '{paramName}' missing from transformation id '{transformId}'.|||||No Remediation Provided
501242|||||ClaimsTransformations with ID '{identifier}' contains an unsupported InputClaim.Source '{source}'.|||||No Remediation Provided
501271|||||Broker app needs to be installed for device authentication to succeed.|||||No Remediation Provided
501291|||||Client app is a Mam app, device is not registered and request is sent using a broker. Work place join needs to be done to register the device before the app can be accessed.|||||No Remediation Provided
501292|||||Client application cannot satisfy app protection requirement. If it's a first party app, then it's not whitelisted to be used with app protection policies, otherwise, the app has not advertised as app-compliant capable, or the authentication library used does not support app protection policies.|||||No Remediation Provided
501311|||||Browser not supported.|||||No Remediation Provided
501312|||||Device used during the authentication is not registered for the account.|||||No Remediation Provided
501313|||||Your device is required to be managed to access this resource.|||||No Remediation Provided
501314|||||Silent interrupt required to recognize browser capabilities. Used to differentiate between Safari running in iPadOS or Mac.|||||No action required, this is expected as part of determining device identities due to application or conditional access requirements.
501431|||||Session is invalid due to different resource.|||||No Remediation Provided
501461|||||AcceptMappedClaims is only supported for a token audience matching the application GUID or an audience within the tenant's verified domains. Either change the resource identifier, or use an application-specific signing key.|||||No Remediation Provided
501471|||||Missing code_challenge parameter.|||||No Remediation Provided
501481|||||The Code_Verifier does not match the code_challenge supplied in the authorization request.|||||No Remediation Provided
501482|||||The Code_Verifier length is less than invalid.|||||No Remediation Provided
501491|||||Invalid size of Code_Challenge parameter.|||||No Remediation Provided
501571|||||User routing cookie missing.|||||No Remediation Provided
501591|||||Missing claim requested to external provider.|||||No Remediation Provided
501592|||||idToken doesn't contain expected claim: '{claim}'.|||||No Remediation Provided
501593|||||Value of {type} claim in idToken: {value} doesn't match expected values: {expected}|||||No Remediation Provided
501621|||||Regular expression replacement for claims transformation has timed out. This indicates a too complex regular expression may have been configured for this application. A retry of the request may succeed. Otherwise, please contact your admin to fix the configuration.|||||No Remediation Provided
501631|||||Regular expression replacement for claims transformation results in too many replacements in the input sourceClaim. Please contact your admin to fix the configuration.|||||No Remediation Provided
501632|||||Regular expression replacement for claims transformation has too many substitution parameters in the replacement input parameter. Please contact your admin to fix the configuration.|||||No Remediation Provided
501661|||||Request to External OIDC endpoint failed.|||||No Remediation Provided
501791|||||Client_info is only supported for MSAL/ADAL, please ensure that MSAL/ADAL custom headers are being sent.|||||No Remediation Provided
501811|||||No otp for the given tenant/user.|||||No Remediation Provided
501831|||||Cannot generate more one time passcode due to cache exception.|||||No Remediation Provided
501941|||||Resource '{resourceId}'({resourceName}) is not configured as a multi-tenant application. Usage of the /common endpoint is not supported for such applications created after '{time}'. Use a tenant-specific endpoint or configure the application to be multi-tenant.|||||No Remediation Provided
510001|||||Cannot meet the requirements stated in the request.|||||No Remediation Provided
530001|||||Browser not supported.|||||The user is using a browser that does not support device identification so the device state is unknown. Access to the resource requires a compliant device. To see a list of browsers that support device identification, see https://docs.microsoft.com/azure/active-directory/conditional-access/technical-reference#supported-browsers
530002|||||Your device is required to be compliant to access this resource.|||||The requested resource can only be accessed using a compliant device. The user is using a device already managed by a Mobile-Device-Management (MDM) agent like Intune, but it's not being reported as compliant yet. The user could check with your MDM provider on how to become compliant. More details available at https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-device-remediation
530003|||||Your device is required to be managed to access this resource.|||||The requested resource can only be accessed using a compliant device. The user is either using a device not managed by a Mobile-Device-Management (MDM) agent like Intune, or it's using an application that doesn't support device authentication. The user could enroll their devices with an approved MDM provider, or use a different app to sign in, or find the app vendor and ask them to update their app. More details available at https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-device-remediation
530004|||||AcceptCompliantDevice setting isn't configured for this organization. The admin needs to configure this setting to allow external users access to protected resources.|||||AcceptCompliantDevice setting isn't configured for this organization. The admin needs to configure this setting to allow external users access to protected resources.
530011|||||Browser not supported.|||||The user is using a browser that does not support device identification so the device state is unknown. Access to the resource requires a Hybrid Azure AD joined device. To see a list of browsers that support device identification, see https://docs.microsoft.com/azure/active-directory/conditional-access/technical-reference#supported-browsers
530021|||||Application does not meet the conditional access approved app requirements.|||||Application used is not an approved application for conditional access. User needs to use one of the apps from the list of approved applications to use in order to get access. To see a list of approved apps, see https://docs.microsoft.com/azure/active-directory/conditional-access/technical-reference#approved-client-app-requirement
530022|||||Browser not supported.|||||Application used is not an approved application for conditional access. User needs to use one of the apps from the list of approved applications to use in order to get access. To see a list of approved apps, see https://docs.microsoft.com/azure/active-directory/conditional-access/technical-reference#approved-client-app-requirement
530031|||||Access policy does not allow token issuance.|||||A classic conditional access policy, or a policy from Azure AD Identity Protection, prevented this resource from being accessed. View the Conditional Access information for this request in the sign-in logs for more details about the policy applied here.
530032|||||User blocked due to risk on home tenant.|||||If this user is risky in your tenant, learn more here: aka.ms/unblockrisk. If this is a guest user, learn more here: aka.ms/riskyguestuser.
530033|||||Remote device flow blocked due to device based conditional access.|||||This request is authorizing a remote device, and there is a conditional access policy that requires device authentication. The request is blocked because we cannot assert the properties of the remote device. View the Conditional Access information for this request in the sign-in logs for more details about the policy applied here.
530034|||||A delegated administrator was blocked from accessing the tenant due to account risk.|||||Azure AD blocked delegated administrator access due to account risk in their home tenant.
530081|||||Managed browser or Microsoft Edge is required for device registration to succeed.|||||No Remediation Provided
530082|||||Workplace join is required to register the device.|||||User is required to add their work account to the device. To learn more, see https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-device-remediation
600071|||||An error occurred while attempting to create a certificate from bytes.|||||No Remediation Provided
650011|||||The user or administrator has not consented to use the application with ID '{identifier}'{namePhrase}. Send an interactive authorization request for this user and resource. Alternatively, the Application URI {uri} for the App:'{appId}'{name} in the tenant '{tenant}' might be in conflict with the Application URI for the multitenant app '{conflict}'. Update the registered Application URI to something else to avoid the conflict.|||||No Remediation Provided
650041|||||User terminated the request.|||||No Remediation Provided
650051|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
650052|||||The app needs access to a service ('{name}') that your organization '{organization}' has not subscribed to or enabled. Contact your IT Admin to review the configuration of your service subscriptions.|||||Contact your IT Admin to review the configuration of your service subscriptions.
650053|||||The application '{name}' asked for scope '{scope}' that doesn't exist on the resource '{resource}'. Contact the app vendor.|||||No Remediation Provided
650054|||||The application '{name}' asked for permissions to access a resource that has been removed or is no longer available. Contact the app vendor.|||||No Remediation Provided
650055|||||The application '{name}' required resource access list does not contain applications discoverable by '{resource}'.|||||No Remediation Provided
650056|||||Misconfigured application. This could be due to one of the following: the client has not listed any permissions for '{name}' in the requested permissions in the client's application registration. Or, the admin has not consented in the tenant. Or, check the application identifier in the request to ensure it matches the configured client application identifier. Or, check the certificate in the request to ensure it's valid. Please contact your admin to fix the configuration or consent on behalf of the tenant. Client app ID: {id}.|||||Please contact your admin to fix the configuration or consent on behalf of the tenant.
650057|||||Invalid resource. The client has requested access to a resource which is not listed in the requested permissions in the client's application registration. Client app ID: {appId}({appName}). Resource value from request: {resource}. Resource app ID: {resourceAppId}. List of valid resources from app registration: {regList}.|||||No Remediation Provided
650058|||||The app needs access to a service that your organization has not subscribed to or enabled. Contact your IT Admin to review the configuration of your service subscriptions.|||||No Remediation Provided
650061|||||Requested permission ID: '{permissionId}' in the resource access for client '{clientId}' has an invalid type. Please followup with the owner of Resource '{resourceId}' to fix the resource entitlement configuration.|||||No Remediation Provided
699981|||||OfficeS2S delegation service endpoints are not supported for calling application '{appId}'({appName}).|||||No Remediation Provided
700001|||||Application: {samlAudience} needs to opt-in for 'aio' optional claim for On Behalf Of flow to work with SAML tokens issued to this application|||||Invalid grant due to the following reasons:      - Requested SAML 2.0 assertion has invalid Subject Confirmation Method      - Application On-Behalf-Of flow is not supported on V2      - Primary refresh token is not signed with session key      - Invalid external refresh token      - The access grant was obtained for a different tenant
700002|||||SAML 1.1 Bearer assertion must be a valid Base64 encoded value.|||||No Remediation Provided
700003|||||Device object was not found in the tenant '{tenantName}' directory.|||||Invalid grant due to the following reasons:      - Requested SAML 2.0 assertion has invalid Subject Confirmation Method      - Application On-Behalf-Of flow is not supported on V2      - Primary refresh token is not signed with session key      - Invalid external refresh token      - The access grant was obtained for a different tenant
700004|||||onpremobjectguid '{objGuid}' attribute in the presented grant is malformed.|||||Invalid grant due to the following reasons:      - Requested SAML 2.0 assertion has invalid Subject Confirmation Method      - Application On-Behalf-Of flow is not supported on V2      - Primary refresh token is not signed with session key      - Invalid external refresh token      - The access grant was obtained for a different tenant
700005|||||Provided Authorization Code is intended to use against other tenant, thus rejected.|||||OAuth2 Authorization Code must be redeemed against same tenant it was acquired for.
700006|||||The Audience: {audience} of the token is NOT an absolute Uri|||||No Remediation Provided
700007|||||The grant was issued for a different client id.|||||No Remediation Provided
700008|||||Social IDP users are not expected to have home tenant.|||||No Remediation Provided
700009|||||Reply address must be provided when presenting an authorization code requested with an explicit reply address.|||||No Remediation Provided
700011|||||Application with identifier {appIdentifier} was not found in the directory.|||||A client application requested a token from your tenant, but the client app doesn't exist in your tenant, so the call failed.
700012|||||Missing Authorization header with bearer token. Client was not authenticated.|||||No Remediation Provided
700013|||||Client is not authorized to request managed browser purpose token.|||||No Remediation Provided
700014|||||Mobile Edge app needs to provide an enrollment id in order to acquire a purpose token that can satisfy the compliant app requirement.|||||No Remediation Provided
700016|||||Application with identifier '{appIdentifier}' was not found in the directory '{tenantName}'. This can happen if the application has not been installed by the administrator of the tenant or consented to by any user in the tenant. You may have sent your authentication request to the wrong tenant.|||||The application named X was not found in the tenant named Y. This can happen if the application with identifier X has not been installed by the administrator of the tenant or consented to by any user in the tenant. You might have misconfigured the Identifier value for the application or sent your authentication request to the wrong tenant
700017|||||{resourceConstant} '{resourceIdentifier}' is not supported as resource.|||||No Remediation Provided
700018|||||{resourceConstant} '{resourceIdentifier}' is not supported as resource.|||||No Remediation Provided
700019|||||Application ID {identifier} cannot be used or is not authorized.|||||No Remediation Provided
700020|||||Application ID {identifier} is a reserverd identifier and should be removed on the application: {applicationId}.|||||No Remediation Provided
700021|||||Client assertion application identifier doesn't match 'client_id' parameter. Review the documentation at https://docs.microsoft.com/azure/active-directory/develop/active-directory-certificate-credentials .|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
700022|||||No Subject claim provided in the assertion. Review the documentation at https://docs.microsoft.com/azure/active-directory/develop/active-directory-certificate-credentials .|||||No Remediation Provided
700023|||||Client assertion audience claim does not match Realm issuer. Review the documentation at https://docs.microsoft.com/azure/active-directory/develop/active-directory-certificate-credentials .|||||No Remediation Provided
700024|||||Client assertion is not within its valid time range. Current time: {curTime}, expiry time of assertion {expTime}. Review the documentation at https://docs.microsoft.com/azure/active-directory/develop/active-directory-certificate-credentials .|||||The app used an expired client assertion. It needs to be updated in the Azure Portal to generate a new client secret or certificate.
700025|||||Client is public so neither 'client_assertion' nor 'client_secret' should be presented.|||||No Remediation Provided
700026|||||Client application has no configured keys.|||||No Remediation Provided
700027|||||Client assertion failed signature validation.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
700028|||||Certificate with thumbprint {thumbprint} is not authorized.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
700029|||||Invalid signing certificate.|||||No Remediation Provided
700030|||||Invalid certificate - subject name in certificate is not authorized. SubjectNames/SubjectAlternativeNames (up to 10) in token certificate are: {certificateSubjects}.|||||No Remediation Provided
700031|||||Invalid certificate - SubjectName or SubjectAlternativeName is missing|||||No Remediation Provided
700032|||||Invalid certificate - Trusted Certificate Subjects for application are missing|||||No Remediation Provided
700033|||||Client assertion should declare both custom_claims and xms_actor_token claims when overriding managed resource ID.|||||No Remediation Provided
700034|||||Client assertion contains an invalid xms_actor_token claim.|||||No Remediation Provided
700035|||||Client assertion contains custom_claims in the incorrect format.|||||No Remediation Provided
700036|||||Client is not authorized to override managed identity claim in the token.|||||No Remediation Provided
700037|||||Client assertion must declare x5c header when overriding managed resource ID.|||||No Remediation Provided
700038|||||00000000-0000-0000-0000-000000000000 is not a valid application identifier.|||||No Remediation Provided
700039|||||00000000-0000-0000-0000-000000000000 is not a valid resource identifier|||||No Remediation Provided
700040|||||Managed Resource ID '{inputManagedResourceId}' is not a valid resource identifier.|||||No Remediation Provided
700041|||||Post-logout redirect uri is not in approved list. Requested post-logout url: {url}.|||||No Remediation Provided
700042|||||The reply address does not match the reply addresses configured for the application.|||||No Remediation Provided
700043|||||The redirect address '{address}' does not match the redirect addresses configured for service identity '{serviceId}'.|||||No Remediation Provided
700044|||||The redirect address '{address}' corresponding to this authorization code does not match the redirect address '{requestAddress}' specified in the request.|||||No Remediation Provided
700045|||||Redirect address '{address}' specified by the client does not match any configured addresses '{configuredAddress}' or any addresses on the OIDC approve list.|||||No Remediation Provided
700046|||||Invalid Reply Address. Reply Address must have scheme brk-{brkApplicationId}:// and be of Single Page Application type.|||||No Remediation Provided
700047|||||Invalid Reply Address. Broker must use Single-Page Application Reply Address.|||||No Remediation Provided
700048|||||Client assertion contains an invalid xms_actor_token claim. The audience of the claim is not correctly set.|||||No Remediation Provided
700049|||||Claim override is only allowed for User Assigned Managed Service Identities. Make sure the caller app is a Managed Identity, and the override is being done for a User Assigned identity.|||||No Remediation Provided
700050|||||Actor token is not within its valid time range. Current time: {curTime}, expiry time of actor token {expTime}.|||||No Remediation Provided
700051|||||response_type 'token' is not enabled for the application.|||||The application requested an unsupported response type due to the following reasons: response_type 'token' is not enabled for the application. Application owner should go to the Azure portal or call MS Graph to enable the implicit access token grant.
700052|||||The token request contains one or more unsupported response token type(s): '{ResType}'.|||||No Remediation Provided
700053|||||response_type 'id_token' requires the 'openid' scope.|||||No Remediation Provided
700054|||||response_type 'id_token' is not enabled for the application.|||||The application requested an unsupported response type due to the following reasons: response_type 'id_token' is not enabled for the application. Application owner should go to the Azure portal or call MS Graph to enable the implicit id token grant.
700055|||||Redirection to B2C first party app is permitted only to the /authresp endpoint.|||||No Remediation Provided
700081|||||The refresh token has expired due to maximum lifetime. The token was issued on {issueDate} and the maximum allowed lifetime for this application is {time}.|||||Expected part of the token lifecycle - the user went an extended period of time without using the application, so the token was expired when the app attempted to refresh it.
700082|||||The refresh token has expired due to inactivity. The token was issued on {issueDate} and was inactive for {time}.|||||Expected part of the token lifecycle - the user went an extended period of time without using the application, so the token was expired when the app attempted to refresh it.
700083|||||The primary refresh token has expired due to maximum lifetime. The token was issued on {issueDate} and the maximum allowed lifetime for this application is {time}.|||||No Remediation Provided
700084|||||The refresh token was issued to a single page app (SPA), and therefore has a fixed, limited lifetime of {time}, which cannot be extended. It is now expired and a new sign in request must be sent by the SPA to the sign in page. The token was issued on {issueDate}.|||||Single page apps receive fixed, shorter-lived refresh tokens, and are expected to encounter this error on a regular basis. Apps must handle this error by redirecting the user to the sign in page for a refreshed sign in session.
700171|||||End-user declined to authorize the request.|||||No Remediation Provided
700172|||||Authentication loop detected: please check application's configuration.|||||No Remediation Provided
700221|||||Issuer from the provided JWT '{jwtIssuer}' does not match the issuer published in the OIDC discovery metadata ('{metadataIssuer}') registered for this federated credential.|||||Ensure that the OpenID Connect metadata issuer matches issuer presented in the JWT.
700222|||||AAD-issued tokens may not be used for federated identity flows.|||||The federated identity credentials flow does not support tokens issued by Azure AD at this time.
700311|||||Remote auth session in cache is invalid.|||||No Remediation Provided
701011|||||Unable to save code into cache.|||||No Remediation Provided
701012|||||Unable to create remote auth session in device flow cache.|||||No Remediation Provided
701013|||||Unable to create remote auth session for user in activity store.|||||No Remediation Provided
701014|||||Cannot generate more one time passcodes.|||||No Remediation Provided
750011|||||Cannot validate RelayState. Check that RequestDataStorage is properly configured.|||||No Remediation Provided
750012|||||RelayState of response does not match with RelayState from request. Expected '{expected}' actual '{actual}'.|||||No Remediation Provided
750013|||||Cannot serialize SAML message container with no endpoint specified.|||||No Remediation Provided
750014|||||Could not find a SAMLRequest or SAMLResponse in the message. Check if the request contains a valid Uri or Form Post that contains protocol parameters for SAML HTTP bindings.|||||No Remediation Provided
750015|||||Wrong SAML message type '{wrongType}', expected '{expectedType}'.|||||No Remediation Provided
750016|||||Parameter '{name}' must be unique in HTTP SAML message.|||||No Remediation Provided
750017|||||The specified encoding method '{actual}' is not supported. Use '{expected}' encoding instead.|||||No Remediation Provided
750018|||||The signature algorithm '{algo}' is not valid.|||||No Remediation Provided
750019|||||The query string hash could not be computed for signature generation/validation. Neither SAMLRequest nor SAMLResponse was present in the message.|||||No Remediation Provided
750031|||||The requested protocol binding '{reqBinding}' is not supported. The supported bindings are GET (HTTP Redirect) and POST.|||||Use either HTTP Redirect binding or HTTP Post binding to send the SAML AuthnRequest or LogoutRequest.
750032|||||SAML protocol response cannot be sent via bindings other than HTTP POST. Requested binding: {reqBinding}|||||In the SAML AuthnRequest, specify POST as the ProtocolBinding.
750051|||||Must specify HTTP POST operation for SAML POST binding.|||||No Remediation Provided
750052|||||SAMLRequest or SAMLResponse must be present in body of HTTP request for SAML POST binding.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
750053|||||Must specify HTTP GET operation for SAML HTTP Redirect binding.|||||No Remediation Provided
750054|||||SAMLRequest or SAMLResponse must be present as query string parameters in HTTP request for SAML Redirect binding.|||||Azure AD wasn't able to identify the SAML request within the URL parameters in the HTTP request. This can happen if the application is not using HTTP Redirect Binding for sending the SAML request to Azure AD.    The application needs to send the SAML request encoded into the location header using HTTP Redirect Binding. For more information about how to implement it, read the section HTTP Redirect Binding in the SAML protocol specification document.[https://docs.oasis-open.org/security/saml/v2.0/saml-bindings-2.0-os.pdf]
750055|||||SAML message was not properly DEFLATE-encoded.|||||No Remediation Provided
750056|||||SAML message was not properly base64-encoded.|||||No Remediation Provided
750057|||||SAML message was not properly UTF8-encoded.|||||No Remediation Provided
750058|||||XML attribute '{attributeName}' in the SAML message must be a boolean.|||||No Remediation Provided
750059|||||XML attribute '{attributeName}' in the SAML message must be an integer.|||||No Remediation Provided
750161|||||Allowed SAML authentication request's NameIDPolicy formats are: {format}.|||||No Remediation Provided
800111|||||Encryption keys retrieved is null or empty.|||||No Remediation Provided
800181|||||Invalid configuration detected causing multiple redirects.|||||No Remediation Provided
800182|||||Failed to determine on-premises password validation endpoints for request.|||||No Remediation Provided
800183|||||The on-premises region configuration is invalid for the tenant.|||||No Remediation Provided
800184|||||The on-premises password validation request was throttled.|||||No Remediation Provided
900000|||||Environment error.|||||No Remediation Provided
900001|||||The browser is having problems downloading resources from the CDN (Content Delivery Network). Please check with your organization's system administrators to ensure that they have not blocked the resource url endpoint and that the files exists and are accessible.|||||No Remediation Provided
900021|||||Requested tenant identifier '{tenant_id}' is not valid. Tenant identifiers may not be an empty GUID.|||||No Remediation Provided
900022|||||Provided tenant identifier is empty.|||||No Remediation Provided
900023|||||Specified tenant identifier '{tenant_id}' is neither a valid DNS name, nor a valid external domain.|||||Application error - the login request was malformed and could not be matched with an existing authentication endpoint or instance.
900041|||||The request contains {num} tokens separated by '{splitter}' instead of a single key value pair.|||||No Remediation Provided
900042|||||Authorization header is missing or malformed.|||||No Remediation Provided
900043|||||Bad request. Passed context cannot be parsed.|||||No Remediation Provided
900044|||||Only version {num} of PKeyAuth is supported.|||||No Remediation Provided
900045|||||Missing PKeyAuth Authorization header.|||||No Remediation Provided
900046|||||Unprotected credential key parsing failed: invalid JWE format.|||||No Remediation Provided
900047|||||Malformed PKeyAuth header.|||||No Remediation Provided
900048|||||Request too large.|||||No Remediation Provided
900049|||||Malformed request.|||||No Remediation Provided
900051|||||Unable to complete request. The request was invalid since sid and domain_hint cannot be used together.|||||No Remediation Provided
900052|||||Request body may not be encoded in UTF-16.|||||No Remediation Provided
900053|||||Request body must not begin with UTF-8 BOM.|||||No Remediation Provided
900054|||||Specified Broker Client ID does not match ID in provided grant.|||||No Remediation Provided
900055|||||Broker Client ID expected in GUID format.|||||No Remediation Provided
900056|||||redirect_uri is a required parameter for brokered authentication.|||||No Remediation Provided
900057|||||Unexpected 'brk_client_id' or 'brk_redirect_uri' parameters when obtaining or redeeming grants for broker application.|||||No Remediation Provided
900058|||||Server cannot satisfy the request. MSIs do not support user-based flows, only the client credentials flow. Use a multi-tenant application and secret or certificate in order to sign in users at this time.|||||This is a platform error - a certificate was used by an Azure component in a way that Azure AD does not support.
900059|||||You must request the hybrid SPA auth code on your confidential client back-end, while redeeming the original auth code requested for a web type redirect URI. Auth codes obtained for the Pairwise broker flow cannot be redeemed for a hybrid SPA authorization code.|||||No Remediation Provided
900101|||||Unable to create default encryption algorithm: {algoName}.|||||No Remediation Provided
900102|||||'{algoName}' algorithm not supported.|||||No Remediation Provided
900103|||||The digest algorithm '{algoName}' is not supported.|||||No Remediation Provided
900104|||||Lifetime must be greater than or equal to TimeSpan.Zero.|||||No Remediation Provided
900105|||||The token signing digest algorithm '{algoName}' requested by the application is not supported for this type of token. This indicates the application is misconfigured.|||||No Remediation Provided
900106|||||The '{name}' input type is not supported for the transform.|||||No Remediation Provided
900107|||||The exclusive canonicalization transform does not support the '{algoName}' algorithm.|||||No Remediation Provided
900108|||||{name} implementation not supported.|||||No Remediation Provided
900109|||||Cannot create a signature deformatter for the requested algorithm.|||||No Remediation Provided
900143|||||'{name}' is required for the '{type}' grant type.|||||No Remediation Provided
900144|||||The request body must contain the following parameter: '{name}'.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
900161|||||Invalid access token. Required tenant ID claim is missing.|||||No Remediation Provided
900191|||||The 'client_credentials' grant type requires a tenant to be specified.|||||No Remediation Provided
900192|||||Unable to determine the tenant identifier from the request. Client ID '{id}' does not specify a tenant realm.|||||No Remediation Provided
900193|||||The 'urn:microsoft.com:grant-type:device:credentials' grant type requires a tenant to be specified.|||||No Remediation Provided
900194|||||Unable to determine the tenant identifier from the request. Token audience '{audienceSpn}' does not specify a tenant realm.|||||No Remediation Provided
900195|||||Unable to determine the tenant identifier from the request. Token audience '{audienceSpn}' is not valid.|||||No Remediation Provided
900231|||||Unable to authenticate the user.|||||No Remediation Provided
900232|||||Request specified an authentication method '{authRequirementInRequest}' that is not in the allowed list of authentication methods supported by application '{appName}'.|||||No Remediation Provided
900233|||||The SAML AuthnRequest or LogoutRequest must specify an Issuer.|||||No Remediation Provided
900234|||||The SAML AuthnRequest or LogoutRequest must specify the default Issuer Format '{expectedIssuerFormat}'. Received Issuer Format: '{receivedIssuerFormat}'.|||||No Remediation Provided
900235|||||SAML authentication request's RequestedAuthenticationContext Comparison value must be 'exact'. Received value: '{samlComparison}'.|||||No Remediation Provided
900236|||||The SAML authentication request property '{propertyName}' is not supported and must not be set.|||||No Remediation Provided
900237|||||AssertionConsumerServiceIndex cannot be set when ProtocolBinding or AssertionConsumerServiceUrl are set.|||||No Remediation Provided
900238|||||AssertionConsumerServiceUrl cannot be set when AssertionConsumerServiceIndex is set.|||||No Remediation Provided
900239|||||ProtocolBinding cannot be set when AssertionConsumerServiceIndex is set.|||||No Remediation Provided
900281|||||Principal name format is invalid. Realm component of the name cannot be empty.|||||No Remediation Provided
900282|||||Principal name format is invalid for name '{name}'. Expected primary[@realm].|||||No Remediation Provided
900381|||||Request redirection failed. Tenant '{tenant_name}' specified belongs to the National Cloud '{tenant_cloud}', but Current Cloud Instance '{current_cloud}' does not federate with '{tenant_cloud}'.|||||No Remediation Provided
900382|||||Confidential Client is not supported in Cross Cloud request.|||||No Remediation Provided
900383|||||Internal error has occurred during a redirect. Please login directly to your National Cloud dedicated portal.|||||No Remediation Provided
900384|||||JWT token failed signature validation. Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
900385|||||JWT token must be signed.|||||No Remediation Provided
900386|||||WsFederation metadata request for Tenant '{tenantName}' must be made on Cloud '{cloud}'.|||||No Remediation Provided
900387|||||Unsupported version '{apiVersion}' specified in discovery request|||||No Remediation Provided
900388|||||Http request to national cloud failed with time out error|||||No Remediation Provided
900410|||||Non-retryable error has occurred.|||||No Remediation Provided
900421|||||Actual message content is runtime specific. Please see returned exception message for details.|||||No Remediation Provided
900431|||||National Cloud Federation or Proxy Request feature is disabled.|||||No Remediation Provided
900432|||||Confidential Client is not supported in Cross Cloud request.|||||No Remediation Provided
900433|||||Invalid National Cloud Token.|||||No Remediation Provided
900434|||||National Cloud request processing failed: {details}|||||No Remediation Provided
900435|||||Received Empty OAuth response from National Cloud: {name}.|||||No Remediation Provided
900436|||||Invalid request method {name} received.|||||No Remediation Provided
900437|||||Auth Code value is missing.|||||No Remediation Provided
900438|||||Refresh token value is missing.|||||No Remediation Provided
900439|||||Confidential Client requests are not supported on the public endpoint (login.microsoftonline.com) for tenants in the Azure Government cloud. Send your login requests to https://login.microsoftonline.us instead. Please see https://devblogs.microsoft.com/azuregov/azure-government-aad-authority-endpoint-update/ for more details|||||Starting May 5th 2020, Azure AD began enforcing the change in login endpoints for Azure Government that was announced April 3rd, 2018. The app must be updated to sign in users to the US Government cloud instead of the public cloud.
900440|||||Requests to tenants hosted in the public cloud are not supported on USGov endpoints. This user must sign into https://login.microsoftonline.com instead of https://login.microsoftonline.us. The application must send the user to the right login endpoint, usually by hosting two versions of the site (e.g. portal.azure.us and portal.azure.com)|||||Starting May 5th 2020, Azure AD began enforcing the change in login endpoints for Azure Government that was announced April 3rd, 2018. Users from the public cloud cannot be signed into the US Government cloud. This is by design - those users must sign into the public cloud instead.
900441|||||Requests to applications hosted in the public cloud are not supported for USGov tenants.|||||No Remediation Provided
900442|||||Requests from the public cloud user for USGov resource, and requests from USGov user for public cloud resource are not supported.|||||No Remediation Provided
900443|||||The requested endpoint {endpoint} is not supported on air-gapped cloud using public hostname. Please use hostname {hostname} instead.|||||No Remediation Provided
900491|||||Service principal '{identifier}' not found.|||||No Remediation Provided
900501|||||Json format queue length exceeds the threshold.|||||No Remediation Provided
900521|||||Static Content Manager: Has not been initialized.|||||No Remediation Provided
900522|||||You can't have an alias map to another alias.|||||No Remediation Provided
900523|||||Passed in value is not an enum - {type}.|||||No Remediation Provided
900524|||||No CDN roots configured.|||||No Remediation Provided
900525|||||Service configuration error has occurred: unable to obtain SAS certificate.|||||No Remediation Provided
900561|||||The endpoint only accepts {valid_verbs} requests. Received a {invalid_verb} request.|||||This can be due to developer error, or due to users pressing the back button in their browser, triggering a bad request. It can be ignored.
900562|||||Unsupported GUID resource format specified, only supported GUID formats types are '00000000000000000000000000000000' and '00000000-0000-0000-0000-000000000000'.|||||No Remediation Provided
900610|||||Non-retryable error has occurred during request to external OIDC endpoint.|||||No Remediation Provided
900611|||||Failed to parse provider metadata.|||||No Remediation Provided
900612|||||Failed to parse provider signing keys.|||||No Remediation Provided
900620|||||Token Remint endpoint generic error.|||||No Remediation Provided
900621|||||Token Remint endpoint missing signing credentials to sign tokens.|||||No Remediation Provided
900622|||||Token Remint endpoint cannot use the asserting token because of allow remint claim is not preset.|||||No Remediation Provided
900623|||||Token Remint endpoint cannot use the token because its issued at value is not valid.|||||No Remediation Provided
900624|||||Token Remint endpoint cannot use the token because asserting token signature is invalid.|||||No Remediation Provided
900625|||||Token Remint endpoint cannot use the token because asserting token type is not eligible for remint.|||||No Remediation Provided
900626|||||Token Remint endpoint cannot use the token because asserting token type has expired.|||||No Remediation Provided
900627|||||Token Remint endpoint cannot parse the request.|||||No Remediation Provided
900700|||||Security Event Token signing endpoint generic error.|||||No Remediation Provided
900701|||||Security Event Token signing endpoint received invalid request.|||||No Remediation Provided
900702|||||Security Event Token signing endpoint received SET which could not be parsed to a JWT|||||No Remediation Provided
900703|||||Security Event Token signing endpoint received SET with null claims.|||||No Remediation Provided
900704|||||Security Event Token signing endpoint received SET with invalid issuer. Issuer: {invalidIssuer}|||||No Remediation Provided
900705|||||Security Event Token signing endpoint received SET with invalid IssuedAt value. IssuedAt: {invalidIssuedAt}|||||No Remediation Provided
900706|||||Security Event Token signing endpoint received SET with unexpected claims. Unexpected claims: {unexpectedClaims}|||||No Remediation Provided
900811|||||Unsupported web method is used.|||||No Remediation Provided
900812|||||Unsupported WS-Federation message of type '{name}'.|||||No Remediation Provided
900821|||||Unsupported WS-Federation message of type '{type}'.|||||No Remediation Provided
900822|||||Requested '{type}' value is unsupported.|||||No Remediation Provided
900851|||||Unable to issue a token since user account is not provisioned yet.|||||No Remediation Provided
900941|||||Administrator consent is required. App is considered risky.|||||No Remediation Provided
900942|||||Admin consent is required in order to allow token to be issued for clients to access resource.|||||No Remediation Provided
900971|||||No reply address provided.|||||No Remediation Provided
900981|||||An admin consent request was received for a risky app.|||||No Remediation Provided
901001|||||Invalid request. The {name} request parameter value '{value}' is invalid.|||||No Remediation Provided
901002|||||The '{name}' request parameter is not supported.|||||No Remediation Provided
901003|||||Invalid request. The request contains too many encoded parameters.|||||No Remediation Provided
901004|||||Expected parameter {name} not found.|||||No Remediation Provided
901005|||||'{value}' is not a supported value for {name} parameter. Expected values are '{expectedVal}'.|||||No Remediation Provided
901006|||||The following extra parameters were found in the request and should be removed from subsequent requests: [{names}]|||||No Remediation Provided
901121|||||No certificates found for {application}.|||||No Remediation Provided
901122|||||Application '{application}' has no encryption certificate configured.|||||No Remediation Provided
901123|||||Misconfigured application '{application}'.|||||No Remediation Provided
901124|||||Application '{application}' does not exist.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
901125|||||Application does not exist.|||||No Remediation Provided
901141|||||Bad request - expiration time is in the past.|||||No Remediation Provided
901142|||||Bad request - requested token lifetime exceeds allowed limit.|||||No Remediation Provided
901151|||||Fallback_domain parameter is not allowed together with domain_hint.|||||No Remediation Provided
901171|||||Unable to sign in. Please sign out and sign in again with your identity provider.|||||No Remediation Provided
901181|||||Mapped Microsoft Graph permissions are not supported for application permissions.|||||No Remediation Provided
901182|||||Application '{applicationId}' must be preauthorized by Microsoft Graph for scopes '{scope}'.|||||No Remediation Provided
901183|||||The service principal with an identifier of {spIdentifier} does not exist in the directory.|||||No Remediation Provided
901201|||||This request is invalid, cannot be processed.|||||No Remediation Provided
901202|||||Device identifier in the device signature is different from the device assigned to the resource account.|||||No Remediation Provided
1000000|||||The Bind API requires the Azure AD user to also authenticate with an external IDP, which hasn't happened yet. Redirecting to external IDP.|||||Expected error when the user attempts to connect a LinkedIn account to their AAD account.
1000001|||||The specified bind provider '{provider}' is not supported.|||||No Remediation Provided
1000002|||||The bind completed successfully, but the user must be informed.|||||This is not an error scenario, but is handled like one by Azure AD to handle certain authentication flows.  This is not an indication that anything went wrong.
1000003|||||MSA redirected to ESTS for an AAD user to login.|||||No Remediation Provided
1000004|||||Values '{notAllowedValues}' are not valid for claim request '{requestedClaim}'.|||||No Remediation Provided
1000005|||||Invalid definition for external identity provider, domain is missing|||||No Remediation Provided
1000006|||||Invalid definition for external identity provider with domain '{domain}'. Reason: Following properties are mandatory: domain, issuer URI, passive authentication URL.|||||No Remediation Provided
1000007|||||Invalid definition for external identity provider with domain '{domain}'. Reason: The value '{url}' in the property '{urlType}' must be an absolute URL.|||||No Remediation Provided
1000008|||||Invalid definition for external identity provider with domain '{domain}'. Reason: The value '{url}' in the property '{urlType}' must be https.|||||No Remediation Provided
1000009|||||Invalid definition for external identity provider with domain '{domain}'. Reason: Only WsFederation/SamlP protocols are allowed.|||||No Remediation Provided
1000010|||||Invalid definition for external identity provider with domain '{domain}'. Reason: Domain '{value}' is not in expected format.|||||No Remediation Provided
1000011|||||Invalid definition for external identity provider with domain '{domain}'. Reason: Issuer '{value}' is not in expected format.|||||No Remediation Provided
1000012|||||Invalid definition for external identity provider with domain '{domain}'. Reason: Domain '{value}' is a reserved value.|||||No Remediation Provided
1000013|||||Invalid definition for external identity provider with domain '{domain}'. Reason: Issuer '{value}' is a reserved value.|||||No Remediation Provided
1000014|||||Cannot issue On-Behalf-Of token for tenant '{tenant1}' as JWT bearer token was issued for '{tenant2}'.|||||No Remediation Provided
1000015|||||Direct federation users are not expected to have home tenant.|||||No Remediation Provided
1000018|||||Realm with domain '{domain}' is not an external realm.|||||No Remediation Provided
1000019|||||The provided certificate authority type '{certificateAuthorityType}' is not valid.|||||No Remediation Provided
1000020|||||The provided application '{applicationId}' may not be used on this endpoint.|||||No Remediation Provided
1000021|||||External Claims Provider unavailable: general exception.|||||No Remediation Provided
1000022|||||External Claims Provider unavailable: WebException status code '{status}'.|||||No Remediation Provided
1000023|||||The GitHub access token forwarded exceeds the configured length of '{sizeLimit}'.|||||No Remediation Provided
1000024|||||Requested claim 'ClientIpReportedByRP' should have a single and valid ip address.|||||No Remediation Provided
1000025|||||Received invalid stk_jwk.|||||No Remediation Provided
1000026|||||Received invalid Primary Refresh Token.|||||No Remediation Provided
1000027|||||Session Transport Key is not present.|||||No Remediation Provided
1000028|||||Received invalid Windows SSO Credential.|||||No Remediation Provided
1000029|||||The provided confirmation request (req_cnf or pop_jwk) is not properly formatted.|||||No Remediation Provided
1000030|||||Microsoft Account granted Refresh Token Credential is not supported on AAD tenant.|||||No Remediation Provided
1000031|||||Application {appDisplayName} cannot be accessed at this time. Contact your administrator.|||||Contact your administrator for more information.
1000032|||||Received invalid stk_jwk key thumbprint.|||||No Remediation Provided
1000033|||||Stk_jwk key doesn't match session transport key thumbprint specified at the beginning of the session.|||||No Remediation Provided
1000034|||||Stk_jwk key must not be submitted via x5c.|||||No Remediation Provided
1000035|||||There was an error issuing Bound RT token.|||||No Remediation Provided
1000036|||||BoundRT use as a bearer refresh token is unsupported.|||||No Remediation Provided
1000037|||||Stk_jwk thumbprint is not provided for SSO Bound RT redemption.|||||No Remediation Provided
1000038|||||Received invalid req_cnf key thumbprint.|||||No Remediation Provided
1000039|||||Req_cnf key '{kid}' doesn't match proof of possession key thumbprint specified at the beginning of the session.|||||No Remediation Provided
1000101|||||Access denied.|||||No Remediation Provided
1000102|||||Invalid request.|||||No Remediation Provided
1000103|||||Invalid request.|||||No Remediation Provided
1000104|||||Resource cloud {resourceCloud} is not allowed on identity tenant {identityTenant}.|||||No Remediation Provided
1000106|||||The provided sec-Restrict-Tenant-Access-Policy header ({headerValue}) is invalid. Please double check the format of the header and try again.|||||No Remediation Provided
1000107|||||The tenant ID {tenantId} provided in the sec-Restrict-Tenant-Access-Policy header was not found in Azure Active Directory. Please contact your administrator for assistance.|||||No Remediation Provided
1000108|||||The policy ID {policyId} provided in the sec-Restrict-Tenant-Access-Policy header did not match a policy ID in tenant {tenantName}. Please contact your administrator for assistance.|||||No Remediation Provided
1000110|||||Invalid request, identity tenant '{identityTenant}' is not allowed on resource tenant '{resourceTenant}' for cross cloud B2B call.|||||No Remediation Provided
1000112|||||Cannot issue On-Behalf-Of token for tenant '{tenant1}' as JWT bearer token was issued for '{tenant2}'.|||||No Remediation Provided
1000113|||||Non Retryable Error Occured.|||||No Remediation Provided
1000114|||||Invalid request. Endpoint does not accept requests with multiple DataCriteria items of type {dataCriteriaType}.|||||No Remediation Provided
1000115|||||Invalid request. TenantId in the URL and DataCriteria has to match.|||||No Remediation Provided
1000116|||||Invalid request. One of the ids in the PolicyObjectIds is not a valid Guid.|||||No Remediation Provided
1000117|||||Invalid request. Max policyIds count of {policyObjectIdsMaxCount} exceeded.|||||No Remediation Provided
1000118|||||Invalid request. UserId cannot be an empty Guid.|||||No Remediation Provided
1000119|||||Invalid global bloomfilter name: {name}.|||||No Remediation Provided
1000202|||||Migration to public cloud is complete for this tenant. Please use login.microsoftonline.com endpoint for this tenant.|||||No Remediation Provided
1000203|||||There’s been a change to your organization. You’ll need to sign out and sign back in to continue using this app. To learn more, refer https://go.microsoft.com/fwlink/?linkid=2150446.|||||No Remediation Provided
1000401|||||The requested tenant has been migrated to {targetCloud}.|||||No Remediation Provided
1000450|||||There is only MSA user active session and need to redirect to Msa.|||||No Remediation Provided
1000460|||||The provided x-ms-plid header value '{headerValue}' is not a properly formatted private link identifier.|||||No Remediation Provided
1000461|||||Private link data couldn't be read. Please try again.|||||No Remediation Provided
1000462|||||The specified private link was not found. If you just provisioned this private link, please wait a few minutes and try again.|||||No Remediation Provided
1000463|||||The tenant you're trying to access, '{tenantName}', is not authorized to use this private link.|||||No Remediation Provided
1000464|||||Private link data couldn't be upserted/read. Please try again.|||||No Remediation Provided
1000465|||||The required private link state could not be found.|||||No Remediation Provided
1000466|||||The provided AppID ACR value is not supported.|||||No Remediation Provided
1000470|||||The protocol {protocolId} is blocked for tenant {tenantId}. Please contact your administrator for assistance.|||||No Remediation Provided
1000471|||||The document with private link id {plid} already present associated with private link resource id {plrid}|||||No Remediation Provided
1000472|||||Unable to parse the session store last written time {lastWrittenTime}.|||||No Remediation Provided
1000473|||||Unable to create session pointer for {sessionType} due to {reason}.|||||No Remediation Provided
1000474|||||User is creating too many freshly logged-in sessions or new refresh tokens in a short period of time. Please try again later.|||||No Remediation Provided
1000501|||||Unable to read session document from Session Store.|||||No Remediation Provided
1000502|||||The provided certificate is not within its specified validity window.|||||No Remediation Provided
1000503|||||Request contains mismatched device ids.|||||No Remediation Provided
1000601|||||This API is not currently supported.|||||No Remediation Provided
1000602|||||Action not permitted. Only managed identity service could call this API.|||||No Remediation Provided
1000603|||||Unsupported tenant provided. The tenant must be a guid.|||||No Remediation Provided
1000604|||||Invalid request parameters.|||||No Remediation Provided
1000605|||||An error occurred during certificate creation.|||||No Remediation Provided
1000606|||||A requested pass through claim is not permitted for this client.|||||No Remediation Provided
1000607|||||This API is not currently supported.|||||No Remediation Provided
1000608|||||Invalid request parameters.|||||No Remediation Provided
1000701|||||Multiple devices with the same device-name found in tenant {tenant}. Please reach out to your tenant-admin to ensure uniqueness of device display-name.|||||No Remediation Provided
1000800|||||Unsupported compound-resource format.|||||No Remediation Provided
1000901|||||The provided certificate cannot be used for requesting tokens. The value of token_not_after extension on the certificate should be greater than the current time.|||||No Remediation Provided
1000902|||||The certificate provided for authentication should contain the Authority Key Identifier (AKI) extension.|||||No Remediation Provided
1000903|||||The Authority Key Identifier extension in the provided certificate doesn't match with the Key Identifier of any available Keys used for signing the certificates.|||||No Remediation Provided
1000904|||||The Format of token_not_after extension is invalid.|||||No Remediation Provided
1001000|||||Unable to acquire certificate policy from tenant|||||No Remediation Provided
1001001|||||Certificate policy acquired from tenant is invalid and contains no user bindings|||||No Remediation Provided
1001002|||||Certificate policy does not contain any valid user bindings|||||No Remediation Provided
1001003|||||Unable to acquire value specified in binding from certificate|||||No Remediation Provided
1001004|||||Unable to create rsa key with the provided exponent and modulus|||||No Remediation Provided
1001005|||||Invalid Request. A certificate should be provided with a non empty value.|||||No Remediation Provided
1001006|||||A transient issue occured, please try again|||||No Remediation Provided
1001007|||||Failed to write revocation events into the storage|||||No Remediation Provided
1001008|||||Failed to read revocation events from the storage|||||No Remediation Provided
1001010|||||The client or resource application: {applicationId} is missing service principal in the tenant: {tenant}. See instructions here: https://go.microsoft.com/fwlink/?linkid=2167121.|||||No Remediation Provided
1001011|||||The request to proxy a call to MSA via this AAD instance is not currently supported.|||||No Remediation Provided
1001012|||||The user principal name entered does not match the user specific information from the certificate.|||||No Remediation Provided
1100000|||||Non-retryable error has occurred.|||||No Remediation Provided
1300011|||||NGC key is malformed.|||||No Remediation Provided
1300012|||||Signature key type is not provided.|||||No Remediation Provided
1300041|||||NGC key cannot be decoded.|||||No Remediation Provided
1300042|||||NGC key is not associated with a device.|||||No Remediation Provided
1350001|||||Fido assertion verification failed. Result: '{result}'|||||No Remediation Provided
1350011|||||Key ID cannot be decoded.|||||No Remediation Provided
1350101|||||Key ID cannot be decoded.|||||No Remediation Provided
1400001|||||Request nonce is not provided.|||||No Remediation Provided
1400002|||||Request nonce is malformed.|||||No Remediation Provided
1400011|||||Session key is not provided.|||||No Remediation Provided
1400012|||||Session key type {type} is not supported.|||||No Remediation Provided
1659001|||||Unexpected error decoding the required request.|||||No Remediation Provided
2190001|||||Cannot find a certificate in the pfx.|||||No Remediation Provided
2190002|||||Cannot use the pfx.|||||No Remediation Provided
2200501|||||No cache encryption keys are available for encryption.|||||No Remediation Provided
2200502|||||No cache encryption keys are available for encryption - no key was more than 48 hours old.|||||No Remediation Provided
2201001|||||Authenc: VerifySignatureAndDecrypt failed. {ex}|||||No Remediation Provided
2300241|||||Failed to find cached credential cert with thumbprint: {thumbPrint}.|||||No Remediation Provided
5000211|||||A tenant restrictions policy added to this request by a device or network administrator does not allow access to the resource tenant.|||||The administrator of the tenant that owns this tenant restrictions policy does not allow this access. If this is not expected, that administrator should allow access by editing their cross tenant access policy.
5000221|||||Access to '{tenant}' tenant is denied.|||||Please contact your IT department.
5000222|||||Access to '{tenant}' tenant is denied. It looks like you are trying to access a resource in Microsoft Cloud Deutschland. This organization is in the process of being decommissioned and needs to be re-created in a German datacenter region. Please see aka.ms/office365germancymove for more information, or contact deblockres@microsoft.com for assistance.|||||Please contact your IT department.
5000610|||||Symmetric Key Derivation Function version '{version}' is invalid.|||||No Remediation Provided
5000611|||||Symmetric Key Derivation Function version '{version}' is invalid.|||||No Remediation Provided
5000810|||||Unable to verify token signature. Signing key identifier is missing.|||||No Remediation Provided
5000811|||||Unable to verify token signature. The signing key identifier does not match any valid registered keys.|||||No Remediation Provided
5000812|||||The SAML 1.1 credential must contain exactly one or zero claims of type '{type}'.|||||No Remediation Provided
5000813|||||The SAML 1.1 credential must provide non empty value for claim of type '{type}'.|||||No Remediation Provided
5000815|||||The SAML 1.1 credential contains invalid Device ID claim.|||||No Remediation Provided
5000816|||||The SAML 1.1 credential must contain exactly one Audience in AudienceRestriction.|||||No Remediation Provided
5000817|||||The SAML 1.1 credential must contain SamlAudienceRestrictionCondition.|||||No Remediation Provided
5000818|||||SAML Assertion is invalid. NameId is not present in the token.|||||No Remediation Provided
5000819|||||SAML Assertion is invalid. Email address claim is missing or does not match domain from an external realm.|||||No Remediation Provided
7000011|||||Requested SAML 2.0 assertion has invalid SubjectConfirmation Method: {method}.|||||No Remediation Provided
7000012|||||The grant was obtained for a different tenant.|||||No Remediation Provided
7000013|||||The grant is not supported by API version {apiVersion}.|||||No Remediation Provided
7000014|||||The provided value for the input parameter 'device_code' is not valid.|||||No Remediation Provided
7000015|||||The grant was obtained for a different tenant.|||||No Remediation Provided
7000016|||||Primary refresh token is not signed with session key.|||||No Remediation Provided
7000017|||||Broker restricted refresh token can't be used as credential.|||||No Remediation Provided
7000018|||||Token binding header is empty.|||||No Remediation Provided
7000019|||||Token binding hash does not match.|||||No Remediation Provided
7000020|||||SAML 2.0 Bearer assertion must be a valid Base64Url encoded value.|||||No Remediation Provided
7000021|||||Unrecognized grant type {type}.|||||No Remediation Provided
7000022|||||VSM Binding Key missing from Ticket Granting Ticket request.|||||No Remediation Provided
7000023|||||VSM Binding key mismatch.|||||No Remediation Provided
7000024|||||Inconsistent broker application IDs asserted by incoming credentials.|||||No Remediation Provided
7000025|||||Ambiguous request. The grant contains duplicate claims.|||||No Remediation Provided
7000026|||||Provided grant is invalid or malformed. The grant requires an encrypted response, but the client is not indicating it understands encrypted responses.|||||No Remediation Provided
7000110|||||Request is ambiguous, multiple application identifiers found.|||||No Remediation Provided
7000112|||||Application '{appIdentifier}'({appName}) is disabled.|||||No Remediation Provided
7000113|||||Application '{appIdentifier}' is not authorized to make application on-behalf-of calls.|||||No Remediation Provided
7000114|||||Application '{appIdentifier}' is not allowed to make application on-behalf-of calls.|||||No Remediation Provided
7000115|||||This grant is reedemable only by broker application.|||||No Remediation Provided
7000116|||||Application '{appIdentifier}'({appName}) is disabled in tenant {tenant}. Please review the documentation: https://go.microsoft.com/fwlink/?linkid=2167553|||||No Remediation Provided
7000117|||||Resource application '{appIdentifier}'({appName}) is disabled in tenant {tenant}. Please review the documentation: https://go.microsoft.com/fwlink/?linkid=2167553|||||No Remediation Provided
7000210|||||Unable to find source of Trusted Certificate Authority policy.|||||No Remediation Provided
7000211|||||Trusted Certificate Authority policy is not configured on the tenant '{tenantId}'.|||||No Remediation Provided
7000212|||||No matching Trusted Certificate Authority policy found for authorized subject name.|||||No Remediation Provided
7000213|||||Invalid certificate chain.|||||No Remediation Provided
7000214|||||Certificate has been revoked.|||||No Remediation Provided
7000215|||||Invalid client secret provided. Ensure the secret being sent in the request is the client secret value, not the client secret ID, for a secret added to app '{identifier}'.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
7000216|||||'client_assertion', 'client_secret' or 'request' is required for the 'client_credentials' grant type.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
7000217|||||The service principal named {appPhrase} was not found in the tenant named {tenant_name}. This can happen if the application has not been installed by the administrator of the tenant.|||||No Remediation Provided
7000218|||||The request body must contain the following parameter: 'client_assertion' or 'client_secret'.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
7000219|||||'client_assertion' or 'client_secret' is required for the '{type}' grant type.|||||No Remediation Provided
7000220|||||Client application identifier in the provided grant doesn't match 'client_id' parameter.|||||No Remediation Provided
7000221|||||Certificate Subject must match Issuer claim in the client assertion.|||||No Remediation Provided
7000222|||||The provided client secret keys for app '{identifier}' are expired. Visit the Azure portal to create new keys for your app: https://aka.ms/NewClientSecret, or consider using certificate credentials for added security: https://aka.ms/certCreds.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
7000223|||||Application {brokerAppId} is not authorized to broker tokens.|||||No Remediation Provided
7000224|||||Application {childAppId} is not authorized to have tokens brokered on its behalf.|||||No Remediation Provided
7000225|||||Invalid credentials: An MSI certificate was included in the request for the app, but the app (object ID: {oid}, application id: {clientId}) is not an MSI. Ensure that your code is matching MSI identities and certificates appropriately.|||||This is a platform error, and cannot be remediated by the app developer or admin. Consider filing a support ticket against the Azure service that is failing.
7000226|||||No federated identity credential policy found on application ({appid}). The client_assertion used to authenticate the request does not match the subject or application being requested.  Ensure that the application ID in the request is correct, that the app has a policy applied to it, and that the correct client_assertion is being provided in the request.|||||The request attempted to use a credential from one service to authenticate as another service, which requires a federated identity credential to be in place. The application ID in the request does not have a federated credentials policy applied to it, so the request was rejected. Ensure that the app has a policy applied to it, and that the developer intended to perform a cross-service authentication.
7000227|||||No Federated Identity Credential policy found on application that matched the presented MSI-signed client assertion. Expecting a Federated Identity Credential with subject: '{msiSpid}', issuer: '{expectedIssuer}' and audience: '{expectedAudience}'.|||||Ensure that the federated identity credential policy on the application matches the expected values.
7000281|||||Certificate with thumbprint {thumbprint} is not authorized.|||||Developer error - the app is attempting to sign in without the necessary or correct authentication parameters.
7000361|||||Client assertion claim '{claimName}' can only contain a maximum of '{maxItems}' items.|||||No Remediation Provided
7000471|||||A reply address scheme starting with 'brk-' was seen on a request that wasn't for brokering. This scheme is reserved for brokered application requests. Use a valid reply URI instead, either a native app reply URI or an https:// uri.|||||The app sent an inappropriate reply URI on this request. The app should be updated to provide a reply URI that is supported for their flow (https:// or a native app URI)
7500110|||||The query string hash could not be computed for signature generation/validation. Signature algorithm was not specified.|||||No Remediation Provided
7500111|||||The query string hash could not be computed for signature generation/validation. Cannot create a SAML binding message from the given HttpRequest parameters. Check if the request contains a valid Uri or Form POST that contains protocol parameters for SAML HTTP bindings.|||||No Remediation Provided
7500112|||||MessageType property get is not supported by this class.|||||No Remediation Provided
7500510|||||XML attribute '{attributeName}' in the SAML message must be a dateTime.|||||No Remediation Provided
7500511|||||XML attribute '{attributeName}' in the SAML message must be a URI.|||||No Remediation Provided
7500512|||||XML element '{elementName}' in XML namespace '{xmlNamespace}' was not expected in the SAML message. Either the element is not an expected part of a SAML message or was in the wrong location in the message. Check the names and ordering of the elements to confirm they conform to the SAML protocol specifications.|||||No Remediation Provided
7500513|||||The message type '{messageType}' is not a supported type of SAML request. Supported SAML requests are AuthnRequest and LogoutRequest.|||||No Remediation Provided
7500514|||||A supported type of SAML response was not found. The supported response types are 'Response' (in XML namespace 'urn:oasis:names:tc:SAML:2.0:protocol') or 'Assertion' (in XML namespace 'urn:oasis:names:tc:SAML:2.0:assertion').|||||Application error - the developer will handle this error.
7500515|||||Was expecting to find XML element '{xmlElement}' in XML namespace '{xmlNamespace}', but it was not present. Either the expected element is not present or was in the wrong location in the message. Check the names and ordering of the elements to confirm they conform to the SAML protocol specifications.|||||No Remediation Provided
7500516|||||A required attribute is not present in the SAML message: '{xmlAttribute}'.|||||No Remediation Provided
7500517|||||The element '{xmlElement}' in XML namespace '{xmlNamespace}' cannot be empty.|||||No Remediation Provided
7500518|||||The specified comparison '{comparison}' is not a supported value for samlp:AuthnContextComparisonType.|||||No Remediation Provided
7500519|||||An unsupported SAML version was encountered: {version}.|||||No Remediation Provided
7500520|||||Unrecognized XML content of type '{nodeType}', name '{name}' was found at the beginning of the the SAML message. Expected to find an element 'AuthnRequest', 'Response', 'LogoutRequest' or 'LogoutResponse' from XML namespace 'urn:oasis:names:tc:SAML:2.0:protocol'.|||||No Remediation Provided
7500521|||||Unrecognized XML content of type '{nodeType}' was found at the beginning of the the SAML message. Expected to find an element 'AuthnRequest', 'Response', 'LogoutRequest' or 'LogoutResponse' from XML namespace 'urn:oasis:names:tc:SAML:2.0:protocol'.|||||No Remediation Provided
7500522|||||XML element '{xmlElement}' in XML namespace '{xmlNamespace}' in the SAML message must be a URI.|||||No Remediation Provided
7500523|||||The SAML IDPList must contain one or more IDPEntry elements.|||||No Remediation Provided
7500524|||||No saml:AuthnContextClassRef or saml:AuthnContextDeclRefs elements were found within samlp:RequestedAuthnContext.|||||No Remediation Provided
7500525|||||There was an XML error in the SAML message at line {lineNumber}, position {linePosition}. Verify that the XML content of the SAML messages conforms to the SAML protocol specifications.|||||No Remediation Provided
7500526|||||The value '{value}' must be nonnegative.|||||No Remediation Provided
7500527|||||The value '{value}' must be nonnegative and less than or equal to 65535.|||||No Remediation Provided
7500528|||||Unexpected xsi:type: '{message}'|||||No Remediation Provided
7500529|||||The value '{value}' is not a valid SAML ID. The ID must not begin with a number.|||||Azure AD uses this attribute to populate the InResponseTo attribute of the returned response. The ID must not begin with a number, so a common strategy is to prepend a string like "id" to the string representation of a GUID. For example, id6c1c178c166d486687be4aaf5e482730 is a valid ID.
7500530|||||SAML NameId cannot be null.|||||No Remediation Provided
7500531|||||The end of an XML element was expected, but instead XML content of type '{nodeType}', name '{name}' was found. XML content may be present that is not defined in the SAML protocol specifications.|||||No Remediation Provided
7500532|||||The end of an XML element was expected, but instead XML content of type '{nodeType}' was found. XML content may be present that is not defined in the SAML protocol specifications.|||||No Remediation Provided
7500533|||||The SAML response was expected to start with either a Response element or a LogoutResponse element, from the XML namespace 'urn:oasis:names:tc:SAML:2.0:protocol'.|||||No Remediation Provided
7500534|||||Exactly one saml:AuthnContextClassRef or saml:AuthnContextDeclRefs element is expected in the samlp:RequestedAuthnContext.|||||No Remediation Provided
9000410|||||Malformed JSON.|||||No Remediation Provided
9000411|||||The request is not properly formatted. The parameter '{name}' is duplicated.|||||No Remediation Provided
9000412|||||The request is missing a key.|||||No Remediation Provided
9000413|||||'Context' field is required.|||||No Remediation Provided
9000414|||||Malformed request.|||||No Remediation Provided
9000510|||||Hybrid SPA authorization codes cannot be requested on the app-only flow.|||||No Remediation Provided
9000511|||||Cannot emit Hybrid SPA auth code for Public or SPA client.  You must request the hybrid SPA auth code on your confidential client back-end, while redeeming the original auth code requested for a web type redirect URI.|||||No Remediation Provided
9000512|||||A Hybrid SPA code can only be requested while redeeming a confidential client authorization code (a code issued to a web-type redirect URI). Do not request a hybrid code otherwise.|||||No Remediation Provided
9004351|||||Requested resource '{resource}' cannot accept cross-cloud tokens, where user belongs to the cloud '{nationalCloud}' and authentication request is to https://login.microsoftonline.com.|||||No Remediation Provided
```
