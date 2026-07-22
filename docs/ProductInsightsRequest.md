# ForecastAPI.ProductInsightsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **String** | Product identifier | 
**tenantContext** | **String** |  | [optional] 
**productName** | **String** |  | [optional] 
**productGroupId** | **String** |  | [optional] 
**baseCurrency** | **String** | ISO 4217 currency the analysis reports in | [optional] 
**baselinePeriodDays** | [**ProductInsightsRequestBaselinePeriodDays**](ProductInsightsRequestBaselinePeriodDays.md) |  | [optional] 
**locale** | **String** | Locale for insight texts | [optional] [default to &#39;en&#39;]
**sales** | [**[ProductInsightsRequestSalesInner]**](ProductInsightsRequestSalesInner.md) |  | [optional] 
**purchases** | [**[ProductInsightsRequestPurchasesInner]**](ProductInsightsRequestPurchasesInner.md) |  | [optional] 
**costHistory** | [**[ProductInsightsRequestCostHistoryInner]**](ProductInsightsRequestCostHistoryInner.md) |  | [optional] 
**insightSettings** | [**ProductInsightsRequestInsightSettings**](ProductInsightsRequestInsightSettings.md) |  | [optional] 


