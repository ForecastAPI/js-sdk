# ForecastAPI.BatchForecastRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**series** | [**[BatchForecastSeries]**](BatchForecastSeries.md) | The series to forecast — up to 100,000 per call on a paid plan, 10 on the free tier | [optional] 
**fileKey** | **String** | Instead of inline &#x60;series&#x60; — the key returned by /v2/batch/forecast/presign, after uploading a JSON file of the same shape as this request body (an object with a &#x60;series&#x60; array). Series from a file are validated as they are streamed: an invalid series fails that series, not the whole batch.  | [optional] 
**periods** | **Number** | Default forecast horizon for series that don&#39;t set their own | [optional] [default to 6]
**frequency** | **String** | Default data frequency | [optional] 
**dataType** | **String** | Default data type | [optional] 
**model** | **String** | Default forecasting engine for series that don&#39;t set their own. &#x60;auto&#x60; routes each series independently on its own realized-accuracy scorecard. Usage is billed per series at its effective model&#39;s rate.  | [optional] [default to &#39;standard&#39;]
**confidence** | **Number** | Default confidence level for prediction intervals | [optional] [default to 0.8]
**confidenceLevel** | **Number** | Alias for &#x60;confidence&#x60; | [optional] 
**quantiles** | **[Number]** | Decile levels to return per period — only deciles between 0.1 and 0.9 are accepted, because those are the levels every backend produces natively; anything finer would be interpolation served under a label the model never predicted. Adds a &#x60;quantiles&#x60; object to each forecast row alongside the usual bounds. Honoured by /v2/forecast and /v2/batch/forecast (request-level default or per-series override); rejected on grouped forecasts; ignored by other endpoints sharing this request shape.  | [optional] 
**valueBounds** | [**ValueBounds**](ValueBounds.md) |  | [optional] 
**adjustments** | [**[AdjustmentsInner]**](AdjustmentsInner.md) | What-if scenario applied on top of the forecast (\&quot;assume we lose the enterprise deal\&quot;). Adjustments compose in array order — ×2 then +50 is not +50 then ×2. Each one moves the point, both bounds and any quantile fan together. Returns an &#x60;adjusted&#x60; block; the adjusted path is never stored or accuracy-tracked. Honoured by /v2/forecast and /v2/batch/forecast (request-level default or per-series override — period windows are checked against each series&#39; own horizon); rejected on grouped forecasts; ignored by other endpoints sharing this request shape.  | [optional] 
**accumulate** | [**AccumulateOptions**](AccumulateOptions.md) |  | [optional] 



## Enum: FrequencyEnum


* `H` (value: `"H"`)

* `D` (value: `"D"`)

* `W` (value: `"W"`)

* `M` (value: `"M"`)

* `MS` (value: `"MS"`)

* `ME` (value: `"ME"`)

* `Q` (value: `"Q"`)

* `Y` (value: `"Y"`)





## Enum: ModelEnum


* `standard` (value: `"standard"`)

* `advanced` (value: `"advanced"`)

* `advanced-quantized` (value: `"advanced-quantized"`)

* `advanced-patched` (value: `"advanced-patched"`)

* `ensemble` (value: `"ensemble"`)

* `auto` (value: `"auto"`)





## Enum: [QuantilesEnum]


* `0.1` (value: `0.1`)

* `0.2` (value: `0.2`)

* `0.3` (value: `0.3`)

* `0.4` (value: `0.4`)

* `0.5` (value: `0.5`)

* `0.6` (value: `0.6`)

* `0.7` (value: `0.7`)

* `0.8` (value: `0.8`)

* `0.9` (value: `0.9`)




