# Basic queries for searching Palo Alto firewall logs

##### Queries firewall logs based on an specific firewall and IP address
```KQL
CommonSecurityLog
| where DeviceVendor == "Palo Alto Networks"
| where DeviceName == ""
| where SourceIP == ""
```
