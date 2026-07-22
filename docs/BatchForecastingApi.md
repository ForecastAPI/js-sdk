# ForecastAPI.BatchForecastingApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createBatchForecast**](BatchForecastingApi.md#createBatchForecast) | **POST** /v2/batch/forecast | Submit a batch of series for forecasting
[**getBatchForecast**](BatchForecastingApi.md#getBatchForecast) | **GET** /v2/batch/forecast/{batch_id} | Poll a batch forecast for status and results
[**presignBatchForecast**](BatchForecastingApi.md#presignBatchForecast) | **POST** /v2/batch/forecast/presign | Get a presigned URL for a file-based batch upload



## createBatchForecast

> BatchForecastAccepted createBatchForecast(batchForecastRequest)

Submit a batch of series for forecasting

Forecast up to 100,000 independent series in one call (10 on the free tier), at a discount per forecast. Each series is processed independently — one failing series does not fail the others. Submission returns &#x60;202&#x60; with a &#x60;batch_id&#x60; to poll via &#x60;GET /v2/batch/forecast/{batch_id}&#x60;.  Request-level &#x60;periods&#x60;, &#x60;frequency&#x60;, &#x60;data_type&#x60;, &#x60;confidence&#x60; and the four planning parameters (&#x60;quantiles&#x60;, &#x60;value_bounds&#x60;, &#x60;adjustments&#x60;, &#x60;accumulate&#x60;) act as defaults every series inherits; any series may override any of them. &#x60;model&#x60; is request-level only.  For payloads too large to send inline, get a presigned upload URL from &#x60;POST /v2/batch/forecast/presign&#x60; and submit &#x60;file_key&#x60; instead of &#x60;series&#x60;. 

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';
let defaultClient = ForecastAPI.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastAPI.BatchForecastingApi();
let batchForecastRequest = {"series":[{"identifier":"SKU-001","data":[{"date":"2024-01-01","value":100},{"date":"2024-02-01","value":150}],"data_type":"sales","periods":3},{"identifier":"CHURN-RATE","data":[{"date":"2024-01-01","value":0.041},{"date":"2024-02-01","value":0.038}],"periods":3,"value_bounds":{"min":0,"max":1}}],"frequency":"M","confidence":0.8,"quantiles":[0.1,0.5,0.9]}; // BatchForecastRequest | 
apiInstance.createBatchForecast(batchForecastRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **batchForecastRequest** | [**BatchForecastRequest**](BatchForecastRequest.md)|  | 

### Return type

[**BatchForecastAccepted**](BatchForecastAccepted.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## getBatchForecast

> BatchForecastStatusResponse getBatchForecast(batchId)

Poll a batch forecast for status and results

Returns the batch&#39;s status, a summary once it finalises, and each series&#39; results under &#x60;results.data&#x60; — keyed by **entity id** rather than by your identifier, because one batch may contain the same identifier under several &#x60;tenant_context&#x60; values. Match series via the &#x60;identifier&#x60; and &#x60;tenant_context&#x60; echoed inside each result object. 

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';
let defaultClient = ForecastAPI.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastAPI.BatchForecastingApi();
let batchId = "batchId_example"; // String | The id returned by POST /v2/batch/forecast
apiInstance.getBatchForecast(batchId).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **batchId** | **String**| The id returned by POST /v2/batch/forecast | 

### Return type

[**BatchForecastStatusResponse**](BatchForecastStatusResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## presignBatchForecast

> BatchPresignResponse presignBatchForecast()

Get a presigned URL for a file-based batch upload

Returns a presigned URL for uploading a JSON file containing the batch request body — an object with a &#x60;series&#x60; array, the same shape as the inline &#x60;/v2/batch/forecast&#x60; request. HTTP PUT the file to &#x60;upload_url&#x60; (including any returned &#x60;headers&#x60;), then submit the batch by POSTing the returned &#x60;file_key&#x60; to &#x60;/v2/batch/forecast&#x60;. The URL is valid for 30 minutes. 

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';
let defaultClient = ForecastAPI.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastAPI.BatchForecastingApi();
apiInstance.presignBatchForecast().then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters

This endpoint does not need any parameter.

### Return type

[**BatchPresignResponse**](BatchPresignResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

