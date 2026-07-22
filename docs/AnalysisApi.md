# ForecastAPI.AnalysisApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**analyzeTimeSeries**](AnalysisApi.md#analyzeTimeSeries) | **POST** /v2/analyze | Analyze time series data without generating forecast



## analyzeTimeSeries

> AnalysisResponse analyzeTimeSeries(forecastRequest)

Analyze time series data without generating forecast

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';
let defaultClient = ForecastAPI.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastAPI.AnalysisApi();
let forecastRequest = new ForecastAPI.ForecastRequest(); // ForecastRequest | 
apiInstance.analyzeTimeSeries(forecastRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **forecastRequest** | [**ForecastRequest**](ForecastRequest.md)|  | 

### Return type

[**AnalysisResponse**](AnalysisResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

