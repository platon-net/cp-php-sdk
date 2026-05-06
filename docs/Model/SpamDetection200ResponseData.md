# SpamDetection200ResponseData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**classification** | **string** | Normalized classification returned by the LLM. |
**confidence** | **float** | Normalized confidence from 0 to 100. |
**reason** | **string** | Short explanation in Slovak. |
**signals** | **string[]** | Most important signals used for the classification. |
**error** | **bool** | True when the LLM call or response validation failed. |
**error_message** | **string** | Short technical error reason. Raw LLM response is never returned here. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
