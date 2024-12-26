# Non company VPN usage seen on managed hosts

## Description

The following will querey CommonSecurityLogs for **threats** containing VPN usage via firewall logs.

### Microsoft Sentinel
```
CommonSecurityLog
| where Activity == 'THREAT'
    and DeviceEventClassID contains 'vpn'
| summarize count() by DeviceEventClassID
```
