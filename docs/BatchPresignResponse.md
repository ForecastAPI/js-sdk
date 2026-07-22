# ForecastAPI.BatchPresignResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uploadUrl** | **String** | Presigned URL — HTTP PUT the JSON file here, including any returned headers | [optional] 
**headers** | **{String: String}** | Headers that must be sent with the upload request | [optional] 
**fileKey** | **String** | Pass this as &#x60;file_key&#x60; to POST /v2/batch/forecast after uploading | [optional] 
**expiresIn** | **Number** | Seconds the upload URL stays valid | [optional] 


