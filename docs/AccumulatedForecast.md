# ForecastAPI.AccumulatedForecast

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **Number** | Σ (value × survival × discount) over the horizon. Null when a period lacks a usable point forecast (see &#x60;total_reason&#x60;). | [optional] 
**totalReason** | **String** | Why &#x60;total&#x60; is null; null when the total is usable | [optional] 
**lower** | **Number** | Lower bound of the total under the stated correlation assumption. Null with an &#x60;interval_reason&#x60; when any period lacks a band or its coverage is unknown — rather than a band built from a partial set of variances.  | [optional] 
**upper** | **Number** |  | [optional] 
**intervalReason** | **String** | Why the total&#39;s band is absent; null when the band is present | [optional] 
**confidenceLevel** | **Number** | Coverage the total&#39;s band targets | [optional] 
**path** | **String** | Which path was accumulated — &#x60;adjusted&#x60; when &#x60;adjustments&#x60; was also sent, otherwise &#x60;baseline&#x60; | [optional] 
**assumptions** | [**AccumulatedForecastAssumptions**](AccumulatedForecastAssumptions.md) |  | [optional] 
**byPeriod** | [**[AccumulatedForecastByPeriodInner]**](AccumulatedForecastByPeriodInner.md) | Running accumulation per period — &#x60;cumulative&#x60; through period L is the number a lead-time/safety-stock calculation reads | [optional] 



## Enum: PathEnum


* `baseline` (value: `"baseline"`)

* `adjusted` (value: `"adjusted"`)




