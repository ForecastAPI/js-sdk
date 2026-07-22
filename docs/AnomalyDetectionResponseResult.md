# ForecastAPI.AnomalyDetectionResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**anomalies** | [**[AnomalyDetectionResponseResultAnomaliesInner]**](AnomalyDetectionResponseResultAnomaliesInner.md) | Detected anomalies, most severe first | [optional] 
**analysis** | [**AnomalyDetectionResponseResultAnalysis**](AnomalyDetectionResponseResultAnalysis.md) |  | [optional] 
**alternatives** | **[{String: Object}]** | Other suitable methods (present on auto selection) | [optional] 
**statistics** | **{String: Object}** | Method statistics (present when a method was named in the request) | [optional] 
**interpretation** | **{String: Object}** | Human-readable interpretation (present when a method was named in the request) | [optional] 


