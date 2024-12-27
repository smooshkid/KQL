# NON-Successful Signins with Result Description

## Microsoft Sentinel
```
SigninLogs
| where TimeGenerated > ago(1h)
| where ResultType != '0'
| project TimeGenerated, Identity, ResultType, ResultDescription
```
