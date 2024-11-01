# ForecastapiSdk.HealthApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v2Get**](HealthApi.md#v2Get) | **GET** /v2 | API root endpoint
[**v2HealthGet**](HealthApi.md#v2HealthGet) | **GET** /v2/health | Health check endpoint



## v2Get

> V2Get200Response v2Get()

API root endpoint

### Example

```javascript
import ForecastapiSdk from 'forecastapi-sdk';

let apiInstance = new ForecastapiSdk.HealthApi();
apiInstance.v2Get((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**V2Get200Response**](V2Get200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## v2HealthGet

> V2HealthGet200Response v2HealthGet()

Health check endpoint

### Example

```javascript
import ForecastapiSdk from 'forecastapi-sdk';

let apiInstance = new ForecastapiSdk.HealthApi();
apiInstance.v2HealthGet((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**V2HealthGet200Response**](V2HealthGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

