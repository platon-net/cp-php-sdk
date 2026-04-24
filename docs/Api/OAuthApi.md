# Platon\\ControlPanel\\Sdk\OAuthApi



All URIs are relative to https://setup.platon.sk/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createOauthRequest()**](OAuthApi.md#createOauthRequest) | **POST** /oauth/requests | Create OAuth request |
| [**deleteOauthToken()**](OAuthApi.md#deleteOauthToken) | **DELETE** /oauth/tokens | Delete OAuth token |
| [**getOauthScopes()**](OAuthApi.md#getOauthScopes) | **GET** /oauth/scopes | List available OAuth scopes |
| [**refreshOauthToken()**](OAuthApi.md#refreshOauthToken) | **POST** /oauth/tokens/refresh | Refresh OAuth token |
| [**verifyOauthRequest()**](OAuthApi.md#verifyOauthRequest) | **GET** /oauth/requests/verify | Verify OAuth request |


## `createOauthRequest()`

```php
createOauthRequest($create_oauth_request_request): \Platon\\ControlPanel\\Sdk\Model\CreateOauthRequest200Response
```

Create OAuth request

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Platon\\ControlPanel\\Sdk\Api\OAuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$create_oauth_request_request = new \Platon\\ControlPanel\\Sdk\Model\CreateOauthRequestRequest(); // \Platon\\ControlPanel\\Sdk\Model\CreateOauthRequestRequest | OAuth create payload

try {
    $result = $apiInstance->createOauthRequest($create_oauth_request_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OAuthApi->createOauthRequest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_oauth_request_request** | [**\Platon\\ControlPanel\\Sdk\Model\CreateOauthRequestRequest**](../Model/CreateOauthRequestRequest.md)| OAuth create payload | [optional] |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\CreateOauthRequest200Response**](../Model/CreateOauthRequest200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteOauthToken()`

```php
deleteOauthToken($token): \Platon\\ControlPanel\\Sdk\Model\DeleteOauthToken200Response
```

Delete OAuth token

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\OAuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$token = 'token_example'; // string | OAuth token

try {
    $result = $apiInstance->deleteOauthToken($token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OAuthApi->deleteOauthToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **token** | **string**| OAuth token | |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\DeleteOauthToken200Response**](../Model/DeleteOauthToken200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOauthScopes()`

```php
getOauthScopes(): \Platon\\ControlPanel\\Sdk\Model\GetOauthScopes200Response
```

List available OAuth scopes

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Platon\\ControlPanel\\Sdk\Api\OAuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getOauthScopes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OAuthApi->getOauthScopes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\GetOauthScopes200Response**](../Model/GetOauthScopes200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `refreshOauthToken()`

```php
refreshOauthToken($refresh_oauth_token_request): \Platon\\ControlPanel\\Sdk\Model\VerifyOauthRequest200Response
```

Refresh OAuth token

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\OAuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$refresh_oauth_token_request = new \Platon\\ControlPanel\\Sdk\Model\RefreshOauthTokenRequest(); // \Platon\\ControlPanel\\Sdk\Model\RefreshOauthTokenRequest | OAuth refresh payload

try {
    $result = $apiInstance->refreshOauthToken($refresh_oauth_token_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OAuthApi->refreshOauthToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **refresh_oauth_token_request** | [**\Platon\\ControlPanel\\Sdk\Model\RefreshOauthTokenRequest**](../Model/RefreshOauthTokenRequest.md)| OAuth refresh payload | |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\VerifyOauthRequest200Response**](../Model/VerifyOauthRequest200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `verifyOauthRequest()`

```php
verifyOauthRequest($verify_token): \Platon\\ControlPanel\\Sdk\Model\VerifyOauthRequest200Response
```

Verify OAuth request

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Platon\\ControlPanel\\Sdk\Api\OAuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$verify_token = 'verify_token_example'; // string | Verify token from OAuth create response

try {
    $result = $apiInstance->verifyOauthRequest($verify_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OAuthApi->verifyOauthRequest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **verify_token** | **string**| Verify token from OAuth create response | |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\VerifyOauthRequest200Response**](../Model/VerifyOauthRequest200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
