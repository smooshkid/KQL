# Basic queries for searching Palo Alto firewall logs

##### Queries firewall logs based on a specific firewall and IP address
```KQL
CommonSecurityLog
| where DeviceVendor == "Palo Alto Networks"
| where DeviceName == ""
| where SourceIP == ""
```
