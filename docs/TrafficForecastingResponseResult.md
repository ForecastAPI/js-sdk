# ForecastapiSdk.TrafficForecastingResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | **String** | Metric identifier from the request | [optional] 
**currentCapacity** | **Number** | Current infrastructure capacity | [optional] 
**baselineTraffic** | **Number** | Baseline traffic level | [optional] 
**scalingRecommendations** | [**TrafficForecastingResponseResultScalingRecommendations**](TrafficForecastingResponseResultScalingRecommendations.md) |  | [optional] 
**capacityAnalysis** | [**TrafficForecastingResponseResultCapacityAnalysis**](TrafficForecastingResponseResultCapacityAnalysis.md) |  | [optional] 
**trafficAlerts** | [**TrafficForecastingResponseResultTrafficAlerts**](TrafficForecastingResponseResultTrafficAlerts.md) |  | [optional] 
**costOptimization** | [**TrafficForecastingResponseResultCostOptimization**](TrafficForecastingResponseResultCostOptimization.md) |  | [optional] 
**forecastData** | [**[TrafficForecastingResponseResultForecastDataInner]**](TrafficForecastingResponseResultForecastDataInner.md) | Underlying forecast data used for analysis | [optional] 


