# ForecastAPI.AccumulatedForecastAssumptions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**correlation** | **Number** |  | [optional] 
**correlationSource** | **String** |  | [optional] 
**measured** | **Boolean** | True only when the correlation in force is our measured default — a caller-supplied value is never labelled measured | [optional] 
**basis** | **String** | The statistical model behind the total&#39;s band | [optional] 
**decay** | **Number** |  | [optional] 
**discountRate** | **Number** |  | [optional] 
**periodsPerYear** | **Number** | How the annual discount rate was converted to the series frequency | [optional] 
**timing** | **String** |  | [optional] 



## Enum: CorrelationSourceEnum


* `default` (value: `"default"`)

* `request` (value: `"request"`)




