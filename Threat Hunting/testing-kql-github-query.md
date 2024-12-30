# testing testing one two


```KQL
let SuspiciousTLD = externaldata(TLD: string)[@"https://raw.githubusercontent.com/smooshkid/KQL/refs/heads/main/IOCs/testing-kql-query-from-github.csv"] with (format="csv", ignoreFirstRecord=True);
DeviceNetworkEvents  
| where ActionType == "DnsConnectionInspected"
| extend AdditionalFields = todynamic(AdditionalFields)
| extend DnsQuery = tostring(AdditionalFields.query), ResponseCode = tostring(AdditionalFields.rcode_name), Direction = tostring(AdditionalFields.direction)
| extend TLDArray = split(DnsQuery,'.')
| extend TLD = strcat(".",TLDArray[array_length(TLDArray)-1])
| where Direction == "Out"
| project DeviceName, DnsQuery, ResponseCode, TLDArray, TLD
| join SuspiciousTLD on $left.TLD == $right.TLD
```
