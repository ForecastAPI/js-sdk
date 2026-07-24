# ForecastAPI.TrafficForecastingRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** | Metric identifier (e.g., endpoint name, service name) | 
**frequency** | **String** | Data frequency for forecasting: - M: Minute (for real-time traffic) - H: Hourly - D: Daily - W: Weekly - MS: Monthly (start of month) - ME: Monthly (end of month) - Q: Quarterly - Y: Yearly  | 
**startDate** | **Date** | Optional start date for the forecast period | [optional] 
**periods** | **Number** | Number of periods to forecast ahead | 
**model** | **String** | Forecasting model behind the plan. &#x60;auto&#x60; routes the identifier to whichever model has proven most accurate on it, sharing the scorecard built by /v2/forecast and /v2/batch/forecast; on this endpoint auto&#39;s ensemble default runs as &#x60;standard&#x60; until a winner emerges, and the decision is reported in &#x60;meta.auto_selection&#x60;. Advanced variants, ensemble and auto cost 25% more usage.  | [optional] [default to &#39;standard&#39;]
**enableIntelligentAggregation** | **Boolean** | Enable intelligent data aggregation for improved forecasting | [optional] 
**confidenceLevel** | **Number** | Confidence level for forecast intervals (default 0.95) | [optional] 
**data** | [**[TrafficForecastingRequestDataInner]**](TrafficForecastingRequestDataInner.md) | Historical traffic data for forecasting | 
**trafficSettings** | [**TrafficForecastingRequestTrafficSettings**](TrafficForecastingRequestTrafficSettings.md) |  | 



## Enum: FrequencyEnum


* `M` (value: `"M"`)

* `H` (value: `"H"`)

* `D` (value: `"D"`)

* `W` (value: `"W"`)

* `MS` (value: `"MS"`)

* `ME` (value: `"ME"`)

* `Q` (value: `"Q"`)

* `Y` (value: `"Y"`)





## Enum: ModelEnum


* `standard` (value: `"standard"`)

* `advanced` (value: `"advanced"`)

* `advanced-quantized` (value: `"advanced-quantized"`)

* `advanced-patched` (value: `"advanced-patched"`)

* `ensemble` (value: `"ensemble"`)

* `auto` (value: `"auto"`)




