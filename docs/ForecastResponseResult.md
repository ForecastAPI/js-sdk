# ForecastAPI.ForecastResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** | Echoes the series identifier from the request | [optional] 
**tenantContext** | **String** |  | [optional] 
**forecasts** | [**[ForecastPeriod]**](ForecastPeriod.md) | One row per forecast period. Each period carries its own bounds, and they widen with horizon. | [optional] 
**modelInfo** | **{String: Object}** | The selected model (&#x60;best_model&#x60;), the models evaluated, the interval source, and per-model back-testing scores (smape/mape/mase) when validation runs. Also carries &#x60;bounds_transform&#x60; when &#x60;value_bounds&#x60; was sent, and &#x60;quantile_levels&#x60; when a fan was requested.  | [optional] 


