# forecastapi-sdk

ForecastapiSdk - JavaScript client for forecastapi-sdk
Time series forecasting service with multiple algorithms and automatic method selection.


## Installation

### npm

```shell
npm install forecastapi-sdk 
```

## Getting Started

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var ForecastapiSdk = require('forecastapi-sdk');

var defaultClient = ForecastapiSdk.ApiClient.instance;
// Configure API key authorization: apiKey
var apiKey = defaultClient.authentications['apiKey'];
apiKey.apiKey = "YOUR API KEY"
apiKey.apiKeyPrefix['Authorization'] = "Bearer"

var api = new ForecastapiSdk.AnalysisApi()
var forecastRequest = new ForecastapiSdk.ForecastRequest(); // {ForecastRequest} 
var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.v2AnalyzePost(forecastRequest, callback);

```

## Documentation for API Endpoints

All URIs are relative to *https://forecastapi.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ForecastapiSdk.AnalysisApi* | [**v2AnalyzePost**](docs/AnalysisApi.md#v2AnalyzePost) | **POST** /v2/analyze | Analyze time series data without generating forecast
*ForecastapiSdk.DefaultApi* | [**v1AnyGet**](docs/DefaultApi.md#v1AnyGet) | **GET** /v1/{any} | Deprecated v1 endpoints
*ForecastapiSdk.ForecastingApi* | [**v2ForecastPost**](docs/ForecastingApi.md#v2ForecastPost) | **POST** /v2/forecast | Generate forecast for time series data
*ForecastapiSdk.HealthApi* | [**v2Get**](docs/HealthApi.md#v2Get) | **GET** /v2 | API root endpoint
*ForecastapiSdk.HealthApi* | [**v2HealthGet**](docs/HealthApi.md#v2HealthGet) | **GET** /v2/health | Health check endpoint
*ForecastapiSdk.InventoryPlanningApi* | [**v2InventoryPlanningPost**](docs/InventoryPlanningApi.md#v2InventoryPlanningPost) | **POST** /v2/inventory-planning | Generate comprehensive inventory planning recommendations
*ForecastapiSdk.TrafficForecastingApi* | [**v2TrafficForecastingPost**](docs/TrafficForecastingApi.md#v2TrafficForecastingPost) | **POST** /v2/traffic-forecasting | Generate traffic forecasting with infrastructure scaling recommendations


## Documentation for Models

 - [ForecastapiSdk.AnalysisResponse](docs/AnalysisResponse.md)
 - [ForecastapiSdk.AnalysisResponseMeta](docs/AnalysisResponseMeta.md)
 - [ForecastapiSdk.AnalysisResponseMetaTiming](docs/AnalysisResponseMetaTiming.md)
 - [ForecastapiSdk.AnalysisResponseResult](docs/AnalysisResponseResult.md)
 - [ForecastapiSdk.AnalysisResponseResultCharacteristics](docs/AnalysisResponseResultCharacteristics.md)
 - [ForecastapiSdk.ErrorResponse](docs/ErrorResponse.md)
 - [ForecastapiSdk.ForecastRequest](docs/ForecastRequest.md)
 - [ForecastapiSdk.ForecastRequestDataInner](docs/ForecastRequestDataInner.md)
 - [ForecastapiSdk.ForecastResponse](docs/ForecastResponse.md)
 - [ForecastapiSdk.ForecastResponseMeta](docs/ForecastResponseMeta.md)
 - [ForecastapiSdk.ForecastResponseMetaTiming](docs/ForecastResponseMetaTiming.md)
 - [ForecastapiSdk.ForecastResponseResult](docs/ForecastResponseResult.md)
 - [ForecastapiSdk.InventoryPlanningRequest](docs/InventoryPlanningRequest.md)
 - [ForecastapiSdk.InventoryPlanningRequestDataInner](docs/InventoryPlanningRequestDataInner.md)
 - [ForecastapiSdk.InventoryPlanningRequestInventorySettings](docs/InventoryPlanningRequestInventorySettings.md)
 - [ForecastapiSdk.InventoryPlanningRequestInventorySettingsSuppliersInner](docs/InventoryPlanningRequestInventorySettingsSuppliersInner.md)
 - [ForecastapiSdk.InventoryPlanningResponse](docs/InventoryPlanningResponse.md)
 - [ForecastapiSdk.InventoryPlanningResponseMeta](docs/InventoryPlanningResponseMeta.md)
 - [ForecastapiSdk.InventoryPlanningResponseMetaTiming](docs/InventoryPlanningResponseMetaTiming.md)
 - [ForecastapiSdk.InventoryPlanningResponseResult](docs/InventoryPlanningResponseResult.md)
 - [ForecastapiSdk.InventoryPlanningResponseResultForecastDataInner](docs/InventoryPlanningResponseResultForecastDataInner.md)
 - [ForecastapiSdk.InventoryPlanningResponseResultStockAnalysis](docs/InventoryPlanningResponseResultStockAnalysis.md)
 - [ForecastapiSdk.InventoryPlanningResponseResultSuppliersInner](docs/InventoryPlanningResponseResultSuppliersInner.md)
 - [ForecastapiSdk.TrafficForecastingRequest](docs/TrafficForecastingRequest.md)
 - [ForecastapiSdk.TrafficForecastingRequestDataInner](docs/TrafficForecastingRequestDataInner.md)
 - [ForecastapiSdk.TrafficForecastingRequestTrafficSettings](docs/TrafficForecastingRequestTrafficSettings.md)
 - [ForecastapiSdk.TrafficForecastingResponse](docs/TrafficForecastingResponse.md)
 - [ForecastapiSdk.TrafficForecastingResponseMeta](docs/TrafficForecastingResponseMeta.md)
 - [ForecastapiSdk.TrafficForecastingResponseMetaTiming](docs/TrafficForecastingResponseMetaTiming.md)
 - [ForecastapiSdk.TrafficForecastingResponseResult](docs/TrafficForecastingResponseResult.md)
 - [ForecastapiSdk.TrafficForecastingResponseResultCapacityAnalysis](docs/TrafficForecastingResponseResultCapacityAnalysis.md)
 - [ForecastapiSdk.TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner](docs/TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner.md)
 - [ForecastapiSdk.TrafficForecastingResponseResultCostOptimization](docs/TrafficForecastingResponseResultCostOptimization.md)
 - [ForecastapiSdk.TrafficForecastingResponseResultCostOptimizationCostBreakdown](docs/TrafficForecastingResponseResultCostOptimizationCostBreakdown.md)
 - [ForecastapiSdk.TrafficForecastingResponseResultCostOptimizationRecommendationsInner](docs/TrafficForecastingResponseResultCostOptimizationRecommendationsInner.md)
 - [ForecastapiSdk.TrafficForecastingResponseResultForecastDataInner](docs/TrafficForecastingResponseResultForecastDataInner.md)
 - [ForecastapiSdk.TrafficForecastingResponseResultScalingRecommendations](docs/TrafficForecastingResponseResultScalingRecommendations.md)
 - [ForecastapiSdk.TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner](docs/TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner.md)
 - [ForecastapiSdk.TrafficForecastingResponseResultTrafficAlerts](docs/TrafficForecastingResponseResultTrafficAlerts.md)
 - [ForecastapiSdk.TrafficForecastingResponseResultTrafficAlertsAlertsInner](docs/TrafficForecastingResponseResultTrafficAlertsAlertsInner.md)
 - [ForecastapiSdk.V1AnyGet404Response](docs/V1AnyGet404Response.md)
 - [ForecastapiSdk.V2ForecastPost400Response](docs/V2ForecastPost400Response.md)
 - [ForecastapiSdk.V2Get200Response](docs/V2Get200Response.md)
 - [ForecastapiSdk.V2HealthGet200Response](docs/V2HealthGet200Response.md)
 - [ForecastapiSdk.V2InventoryPlanningPost400Response](docs/V2InventoryPlanningPost400Response.md)
 - [ForecastapiSdk.V2InventoryPlanningPost500Response](docs/V2InventoryPlanningPost500Response.md)
 - [ForecastapiSdk.V2TrafficForecastingPost500Response](docs/V2TrafficForecastingPost500Response.md)
 - [ForecastapiSdk.ValidationErrorResponse](docs/ValidationErrorResponse.md)


## Documentation for Authorization


Authentication schemes defined for the API:
### apiKey


- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header

