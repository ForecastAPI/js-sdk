# ForecastAPI.AdjustedForecast

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**forecasts** | [**[ForecastPeriod]**](ForecastPeriod.md) | The baseline path with every adjustment applied, in array order | [optional] 
**adjustmentsApplied** | [**[AdjustedForecastAdjustmentsAppliedInner]**](AdjustedForecastAdjustmentsAppliedInner.md) | Echo of each adjustment as applied, in order | [optional] 
**stored** | **Boolean** | Always false — only the baseline in &#x60;result&#x60; is persisted and scored for accuracy | [optional] 


