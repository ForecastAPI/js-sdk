# ForecastAPI.ProductInsightsBatchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**series** | [**[ProductInsightsRequest]**](ProductInsightsRequest.md) | One entry per product, each the same shape as a single /v2/product-insights request | 
**batch** | **String** | Existing batch identifier to append this upload to, for submitting one logical batch in chunks | [optional] 
**parts** | **Number** | Total number of parts the batch will consist of, when submitting in chunks | [optional] 


