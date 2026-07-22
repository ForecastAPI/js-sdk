# ForecastAPI.GroupedForecastRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** | Names the measure being forecast (e.g. \&quot;mrr\&quot;). The hierarchy&#39;s total is stored under this identifier exactly like a plain /v2/forecast for it — the total of the hierarchy IS the measure.  | 
**tenantContext** | **String** | Optional tenant scope, independent of segment — tenancy keeps meaning \&quot;whose data is this\&quot;, segment means \&quot;which slice\&quot;.  | [optional] 
**hierarchy** | **[String]** | The dimensions of the hierarchy, outermost first. Each series&#39; segment must name exactly these dimensions. | 
**reconciliation** | **String** | - bottom_up (default): only the leaves are forecast; every aggregate is the   exact sum of its children. Fast and cheap; best when leaf histories are   substantial enough to forecast well on their own. - min_trace: every node — aggregates included — is forecast, then MinTrace   optimally redistributes the disagreement between levels into a coherent set.   Costs one forecast per node, but lets the usually-smoother aggregate series   inform the result, which tends to help when leaves are short or noisy.  top_down is not supported and is rejected by name.  | [optional] [default to &#39;bottom_up&#39;]
**correlation** | **Number** | bottom_up only — the assumed correlation between sibling errors when building aggregate confidence bands. 0 &#x3D; independent siblings, 1 &#x3D; perfectly correlated (equivalent to summing the bounds). Echoed back in the response and never labelled as measured.  | [optional] [default to 0.5]
**frequency** | **String** | Data frequency, shared by every series in the hierarchy | 
**periods** | **Number** | Number of periods to forecast, shared by every node | 
**dataType** | **String** | Type of data (e.g., sales, demand, revenue). Sales-family types get non-negative reconciliation treatment. | [optional] [default to &#39;sales&#39;]
**model** | **String** | Forecasting engine used for every node | [optional] [default to &#39;standard&#39;]
**confidence** | **Number** | Confidence level for prediction intervals, shared by every node | [optional] [default to 0.8]
**confidenceLevel** | **Number** | Alias for &#x60;confidence&#x60;; if both are sent, &#x60;confidence&#x60; wins | [optional] 
**series** | [**[GroupedForecastSeries]**](GroupedForecastSeries.md) | The leaves of the hierarchy — one entry per combination of dimension values, each combination exactly once. Up to 200 series on a paid plan, 10 on the free tier. Aggregate levels are derived by the API and must not be sent.  | 



## Enum: ReconciliationEnum


* `bottom_up` (value: `"bottom_up"`)

* `min_trace` (value: `"min_trace"`)





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




