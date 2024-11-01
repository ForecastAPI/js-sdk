# ForecastapiSdk.TrafficForecastingResponseResultCapacityAnalysis

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currentCapacity** | **Number** | Current infrastructure capacity | [optional] 
**utilizationPeriods** | [**[TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner]**](TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner.md) | Capacity utilization for each forecast period | [optional] 
**overCapacityPeriods** | **Number** | Number of periods exceeding capacity | [optional] 
**criticalPeriods** | **Number** | Number of periods above 90% utilization | [optional] 
**forecastDurationMinutes** | **Number** | Total forecast duration in minutes | [optional] 
**nextCapacityBreach** | **Date** | Date when capacity will be breached | [optional] 
**capacityEfficiency** | **Number** | Efficiency score (0-100, optimal around 75% utilization) | [optional] 


