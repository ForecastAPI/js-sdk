# ForecastAPI.ProductInsightsBatchStatusResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** | The batch id | [optional] 
**status** | **String** |  | [optional] 
**batchParts** | **Number** |  | [optional] 
**results** | **{String: Object}** | Summary and per-product analysis results as parts complete | [optional] 
**parts** | **[{String: Object}]** | Per-part progress, each carrying its analyses once processed | [optional] 
**startedAt** | **Date** |  | [optional] 
**completedAt** | **Date** |  | [optional] 
**createdAt** | **Date** |  | [optional] 
**updatedAt** | **Date** |  | [optional] 



## Enum: StatusEnum


* `pending` (value: `"pending"`)

* `processing` (value: `"processing"`)

* `completed` (value: `"completed"`)

* `failed` (value: `"failed"`)




