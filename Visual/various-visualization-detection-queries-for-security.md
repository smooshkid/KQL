# Visualization queries with security in mind
#### Some queries use example data, or are based on hyopthetical scenarios, and you should switch in relevant data to your environment if required

### Visualizing sign in data with summarize and render
```KQL
SigninLogs
| where TimeGenerated > ago (30d)
| summarize Count=count() by bin(TimeGenerated, 1d)
| render timechart
```

### Visualizing authentication requirement data with summarize and render
```KQL
SigninLogs
| where TimeGenerated > ago (30d)
| summarize Count=count() by bin(TimeGenerated, 1d), AuthenticationRequirement
| render timechart
```

### Visualizing sign in data with make-series and render
```KQL
SigninLogs
| where TimeGenerated > ago (30d)
| make-series Count=count() default=0 on TimeGenerated step 1d
| render timechart
```

### Visualizing the difference between make series and summarize
```KQL
For summarize:
LAQueryLogs
| where TimeGenerated > ago (30d)
| summarize Count=count() by bin(TimeGenerated, 1d)
| render timechart


For make-series:
LAQueryLogs
| where TimeGenerated > ago (30d)
| make-series Count=count() default=0 on TimeGenerated step 1d
| render timechart
```

### Returning stats using series_stats()
```KQL
SigninLogs
| where TimeGenerated > ago (30d)
| make-series Count=count() default=0 on TimeGenerated step 1d
| project series_stats(Count)
```

### Visualizing trend lines with make-series
```KQL
SigninLogs
| where TimeGenerated > ago (30d)
| make-series Count=count() default=0 on TimeGenerated step 1d
| extend (RSquare, SplitIdx, Variance, RVariance, TrendLine)=series_fit_2lines(Count)
| project TimeGenerated, Count, TrendLine
| render timechart
```

### Visualizing forecasts using make-series
```KQL
SigninLogs
| make-series Count=count() on TimeGenerated from ago(30d)to now()+14d step 1d
| extend forecast = series_decompose_forecast(Count, toint(30d/1d))
| render timechart
```

### Detecting anomalies using time-series analysis
```KQL
let timeframe=1h;
let sensitivity=2;
let threshold=10;
SigninLogs
| where TimeGenerated between (startofday(ago(21d))..startofday(ago(1d)))
| where ResultType == 0
| make-series SigninCount=count() on TimeGenerated from startofday(ago(21d)) to startofday(ago(1d)) step timeframe by Location
| extend outliers=series_decompose_anomalies(SigninCount, sensitivity)
| mv-expand TimeGenerated, SigninCount, outliers
| where outliers == 1 and SigninCount > threshold
```

### Visualizing anomalies using time-series analysis
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

##### MSFT Employee Contribution-Yong Rhee
### You can detect anomalies in many different data sets, including email. Phishing attacks tend to be very short lived, with a sudden burst in activity, which is great to detect and visualize.
```KQL
let interval = 12h;
EmailEvents
| make-series MailCount = count() on Timestamp from ago(30d) to now() step interval by SenderFromDomain
| extend (flag, score, baseline) = series_decompose_anomalies(MailCount)
| mv-expand flag to typeof(int)
| where flag == 1 
| mv-expand score to typeof(double) // expand the score array to a double
| summarize MaxScore = max(score) by SenderFromDomain
| top 5 by MaxScore desc // Get the top 5 highest scoring domains
| join kind=rightsemi EmailEvents on SenderFromDomain
| summarize count() by SenderFromDomain, bin(Timestamp, interval)
| render timechart
```
