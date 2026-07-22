# ForecastAPI.DefaultApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deprecatedV1**](DefaultApi.md#deprecatedV1) | **GET** /v1/{any} | Deprecated v1 endpoints



## deprecatedV1

> deprecatedV1(any)

Deprecated v1 endpoints

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';

let apiInstance = new ForecastAPI.DefaultApi();
let any = "any_example"; // String | 
apiInstance.deprecatedV1(any).then(() => {
  console.log('API called successfully.');
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **any** | **String**|  | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

