# ForecastapiSdk.TrafficForecastingResponseResultTrafficAlertsAlertsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **String** | Type of alert | [optional] 
**severity** | **String** | Alert severity | [optional] 
**period** | **Number** | Period number where alert occurs | [optional] 
**date** | **Date** | Date/time of the alert | [optional] 
**predictedTraffic** | **Number** | Predicted traffic value | [optional] 
**baselineTraffic** | **Number** | Baseline traffic (for spikes) | [optional] 
**increaseFactor** | **Number** | Traffic increase factor (for spikes) | [optional] 
**zScore** | **Number** | Z-score for anomaly detection | [optional] 
**message** | **String** | Alert message | [optional] 



## Enum: TypeEnum


* `traffic_spike` (value: `"traffic_spike"`)

* `anomaly` (value: `"anomaly"`)





## Enum: SeverityEnum


* `high` (value: `"high"`)

* `medium` (value: `"medium"`)




