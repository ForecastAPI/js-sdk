# ForecastAPI.AnomalyDetectionApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**detectAnomalies**](AnomalyDetectionApi.md#detectAnomalies) | **POST** /v2/detect-anomalies | Detect anomalies in time series data



## detectAnomalies

> AnomalyDetectionResponse detectAnomalies(anomalyDetectionRequest)

Detect anomalies in time series data

Detects anomalies using statistical methods — z-score, IQR or seasonal — and automatically selects the best method for the data&#39;s characteristics unless one is named in &#x60;anomaly_settings.method&#x60;. Returns each anomalous point with its expected range, severity and type, plus an analysis of how the method was chosen. 

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';
let defaultClient = ForecastAPI.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastAPI.AnomalyDetectionApi();
let anomalyDetectionRequest = new ForecastAPI.AnomalyDetectionRequest(); // AnomalyDetectionRequest | 
apiInstance.detectAnomalies(anomalyDetectionRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **anomalyDetectionRequest** | [**AnomalyDetectionRequest**](AnomalyDetectionRequest.md)|  | 

### Return type

[**AnomalyDetectionResponse**](AnomalyDetectionResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

