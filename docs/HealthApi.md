# ForecastAPI.HealthApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getApiRoot**](HealthApi.md#getApiRoot) | **GET** /v2 | API root endpoint
[**healthCheck**](HealthApi.md#healthCheck) | **GET** /v2/health | Health check endpoint



## getApiRoot

> GetApiRoot200Response getApiRoot()

API root endpoint

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';

let apiInstance = new ForecastAPI.HealthApi();
apiInstance.getApiRoot().then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters

This endpoint does not need any parameter.

### Return type

[**GetApiRoot200Response**](GetApiRoot200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## healthCheck

> HealthCheck200Response healthCheck()

Health check endpoint

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';

let apiInstance = new ForecastAPI.HealthApi();
apiInstance.healthCheck().then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters

This endpoint does not need any parameter.

### Return type

[**HealthCheck200Response**](HealthCheck200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

