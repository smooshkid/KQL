# Successful sign-ins by application

## Description

Creates a pie chart showing the number of successful sign-ins by application over a set amount of time or days.


### Microsoft Sentinel
```
SigninLogs
| where TimeGenerated > ago(14d)
| where ResultType == "0"
| summarize Appcount = count() by AppDisplayName
| render piechart
```
