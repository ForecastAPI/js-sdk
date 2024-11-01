# ForecastapiSdk.DefaultApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1AnyGet**](DefaultApi.md#v1AnyGet) | **GET** /v1/{any} | Deprecated v1 endpoints



## v1AnyGet

> v1AnyGet(any)

Deprecated v1 endpoints

### Example

```javascript
import ForecastapiSdk from 'forecastapi-sdk';

let apiInstance = new ForecastapiSdk.DefaultApi();
let any = "any_example"; // String | 
apiInstance.v1AnyGet(any, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
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

