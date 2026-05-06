# Platon\\ControlPanel\\Sdk\LLMApi



All URIs are relative to https://setup.platon.sk/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**spamDetection()**](LLMApi.md#spamDetection) | **POST** /llm/spam-detection | Classify a web form message as spam or ham using the local LLM |


## `spamDetection()`

```php
spamDetection($spam_detection_request): \Platon\\ControlPanel\\Sdk\Model\SpamDetection200Response
```

Classify a web form message as spam or ham using the local LLM

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\LLMApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$spam_detection_request = new \Platon\\ControlPanel\\Sdk\Model\SpamDetectionRequest(); // \Platon\\ControlPanel\\Sdk\Model\SpamDetectionRequest | Spam detection payload

try {
    $result = $apiInstance->spamDetection($spam_detection_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LLMApi->spamDetection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **spam_detection_request** | [**\Platon\\ControlPanel\\Sdk\Model\SpamDetectionRequest**](../Model/SpamDetectionRequest.md)| Spam detection payload | |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\SpamDetection200Response**](../Model/SpamDetection200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
