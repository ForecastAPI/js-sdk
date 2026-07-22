# ForecastAPI.ForecastPeriod

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | **Number** | 1-based forecast period number | [optional] 
**date** | **Date** | Date of this forecast period | [optional] 
**forecast** | **Number** | Point forecast for this period | [optional] 
**lower** | **Number** | Lower prediction bound at the requested confidence level | [optional] 
**upper** | **Number** | Upper prediction bound at the requested confidence level | [optional] 
**quantiles** | **{String: Number}** | Present only when &#x60;quantiles&#x60; was requested — the forecast at each requested decile level for this period | [optional] 


