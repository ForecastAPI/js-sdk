# ForecastapiSdk.ForecastRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** | SKU, Product ID, or other identifier for the data series | 
**frequency** | **String** | Data frequency: - D: Daily - W: Weekly - M: Monthly (end of month) - MS: Monthly (start of month) - ME: Monthly (end of month) - Q: Quarterly - Y: Yearly  | 
**startDate** | **Date** | Optional start date for the forecast | [optional] 
**dataType** | **String** | Type of data (e.g., sales, demand, inventory, web_traffic) | 
**periods** | **Number** | Number of periods to forecast | 
**data** | [**[ForecastRequestDataInner]**](ForecastRequestDataInner.md) | Historical time series data | 



## Enum: FrequencyEnum


* `D` (value: `"D"`)

* `W` (value: `"W"`)

* `M` (value: `"M"`)

* `MS` (value: `"MS"`)

* `ME` (value: `"ME"`)

* `Q` (value: `"Q"`)

* `Y` (value: `"Y"`)




