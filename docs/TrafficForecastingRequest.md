# ForecastAPI.TrafficForecastingRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** | Metric identifier (e.g., endpoint name, service name) | 
**frequency** | **String** | Data frequency for forecasting: - M: Minute (for real-time traffic) - H: Hourly - D: Daily - W: Weekly - MS: Monthly (start of month) - ME: Monthly (end of month) - Q: Quarterly - Y: Yearly  | 
**startDate** | **Date** | Optional start date for the forecast period | [optional] 
**periods** | **Number** | Number of periods to forecast ahead | 
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




