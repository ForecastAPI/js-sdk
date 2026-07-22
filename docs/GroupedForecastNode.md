# ForecastAPI.GroupedForecastNode

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** | The measure — the same for every node | [optional] 
**segment** | **{String: Object}** | The dimension values this node covers — empty for the total, all declared dimensions for a leaf | [optional] 
**level** | **Number** | Depth in the tree; 0 is the total | [optional] 
**isLeaf** | **Boolean** |  | [optional] 
**parent** | **String** | Segment key of the parent node; null for the total | [optional] 
**children** | **[String]** | Segment keys of the children; empty for leaves | [optional] 
**forecasts** | [**[ForecastPeriod]**](ForecastPeriod.md) | The reconciled path — this is what is stored and accuracy-tracked per node | [optional] 
**modelInfo** | **{String: Object}** | Method and reconciliation details for this node. With min_trace, the node&#39;s unreconciled path is reported under &#x60;reconciliation.base_forecast&#x60;. When an aggregate band cannot be built honestly (a child&#39;s band coverage is unknown), the band is omitted and &#x60;reconciliation.interval_reason&#x60; states why.  | [optional] 


