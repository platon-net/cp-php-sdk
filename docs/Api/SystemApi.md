# Platon\\ControlPanel\\Sdk\SystemApi



All URIs are relative to https://setup.platon.sk/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**hello()**](SystemApi.md#hello) | **GET** /system/hello | Returns greeting message |
| [**revision()**](SystemApi.md#revision) | **GET** /system/revision | Returns revision number of system |
| [**time()**](SystemApi.md#time) | **GET** /system/time | Returns current date and time of system |


## `hello()`

```php
hello(): \Platon\\ControlPanel\\Sdk\Model\Hello200Response
```

Returns greeting message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Platon\\ControlPanel\\Sdk\Api\SystemApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->hello();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SystemApi->hello: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\Hello200Response**](../Model/Hello200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `revision()`

```php
revision(): \Platon\\ControlPanel\\Sdk\Model\Revision200Response
```

Returns revision number of system

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Platon\\ControlPanel\\Sdk\Api\SystemApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->revision();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SystemApi->revision: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\Revision200Response**](../Model/Revision200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `time()`

```php
time(): \Platon\\ControlPanel\\Sdk\Model\Time200Response
```

Returns current date and time of system

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Platon\\ControlPanel\\Sdk\Api\SystemApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->time();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SystemApi->time: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\Time200Response**](../Model/Time200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
