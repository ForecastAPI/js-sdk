# ForecastAPI.AccumulatedForecastByPeriodInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date** | **Date** |  | [optional] 
**weight** | **Number** | survival × discount weight applied to this period (period 1 is 1.0) | [optional] 
**cumulative** | **Number** | Running weighted total through this period | [optional] 
**cumulativeLower** | **Number** | Running lower bound; present only when every period so far has a usable band | [optional] 
**cumulativeUpper** | **Number** |  | [optional] 


