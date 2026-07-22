# ForecastAPI.ProductInsightsApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createBatchProductInsights**](ProductInsightsApi.md#createBatchProductInsights) | **POST** /v2/batch/product-insights | Submit a batch of products for insights analysis
[**createProductInsights**](ProductInsightsApi.md#createProductInsights) | **POST** /v2/product-insights | Analyze product performance for anomalies, trends and business insights
[**getProductInsightsBatch**](ProductInsightsApi.md#getProductInsightsBatch) | **GET** /v2/batch/product-insights/{batch_id} | Poll a product insights batch for status and results



## createBatchProductInsights

> ProductInsightsBatchStatusResponse createBatchProductInsights(productInsightsBatchRequest)

Submit a batch of products for insights analysis

Analyze up to 1,000 products in one asynchronous batch; each entry is the same shape as a single &#x60;/v2/product-insights&#x60; request. Returns &#x60;202&#x60; with the batch resource to poll via &#x60;GET /v2/batch/product-insights/{batch_id}&#x60;. The optional &#x60;batch&#x60; and &#x60;parts&#x60; fields let a large batch be submitted in chunks that share one batch id. Validation is per series: if any entry fails, the whole submission is rejected with the failing entries listed by index. 

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';
let defaultClient = ForecastAPI.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastAPI.ProductInsightsApi();
let productInsightsBatchRequest = new ForecastAPI.ProductInsightsBatchRequest(); // ProductInsightsBatchRequest | 
apiInstance.createBatchProductInsights(productInsightsBatchRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **productInsightsBatchRequest** | [**ProductInsightsBatchRequest**](ProductInsightsBatchRequest.md)|  | 

### Return type

[**ProductInsightsBatchStatusResponse**](ProductInsightsBatchStatusResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createProductInsights

> ProductInsightsResponse createProductInsights(productInsightsRequest)

Analyze product performance for anomalies, trends and business insights

Analyzes a product&#39;s sales, purchase and cost-history data and returns classified insights — margin compression, sales anomalies, cost changes, lead-time reliability and more — each with severity, the metrics behind it and a recommendation. At least one of &#x60;sales&#x60;, &#x60;purchases&#x60; or &#x60;cost_history&#x60; must be provided. Analyses are stored per product, so repeat calls also return a &#x60;comparison&#x60; against the previous analysis with a new/changed/resolved breakdown. 

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';
let defaultClient = ForecastAPI.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastAPI.ProductInsightsApi();
let productInsightsRequest = new ForecastAPI.ProductInsightsRequest(); // ProductInsightsRequest | 
apiInstance.createProductInsights(productInsightsRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **productInsightsRequest** | [**ProductInsightsRequest**](ProductInsightsRequest.md)|  | 

### Return type

[**ProductInsightsResponse**](ProductInsightsResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## getProductInsightsBatch

> ProductInsightsBatchStatusResponse getProductInsightsBatch(batchId)

Poll a product insights batch for status and results

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';
let defaultClient = ForecastAPI.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastAPI.ProductInsightsApi();
let batchId = "batchId_example"; // String | The batch identifier returned on submission
apiInstance.getProductInsightsBatch(batchId).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **batchId** | **String**| The batch identifier returned on submission | 

### Return type

[**ProductInsightsBatchStatusResponse**](ProductInsightsBatchStatusResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

