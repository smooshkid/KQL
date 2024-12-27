##### Identify PowerShell execution events involving suspicious downloads or commands
```KQL
union DeviceProcessEvents, DeviceNetworkEvents
| where Timestamp > ago(7d)
| where FileName in~ ("powershell.exe", "powershell_ise.exe")
| where ProcessCommandLine has_any("WebClient", "DownloadFile", "DownloadData", "DownloadString", "WebRequest", "Shellcode", "http", "https")
| project Timestamp, DeviceName, InitiatingProcessFileName, InitiatingProcessCommandLine, FileName, ProcessCommandLine, RemoteIP, RemoteUrl, RemotePort, RemoteIPType
| top 100 by Timestamp
'''

## The following query aggregates network event data and identifies IP addresses that have generated a high volume of traffic within the past day, potentially indicating a network anomaly or malicious activity.
```KQL
union DeviceNetworkEvents
| where Timestamp > ago(1d)
| summarize count() by RemoteIP
| where count_ > 1000
| project RemoteIP, count_
```

