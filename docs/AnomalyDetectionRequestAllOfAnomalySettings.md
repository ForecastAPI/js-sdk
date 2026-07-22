# ForecastAPI.AnomalyDetectionRequestAllOfAnomalySettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**method** | **String** | Detection method; auto picks the best fit for the data&#39;s characteristics | [optional] [default to &#39;auto&#39;]
**threshold** | **Number** | Z-score threshold for the zscore method | [optional] 
**multiplier** | **Number** | IQR multiplier for the iqr method | [optional] 
**seasonalPeriod** | **Number** | Season length for the seasonal method; detected automatically when omitted | [optional] 
**minimumPeriods** | **Number** | Minimum data points required before detection runs | [optional] 



## Enum: MethodEnum


* `auto` (value: `"auto"`)

* `zscore` (value: `"zscore"`)

* `iqr` (value: `"iqr"`)

* `seasonal` (value: `"seasonal"`)




