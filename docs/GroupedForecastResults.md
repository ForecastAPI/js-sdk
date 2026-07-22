# ForecastAPI.GroupedForecastResults

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** |  | [optional] 
**tenantContext** | **String** |  | [optional] 
**hierarchy** | **[String]** |  | [optional] 
**reconciliation** | [**GroupedForecastResultsReconciliation**](GroupedForecastResultsReconciliation.md) |  | [optional] 
**confidenceLevel** | **Number** |  | [optional] 
**nodeCount** | **Number** |  | [optional] 
**nodes** | [**{String: GroupedForecastNode}**](GroupedForecastNode.md) | Every node of the hierarchy, keyed by segment key: &#x60;total&#x60; for the root, then e.g. &#x60;region&#x3D;eu&#x60; for aggregates and &#x60;plan&#x3D;pro|region&#x3D;eu&#x60; for leaves. Every parent equals the sum of its children in every period.  | [optional] 


