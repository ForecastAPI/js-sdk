# ForecastAPI.AutoSelection

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**requested** | **String** |  | [optional] 
**selected** | **String** | The model that produced this response | [optional] 
**reason** | **String** | Why this model was selected. &#x60;scored_winner&#x60; means one model beat every alternative by a clear margin on realized accuracy for this identifier; everything else means the evidence-gathering default was served.  | [optional] 
**scores** | [**{String: AutoSelectionScoresValue}**](AutoSelectionScoresValue.md) | Per-model realized-accuracy scorecard for this identifier, when one exists | [optional] 



## Enum: ReasonEnum


* `no_history` (value: `"no_history"`)

* `insufficient_evidence` (value: `"insufficient_evidence"`)

* `no_clear_winner` (value: `"no_clear_winner"`)

* `scored_winner` (value: `"scored_winner"`)




