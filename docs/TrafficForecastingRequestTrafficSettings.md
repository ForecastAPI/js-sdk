# ForecastAPI.TrafficForecastingRequestTrafficSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currentCapacity** | **Number** | Current infrastructure capacity (requests, users, etc.) | 
**baselineTraffic** | **Number** | Normal/expected traffic level for comparison | 
**scalingBuffer** | **Number** | Buffer percentage for scaling decisions (default 0.2 &#x3D; 20%) | [optional] 
**scaleUpThreshold** | **Number** | Utilization threshold to trigger scale up (default 0.8 &#x3D; 80%) | [optional] 
**scaleDownThreshold** | **Number** | Utilization threshold to trigger scale down (default 0.3 &#x3D; 30%) | [optional] 
**alertThreshold** | **Number** | Traffic spike alert threshold as multiplier of baseline (default 1.5 &#x3D; 150%) | [optional] 
**anomalyThreshold** | **Number** | Standard deviations for anomaly detection (default 3.0) | [optional] 
**costPerUnit** | **Number** | Variable cost per traffic unit (default 0.01) | [optional] 
**fixedCostPerCapacity** | **Number** | Fixed cost per capacity unit (default 0.1) | [optional] 
**baseScalingTime** | **Number** | Base time in minutes for scaling operations (default 5) | [optional] 
**enableAutoScaling** | **Boolean** | Whether auto-scaling is currently enabled (default false) | [optional] 


