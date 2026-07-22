# ForecastAPI.AccumulateOptions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**decay** | **Number** | Per-period survival factor — 0.95 means 5% attrition each period | [optional] [default to 1.0]
**discountRate** | **Number** | Annual discount rate, converted to the series frequency (a 10% annual rate on monthly periods discounts period 2 by 1.10^(-1/12), not by 1.10) | [optional] [default to 0]
**correlation** | **Number** | How correlated the per-period errors are assumed to be; controls only the width of the total&#39;s band. 0 &#x3D; independent periods (measurably too narrow), 1 &#x3D; sum of the bounds (conservative envelope). The default 0.5 was measured across the benchmark suite; a value you supply is your assumption and is never labelled measured.  | [optional] [default to 0.5]


