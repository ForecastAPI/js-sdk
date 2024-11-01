# ForecastapiSdk.InventoryPlanningRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** | SKU, Product ID, or other identifier for the inventory item | 
**frequency** | **String** | Data frequency for forecasting: - D: Daily - W: Weekly - M: Monthly (end of month) - MS: Monthly (start of month) - ME: Monthly (end of month) - Q: Quarterly - Y: Yearly  | 
**startDate** | **Date** | Optional start date for the forecast period | [optional] 
**periods** | **Number** | Number of periods to forecast ahead | 
**enableIntelligentAggregation** | **Boolean** | Enable intelligent data aggregation for improved forecasting | [optional] 
**confidenceLevel** | **Number** | Confidence level for forecast intervals (default 0.95) | [optional] 
**data** | [**[InventoryPlanningRequestDataInner]**](InventoryPlanningRequestDataInner.md) | Historical demand/sales data for forecasting | 
**inventorySettings** | [**InventoryPlanningRequestInventorySettings**](InventoryPlanningRequestInventorySettings.md) |  | 



## Enum: FrequencyEnum


* `D` (value: `"D"`)

* `W` (value: `"W"`)

* `M` (value: `"M"`)

* `MS` (value: `"MS"`)

* `ME` (value: `"ME"`)

* `Q` (value: `"Q"`)

* `Y` (value: `"Y"`)




