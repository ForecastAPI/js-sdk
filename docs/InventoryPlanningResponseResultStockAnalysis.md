# ForecastapiSdk.InventoryPlanningResponseResultStockAnalysis

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**daysOfCoverage** | **Number** | Number of days current stock will last | [optional] 
**stockoutRisk** | **Number** | Risk of stockout (0-1, where 1 is certain stockout) | [optional] 
**nextOrderDate** | **Date** | Recommended date for next order | [optional] 
**dailyDemandRate** | **Number** | Average daily demand rate | [optional] 
**stockStatus** | **String** | Current stock status assessment | [optional] 



## Enum: StockStatusEnum


* `critical` (value: `"critical"`)

* `reorder_needed` (value: `"reorder_needed"`)

* `low` (value: `"low"`)

* `adequate` (value: `"adequate"`)




