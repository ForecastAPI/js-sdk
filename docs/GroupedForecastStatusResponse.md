# ForecastAPI.GroupedForecastStatusResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**groupedForecastId** | **String** |  | [optional] 
**status** | **String** | The run is all-or-nothing — there is no per-node failure state | [optional] 
**nodeCount** | **Number** |  | [optional] 
**results** | [**GroupedForecastResults**](GroupedForecastResults.md) | Populated once status is &#x60;completed&#x60;; null before that and on failure | [optional] 
**error** | **String** | Failure reason when status is &#x60;failed&#x60; | [optional] 
**startedAt** | **Date** |  | [optional] 
**completedAt** | **Date** |  | [optional] 
**createdAt** | **Date** |  | [optional] 



## Enum: StatusEnum


* `pending` (value: `"pending"`)

* `processing` (value: `"processing"`)

* `completed` (value: `"completed"`)

* `failed` (value: `"failed"`)




