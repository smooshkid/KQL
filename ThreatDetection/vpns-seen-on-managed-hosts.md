# Non company VPN usage seen on managed hosts

## Description

The following will output vpn clinets seen on companay managed hosts

### Microsoft Sentinel
```
CommonSecurityLog
| where Activity == 'THREAT'
    and DeviceEventClassID contains 'vpn'
| summarize count() by DeviceEventClassID
```
