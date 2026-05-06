# Platon\\ControlPanel\\Sdk\AuthApi



All URIs are relative to https://setup.platon.sk/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createAuthToken()**](AuthApi.md#createAuthToken) | **POST** /auth/token | Create anonymous auth token |


## `createAuthToken()`

```php
createAuthToken(): \Platon\\ControlPanel\\Sdk\Model\CreateAuthToken200Response
```

Create anonymous auth token

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Platon\\ControlPanel\\Sdk\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->createAuthToken();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->createAuthToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\CreateAuthToken200Response**](../Model/CreateAuthToken200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
