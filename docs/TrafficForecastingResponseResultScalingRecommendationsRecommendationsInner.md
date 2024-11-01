# ForecastapiSdk.TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action** | **String** | Recommended scaling action | [optional] 
**currentCapacity** | **Number** | Current capacity | [optional] 
**recommendedCapacity** | **Number** | Recommended capacity | [optional] 
**scalingFactor** | **Number** | Scaling multiplier | [optional] 
**reason** | **String** | Explanation for the recommendation | [optional] 
**urgency** | **String** | Urgency level of the action | [optional] 
**estimatedTimeToScale** | **Number** | Estimated minutes needed for scaling | [optional] 
**potentialSavings** | **Number** | Potential cost savings (for scale down) | [optional] 



## Enum: ActionEnum


* `scale_up` (value: `"scale_up"`)

* `scale_down` (value: `"scale_down"`)

* `maintain` (value: `"maintain"`)





## Enum: UrgencyEnum


* `critical` (value: `"critical"`)

* `high` (value: `"high"`)

* `medium` (value: `"medium"`)

* `low` (value: `"low"`)

* `none` (value: `"none"`)




