# ForecastapiSdk.AnalysisApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v2AnalyzePost**](AnalysisApi.md#v2AnalyzePost) | **POST** /v2/analyze | Analyze time series data without generating forecast



## v2AnalyzePost

> AnalysisResponse v2AnalyzePost(forecastRequest)

Analyze time series data without generating forecast

### Example

```javascript
import ForecastapiSdk from 'forecastapi-sdk';
let defaultClient = ForecastapiSdk.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastapiSdk.AnalysisApi();
let forecastRequest = new ForecastapiSdk.ForecastRequest(); // ForecastRequest | 
apiInstance.v2AnalyzePost(forecastRequest, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
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

