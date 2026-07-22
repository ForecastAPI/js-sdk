# ForecastAPI.BatchForecastStatusResponseResults

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**summary** | [**BatchForecastStatusResponseResultsSummary**](BatchForecastStatusResponseResultsSummary.md) |  | [optional] 
**data** | [**{String: BatchSeriesResult}**](BatchSeriesResult.md) | Each series&#39; results, keyed by ENTITY id rather than by your identifier — one batch may legitimately contain the same identifier under several tenant_context values, so the identifier alone would not be unique. Match series via the identifier and tenant_context echoed inside each result.  | [optional] 


