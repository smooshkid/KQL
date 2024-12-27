# Non GP VPN usage seen on ***Palo Threat Logs***

## Description

The following will querey CommonSecurityLogs for **threats** containing VPN usage via firewall logs, showing the distinct VPN names with log count.

### Microsoft Sentinel
```
CommonSecurityLog
| where Activity == 'THREAT'
    and DeviceEventClassID contains 'vpn'
| summarize count() by DeviceEventClassID
```
### Microsoft Sentinel w/o THREAT Activity Only
```
CommonSecurityLog
//| where Activity == 'THREAT'
| where DeviceEventClassID contains 'vpn'
| summarize count() by DeviceEventClassID
