# ForecastapiSdk.InventoryPlanningApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v2InventoryPlanningPost**](InventoryPlanningApi.md#v2InventoryPlanningPost) | **POST** /v2/inventory-planning | Generate comprehensive inventory planning recommendations



## v2InventoryPlanningPost

> InventoryPlanningResponse v2InventoryPlanningPost(inventoryPlanningRequest)

Generate comprehensive inventory planning recommendations

Generate inventory forecasts with supplier recommendations, reorder points, safety stock calculations, and comprehensive stock analysis. This endpoint combines time series forecasting with inventory optimization to provide actionable recommendations for stock management and procurement.  **Key Features:** - Automatic forecasting method selection based on demand patterns - Multi-supplier cost and lead time optimization - Safety stock calculation with configurable service levels - Reorder point recommendations with minimum order quantity considerations - Stock analysis including stockout risk and days of coverage - Real-time supplier performance evaluation 

### Example

```javascript
import ForecastapiSdk from 'forecastapi-sdk';
let defaultClient = ForecastapiSdk.ApiClient.instance;
// Configure API key authorization: apiKey
let apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

let apiInstance = new ForecastapiSdk.InventoryPlanningApi();
let inventoryPlanningRequest = {"identifier":"SKU-12345","frequency":"M","start_date":"2024-01-01","periods":6,"enable_intelligent_aggregation":true,"data":[{"date":"2023-01-01","value":100},{"date":"2023-02-01","value":120},{"date":"2023-03-01","value":95},{"date":"2023-04-01","value":130},{"date":"2023-05-01","value":110}],"inventory_settings":{"current_stock":250,"minimum_stock":50,"service_level":0.95,"suppliers":[{"identifier":"supplier-a","lead_time_days":14,"minimum_order_quantity":100,"cost_per_unit":12.5,"reliability_score":0.98}]}}; // InventoryPlanningRequest | 
apiInstance.v2InventoryPlanningPost(inventoryPlanningRequest, (error, data, response) => {
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
 **inventoryPlanningRequest** | [**InventoryPlanningRequest**](InventoryPlanningRequest.md)|  | 

### Return type

[**InventoryPlanningResponse**](InventoryPlanningResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

