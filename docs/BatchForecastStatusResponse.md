# ForecastAPI.BatchForecastStatusResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** | The batch id | [optional] 
**status** | **String** |  | [optional] 
**batchParts** | **Number** | Number of parts the batch was split into for processing | [optional] 
**results** | [**BatchForecastStatusResponseResults**](BatchForecastStatusResponseResults.md) |  | [optional] 
**parts** | [**[BatchForecastStatusResponsePartsInner]**](BatchForecastStatusResponsePartsInner.md) | Per-part progress metadata (the forecasts themselves live under results.data) | [optional] 
**startedAt** | **Date** |  | [optional] 
**completedAt** | **Date** |  | [optional] 
**createdAt** | **Date** |  | [optional] 
**updatedAt** | **Date** |  | [optional] 



## Enum: StatusEnum


* `pending` (value: `"pending"`)

* `processing` (value: `"processing"`)

* `completed` (value: `"completed"`)

* `failed` (value: `"failed"`)




