# ForecastAPI.TrafficForecastingApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createTrafficForecast**](TrafficForecastingApi.md#createTrafficForecast) | **POST** /v2/traffic-forecasting | Generate traffic forecasting with infrastructure scaling recommendations



## createTrafficForecast

> TrafficForecastingResponse createTrafficForecast(trafficForecastingRequest)

Generate traffic forecasting with infrastructure scaling recommendations

Generate comprehensive traffic forecasts with infrastructure scaling recommendations, capacity analysis, cost optimization, and traffic anomaly alerts. This endpoint is designed for web applications, APIs, and infrastructure teams to predict traffic patterns and optimize resource allocation.  **Key Features:** - Intelligent traffic pattern forecasting with multiple algorithms - Infrastructure scaling recommendations (scale up/down/maintain) - Real-time capacity utilization analysis - Traffic spike and anomaly detection alerts - Cost optimization recommendations with potential savings - Auto-scaling benefit analysis - Support for various time frequencies (minute, hourly, daily, etc.) 

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';
let defaultClient = ForecastAPI.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastAPI.TrafficForecastingApi();
let trafficForecastingRequest = {"identifier":"api-endpoint-users","frequency":"H","start_date":"2024-01-01","periods":24,"enable_intelligent_aggregation":true,"data":[{"date":"2023-12-01 00:00:00","value":1200},{"date":"2023-12-01 01:00:00","value":800},{"date":"2023-12-01 02:00:00","value":600},{"date":"2023-12-01 03:00:00","value":500},{"date":"2023-12-01 04:00:00","value":450}],"traffic_settings":{"current_capacity":2000,"baseline_traffic":1000,"scaling_buffer":0.2,"scale_up_threshold":0.8,"scale_down_threshold":0.3,"alert_threshold":1.5,"anomaly_threshold":3.0,"cost_per_unit":0.01,"fixed_cost_per_capacity":0.1,"base_scaling_time":5,"enable_auto_scaling":false}}; // TrafficForecastingRequest | 
apiInstance.createTrafficForecast(trafficForecastingRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **trafficForecastingRequest** | [**TrafficForecastingRequest**](TrafficForecastingRequest.md)|  | 

### Return type

[**TrafficForecastingResponse**](TrafficForecastingResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

