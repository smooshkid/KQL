# SigninLog graph based on country location

```KQL
let timeframe=1h;
let sensitivity=2;
let threshold=400;
let outliercountries=
SigninLogs
| where TimeGenerated between (startofday(ago(21d))..startofday(ago(1d)))
| where ResultType == 0
| make-series SigninCount=count() on TimeGenerated from startofday(ago(21d)) to startofday(ago(1d)) step timeframe by Location
| extend outliers=series_decompose_anomalies(SigninCount, sensitivity)
| mv-expand TimeGenerated, SigninCount, outliers
| where outliers == 1 and SigninCount > threshold
| distinct Location;
SigninLogs
| where TimeGenerated between (startofday(ago(21d))..startofday(ago(1d)))
| where ResultType == 0
| where Location  in (outliercountries)
| make-series SigninCount=count() on TimeGenerated from startofday(ago(21d)) to startofday(ago(1d)) step timeframe by Location
| render timechart
```
