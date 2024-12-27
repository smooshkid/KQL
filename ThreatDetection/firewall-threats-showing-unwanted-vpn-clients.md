# Non company VPN usage seen on ***Palo Threat Logs***

## Description

The following will querey CommonSecurityLogs for **threats** containing VPN usage via firewall logs.

### Microsoft Sentinel
```KQL
CommonSecurityLog
| where Activity == 'THREAT'
    and DeviceEventClassID contains 'vpn'
| summarize count() by DeviceEventClassID
```
