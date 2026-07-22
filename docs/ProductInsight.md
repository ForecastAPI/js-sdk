# ForecastAPI.ProductInsight

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_class** | **String** | Insight family (e.g. margin, sales, cost, lead_time) | [optional] 
**type** | **String** |  | [optional] 
**severity** | **String** |  | [optional] 
**title** | **String** |  | [optional] 
**description** | **String** |  | [optional] 
**metrics** | **{String: Object}** | The numbers behind the insight | [optional] 
**recommendation** | [**ProductInsightRecommendation**](ProductInsightRecommendation.md) |  | [optional] 
**confidence** | **String** |  | [optional] 
**date** | **String** |  | [optional] 
**changeStatus** | **String** | How this insight compares to the previous analysis of the same product — every insight is \&quot;new\&quot; on the first analysis | [optional] 



## Enum: SeverityEnum


* `critical` (value: `"critical"`)

* `warning` (value: `"warning"`)

* `info` (value: `"info"`)




