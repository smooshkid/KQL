# Basic queries for searching Palo Alto firewall logs
##### Useful to understand what data is available in the CommonSecurityLog table
```KQL
CommonSecurityLog
| getschema
```
##### Filter by Palo Alto logs
```KQL
CommonSecurityLog
| where DeviceVender == 'Palo Alto Networks'
```
##### Filter by Fortigate logs
```KQL
CommonSecurityLog
| where DeviceVender == 'Fortinet'
```
##### Queries firewall logs based on a specific firewall and IP address
```KQL
CommonSecurityLog
| where DeviceVendor == "Palo Alto Networks"
| where DeviceName == ""
| where SourceIP == ""
```
##### Filters out logs without 'allow' DeviceAction
```KQL
CommonSecurityLog
| where DeviceVendor == "Palo Alto Networks"
| where DeviceName == ""
| where SourceIP == ""
| where DeviceAction <> "allow"
```
##### Filter for Palo Alto CONFIG logs
```KQL
CommonSecurityLog
| where Activity == 'CONFIG'
```
