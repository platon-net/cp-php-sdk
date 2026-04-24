# Platon\\ControlPanel\\Sdk\VehicleApi



All URIs are relative to https://setup.platon.sk/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createVehicleEvent()**](VehicleApi.md#createVehicleEvent) | **POST** /vehicle/events | Create vehicle event without receipt image |
| [**deleteVehicleEvent()**](VehicleApi.md#deleteVehicleEvent) | **DELETE** /vehicle/events/{eventId} | Delete vehicle event |
| [**finalizeVehicleEvent()**](VehicleApi.md#finalizeVehicleEvent) | **POST** /vehicle/events/{eventId}/finalize | Finalize vehicle event draft |
| [**getVehicleEvent()**](VehicleApi.md#getVehicleEvent) | **GET** /vehicle/events/{eventId} | Get vehicle event detail |
| [**getVehicleEventImage()**](VehicleApi.md#getVehicleEventImage) | **GET** /vehicle/events/{eventId}/image | Get event image or thumbnail |
| [**listVehicleCurrencies()**](VehicleApi.md#listVehicleCurrencies) | **GET** /vehicle/currencies | List currencies for vehicle events |
| [**listVehicleEvents()**](VehicleApi.md#listVehicleEvents) | **GET** /vehicle/events | List vehicle events for the authenticated driver |
| [**listVehicleVehicles()**](VehicleApi.md#listVehicleVehicles) | **GET** /vehicle/vehicles | List vehicles available to the authenticated driver |
| [**rescanVehicleEventImage()**](VehicleApi.md#rescanVehicleEventImage) | **POST** /vehicle/events/{eventId}/image | Replace event image and rescan event data |
| [**setPreferredVehicle()**](VehicleApi.md#setPreferredVehicle) | **PATCH** /vehicle/preferred-vehicle | Set or clear preferred vehicle |
| [**uploadVehicleReceiptImage()**](VehicleApi.md#uploadVehicleReceiptImage) | **POST** /vehicle/events/receipt-image | Upload receipt image and create processing event draft |


## `createVehicleEvent()`

```php
createVehicleEvent($create_vehicle_event_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Create vehicle event without receipt image

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\VehicleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_vehicle_event_request = new \Platon\\ControlPanel\\Sdk\Model\CreateVehicleEventRequest(); // \Platon\\ControlPanel\\Sdk\Model\CreateVehicleEventRequest | Vehicle event create payload

try {
    $result = $apiInstance->createVehicleEvent($create_vehicle_event_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VehicleApi->createVehicleEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_vehicle_event_request** | [**\Platon\\ControlPanel\\Sdk\Model\CreateVehicleEventRequest**](../Model/CreateVehicleEventRequest.md)| Vehicle event create payload | |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response**](../Model/CreateDnsRecord200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteVehicleEvent()`

```php
deleteVehicleEvent($event_id): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Delete vehicle event

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\VehicleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$event_id = 56; // int | Vehicle event ID

try {
    $result = $apiInstance->deleteVehicleEvent($event_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VehicleApi->deleteVehicleEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **event_id** | **int**| Vehicle event ID | |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response**](../Model/CreateDnsRecord200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `finalizeVehicleEvent()`

```php
finalizeVehicleEvent($event_id, $finalize_vehicle_event_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Finalize vehicle event draft

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\VehicleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$event_id = 56; // int | Vehicle event ID
$finalize_vehicle_event_request = new \Platon\\ControlPanel\\Sdk\Model\FinalizeVehicleEventRequest(); // \Platon\\ControlPanel\\Sdk\Model\FinalizeVehicleEventRequest | Vehicle event finalize payload

try {
    $result = $apiInstance->finalizeVehicleEvent($event_id, $finalize_vehicle_event_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VehicleApi->finalizeVehicleEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **event_id** | **int**| Vehicle event ID | |
| **finalize_vehicle_event_request** | [**\Platon\\ControlPanel\\Sdk\Model\FinalizeVehicleEventRequest**](../Model/FinalizeVehicleEventRequest.md)| Vehicle event finalize payload | |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response**](../Model/CreateDnsRecord200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVehicleEvent()`

```php
getVehicleEvent($event_id): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Get vehicle event detail

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\VehicleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$event_id = 56; // int | Vehicle event ID

try {
    $result = $apiInstance->getVehicleEvent($event_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VehicleApi->getVehicleEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **event_id** | **int**| Vehicle event ID | |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response**](../Model/CreateDnsRecord200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVehicleEventImage()`

```php
getVehicleEventImage($event_id, $size): \SplFileObject
```

Get event image or thumbnail

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\VehicleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$event_id = 56; // int | Vehicle event ID
$size = 'size_example'; // string | Image size variant: thumb, thumbnail or small for thumbnail response

try {
    $result = $apiInstance->getVehicleEventImage($event_id, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VehicleApi->getVehicleEventImage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **event_id** | **int**| Vehicle event ID | |
| **size** | **string**| Image size variant: thumb, thumbnail or small for thumbnail response | [optional] |

### Return type

**\SplFileObject**

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `image/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listVehicleCurrencies()`

```php
listVehicleCurrencies(): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

List currencies for vehicle events

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\VehicleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listVehicleCurrencies();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VehicleApi->listVehicleCurrencies: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response**](../Model/CreateDnsRecord200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listVehicleEvents()`

```php
listVehicleEvents($since): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

List vehicle events for the authenticated driver

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\VehicleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$since = 'since_example'; // string | Return events with event datetime greater than or equal to the provided local datetime

try {
    $result = $apiInstance->listVehicleEvents($since);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VehicleApi->listVehicleEvents: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **since** | **string**| Return events with event datetime greater than or equal to the provided local datetime | [optional] |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response**](../Model/CreateDnsRecord200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listVehicleVehicles()`

```php
listVehicleVehicles(): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

List vehicles available to the authenticated driver

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\VehicleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listVehicleVehicles();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VehicleApi->listVehicleVehicles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response**](../Model/CreateDnsRecord200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `rescanVehicleEventImage()`

```php
rescanVehicleEventImage($event_id, $image, $timezone, $event_type): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Replace event image and rescan event data

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\VehicleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$event_id = 56; // int | Vehicle event ID
$image = '/path/to/file.txt'; // \SplFileObject
$timezone = 'timezone_example'; // string
$event_type = 'event_type_example'; // string

try {
    $result = $apiInstance->rescanVehicleEventImage($event_id, $image, $timezone, $event_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VehicleApi->rescanVehicleEventImage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **event_id** | **int**| Vehicle event ID | |
| **image** | **\SplFileObject****\SplFileObject**|  | |
| **timezone** | **string**|  | [optional] |
| **event_type** | **string**|  | [optional] |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response**](../Model/CreateDnsRecord200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setPreferredVehicle()`

```php
setPreferredVehicle($set_preferred_vehicle_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Set or clear preferred vehicle

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\VehicleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$set_preferred_vehicle_request = new \Platon\\ControlPanel\\Sdk\Model\SetPreferredVehicleRequest(); // \Platon\\ControlPanel\\Sdk\Model\SetPreferredVehicleRequest | Preferred vehicle payload

try {
    $result = $apiInstance->setPreferredVehicle($set_preferred_vehicle_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VehicleApi->setPreferredVehicle: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **set_preferred_vehicle_request** | [**\Platon\\ControlPanel\\Sdk\Model\SetPreferredVehicleRequest**](../Model/SetPreferredVehicleRequest.md)| Preferred vehicle payload | [optional] |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response**](../Model/CreateDnsRecord200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadVehicleReceiptImage()`

```php
uploadVehicleReceiptImage($image, $timezone, $event_type): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Upload receipt image and create processing event draft

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\VehicleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$image = '/path/to/file.txt'; // \SplFileObject
$timezone = 'timezone_example'; // string
$event_type = 'event_type_example'; // string

try {
    $result = $apiInstance->uploadVehicleReceiptImage($image, $timezone, $event_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VehicleApi->uploadVehicleReceiptImage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **image** | **\SplFileObject****\SplFileObject**|  | |
| **timezone** | **string**|  | |
| **event_type** | **string**|  | [optional] |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response**](../Model/CreateDnsRecord200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
