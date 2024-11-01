# ForecastapiSdk.InventoryPlanningResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** | Product identifier from the request | [optional] 
**currentStock** | **Number** | Current stock level | [optional] 
**minimumStock** | **Number** | Minimum stock level to maintain | [optional] 
**reorderPoint** | **Number** | Recommended reorder point for optimal supplier | [optional] 
**safetyStock** | **Number** | Calculated safety stock for optimal supplier | [optional] 
**suppliers** | [**[InventoryPlanningResponseResultSuppliersInner]**](InventoryPlanningResponseResultSuppliersInner.md) | Analysis and recommendations for each supplier | [optional] 
**stockAnalysis** | [**InventoryPlanningResponseResultStockAnalysis**](InventoryPlanningResponseResultStockAnalysis.md) |  | [optional] 
**forecastData** | [**[InventoryPlanningResponseResultForecastDataInner]**](InventoryPlanningResponseResultForecastDataInner.md) | Underlying forecast data used for planning | [optional] 


