# ForecastAPI.GroupedForecastAccepted

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**groupedForecastId** | **String** | Id to poll via GET /v2/forecast/grouped/{grouped_forecast_id} | [optional] 
**status** | **String** |  | [optional] 
**seriesCount** | **Number** | Leaf series submitted | [optional] 
**nodeCount** | **Number** | What will actually be forecast and reconciled — the leaves plus every derived aggregate and the total | [optional] 
**reconciliation** | **String** |  | [optional] 
**timeTakenMs** | **Number** |  | [optional] 



## Enum: ReconciliationEnum


* `bottom_up` (value: `"bottom_up"`)

* `min_trace` (value: `"min_trace"`)




