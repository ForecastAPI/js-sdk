# ForecastAPI.GroupedForecastingApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createGroupedForecast**](GroupedForecastingApi.md#createGroupedForecast) | **POST** /v2/forecast/grouped | Submit a grouped (hierarchical) forecast with reconciliation
[**getGroupedForecast**](GroupedForecastingApi.md#getGroupedForecast) | **GET** /v2/forecast/grouped/{grouped_forecast_id} | Poll a grouped forecast for status and results



## createGroupedForecast

> GroupedForecastAccepted createGroupedForecast(groupedForecastRequest)

Submit a grouped (hierarchical) forecast with reconciliation

Forecast a set of related series that roll up to a total — MRR by plan and region, demand by warehouse, revenue by category — and get back one coherent result: every parent equals the sum of its children, in every period, at every level.  You send only the **leaves** of the hierarchy (every combination of the declared dimensions, each with its own history). The API derives every aggregate level and the grand total by summing the leaf histories, forecasts the nodes, reconciles them to coherence, and stores each node as its own entity with independently tracked accuracy.  Processing is **asynchronous**: submission returns &#x60;202&#x60; with an id to poll via &#x60;GET /v2/forecast/grouped/{grouped_forecast_id}&#x60;. The run executes in the background as one all-or-nothing job — a hierarchy is one coherent answer, so there is no partial success. If any node cannot be forecast, the run fails with the reason rather than returning numbers that don&#39;t add up.  If you just want independent forecasts per slice — no coherent roll-up — the batch endpoint with per-series identifiers or &#x60;tenant_context&#x60; is simpler and tolerates per-series failure. 

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';
let defaultClient = ForecastAPI.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastAPI.GroupedForecastingApi();
let groupedForecastRequest = {"identifier":"mrr","hierarchy":["region","plan"],"reconciliation":"bottom_up","frequency":"M","periods":6,"data_type":"revenue","series":[{"segment":{"region":"eu","plan":"pro"},"data":[{"date":"2024-01-01","value":42000},{"date":"2024-02-01","value":43800}]},{"segment":{"region":"eu","plan":"free"},"data":[{"date":"2024-01-01","value":3100},{"date":"2024-02-01","value":3300}]},{"segment":{"region":"us","plan":"pro"},"data":[{"date":"2024-01-01","value":61000},{"date":"2024-02-01","value":62500}]}]}; // GroupedForecastRequest | 
apiInstance.createGroupedForecast(groupedForecastRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupedForecastRequest** | [**GroupedForecastRequest**](GroupedForecastRequest.md)|  | 

### Return type

[**GroupedForecastAccepted**](GroupedForecastAccepted.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## getGroupedForecast

> GroupedForecastStatusResponse getGroupedForecast(groupedForecastId)

Poll a grouped forecast for status and results

Returns the run&#39;s status. Once &#x60;completed&#x60;, &#x60;results&#x60; carries a node map keyed by segment (&#x60;total&#x60;, &#x60;region&#x3D;eu&#x60;, &#x60;plan&#x3D;pro|region&#x3D;eu&#x60;, …) — every node with its own forecast rows, its place in the tree, and the reconciliation details. If the run &#x60;failed&#x60;, &#x60;error&#x60; carries the reason and &#x60;results&#x60; stays null. 

### Example

```javascript
import ForecastAPI from 'forecastapi-sdk';
let defaultClient = ForecastAPI.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastAPI.GroupedForecastingApi();
let groupedForecastId = "k3n9x2m4p8q1w5r7"; // String | The id returned by POST /v2/forecast/grouped
apiInstance.getGroupedForecast(groupedForecastId).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupedForecastId** | **String**| The id returned by POST /v2/forecast/grouped | 

### Return type

[**GroupedForecastStatusResponse**](GroupedForecastStatusResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

