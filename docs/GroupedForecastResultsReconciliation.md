# ForecastAPI.GroupedForecastResultsReconciliation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**method** | **String** |  | [optional] 
**correlation** | **Number** | bottom_up only | [optional] 
**correlationSource** | **String** | bottom_up only | [optional] 
**measured** | **Boolean** | bottom_up only — always false; the cross-sibling correlation is an assumption | [optional] 
**variant** | **String** | min_trace only — the MinTrace weighting used | [optional] 
**nonnegative** | **Boolean** | min_trace only — whether the non-negative solve was applied | [optional] 



## Enum: MethodEnum


* `bottom_up` (value: `"bottom_up"`)

* `min_trace` (value: `"min_trace"`)





## Enum: CorrelationSourceEnum


* `default` (value: `"default"`)

* `request` (value: `"request"`)




