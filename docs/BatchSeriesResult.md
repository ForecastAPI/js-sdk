# ForecastAPI.BatchSeriesResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** |  | [optional] 
**tenantContext** | **String** |  | [optional] 
**forecasts** | [**[ForecastPeriod]**](ForecastPeriod.md) |  | [optional] 
**modelInfo** | **{String: Object}** |  | [optional] 
**adjusted** | [**AdjustedForecast**](AdjustedForecast.md) |  | [optional] 
**accumulated** | [**AccumulatedForecast**](AccumulatedForecast.md) |  | [optional] 
**error** | **String** | Present instead of forecasts when this series failed | [optional] 


