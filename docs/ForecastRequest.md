# ForecastAPI.ForecastRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** | SKU, Product ID, or other identifier for the data series | 
**tenantContext** | **String** | Optional segmentation dimension. A series is identified by the pair identifier + tenant_context, so \&quot;mrr\&quot; on \&quot;plan-pro\&quot; and \&quot;mrr\&quot; on \&quot;plan-free\&quot; are two independent series, each with its own history and accuracy tracking. Despite the name it isn&#39;t only for multi-tenancy — use it for any slice: plan, region, store, channel, cohort, device type.  | [optional] 
**frequency** | **String** | Data frequency: - H: Hourly - D: Daily - W: Weekly - M: Monthly (end of month) - MS: Monthly (start of month) - ME: Monthly (end of month) - Q: Quarterly - Y: Yearly  | 
**startDate** | **Date** | Optional start date for the forecast | [optional] 
**dataType** | **String** | Type of data (e.g., sales, demand, inventory, web_traffic) | 
**periods** | **Number** | Number of periods to forecast | 
**model** | **String** | Which forecasting engine to use. The advanced variants, ensemble and auto provide higher accuracy at a higher usage cost than standard.  &#x60;auto&#x60; routes each identifier to whichever model has proven most accurate on that series: a new identifier starts on the ensemble, and as actuals arrive for previously forecast dates, every model&#39;s realized accuracy is scored; once one clearly wins, that identifier is routed to it. The response reports the decision in &#x60;model_info.auto_selection&#x60;. Billed at the ensemble rate whichever model it routes to.  | [optional] [default to &#39;standard&#39;]
**confidenceLevel** | **Number** | Confidence level for the prediction interval. Note that 0.80 is the widest band the foundation models (advanced-quantized, advanced-patched, ensemble) produce natively — for genuinely distinct levels beyond that, request a quantile fan via &#x60;quantiles&#x60; instead of repeating the call at several confidence levels.  | [optional] [default to 0.8]
**quantiles** | **[Number]** | Decile levels to return per period — only deciles between 0.1 and 0.9 are accepted, because those are the levels every backend produces natively; anything finer would be interpolation served under a label the model never predicted. Adds a &#x60;quantiles&#x60; object to each forecast row alongside the usual bounds. Honoured by /v2/forecast and /v2/batch/forecast (request-level default or per-series override); rejected on grouped forecasts; ignored by other endpoints sharing this request shape.  | [optional] 
**valueBounds** | [**ValueBounds**](ValueBounds.md) |  | [optional] 
**adjustments** | [**[AdjustmentsInner]**](AdjustmentsInner.md) | What-if scenario applied on top of the forecast (\&quot;assume we lose the enterprise deal\&quot;). Adjustments compose in array order — ×2 then +50 is not +50 then ×2. Each one moves the point, both bounds and any quantile fan together. Returns an &#x60;adjusted&#x60; block; the adjusted path is never stored or accuracy-tracked. Honoured by /v2/forecast and /v2/batch/forecast (request-level default or per-series override — period windows are checked against each series&#39; own horizon); rejected on grouped forecasts; ignored by other endpoints sharing this request shape.  | [optional] 
**accumulate** | [**AccumulateOptions**](AccumulateOptions.md) |  | [optional] 
**selectionMetric** | **String** | Which back-testing error metric decides the winning model when candidates are compared: - auto: combined for demand/sales/inventory, sMAPE otherwise (default) - combined: 0.6·MASE + 0.4·sMAPE — balances accuracy and trend capture - mase: Mean Absolute Scaled Error — accuracy relative to a naive forecast - smape: Symmetric Mean Absolute Percentage Error  | [optional] 
**data** | [**[ForecastRequestDataInner]**](ForecastRequestDataInner.md) | Historical time series data | 



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





## Enum: SelectionMetricEnum


* `auto` (value: `"auto"`)

* `combined` (value: `"combined"`)

* `mase` (value: `"mase"`)

* `smape` (value: `"smape"`)




