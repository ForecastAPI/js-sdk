# ForecastAPI.AdjustmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **String** | multiplier scales the value; level_shift adds a constant | 
**value** | **Number** | The factor or the offset. A multiplier must be zero or greater. | 
**fromPeriod** | **Number** | Optional 1-based inclusive start of the window; omit to start at period 1 | [optional] 
**toPeriod** | **Number** | Optional 1-based inclusive end of the window; omit to run to the horizon. Must fall within &#x60;periods&#x60;. | [optional] 



## Enum: TypeEnum


* `multiplier` (value: `"multiplier"`)

* `level_shift` (value: `"level_shift"`)




