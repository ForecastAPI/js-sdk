# ForecastapiSdk.ForecastingApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v2ForecastPost**](ForecastingApi.md#v2ForecastPost) | **POST** /v2/forecast | Generate forecast for time series data



## v2ForecastPost

> ForecastResponse v2ForecastPost(forecastRequest)

Generate forecast for time series data

### Example

```javascript
import ForecastapiSdk from 'forecastapi-sdk';
let defaultClient = ForecastapiSdk.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastapiSdk.ForecastingApi();
let forecastRequest = new ForecastapiSdk.ForecastRequest(); // ForecastRequest | 
apiInstance.v2ForecastPost(forecastRequest, (error, data, response) => {
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

[**ForecastResponse**](ForecastResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

