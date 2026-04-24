# Platon\\ControlPanel\\Sdk\DNSApi



All URIs are relative to https://setup.platon.sk/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createDnsRecord()**](DNSApi.md#createDnsRecord) | **POST** /dns/{domain}/records | Create DNS record |
| [**deleteDnsRecord()**](DNSApi.md#deleteDnsRecord) | **DELETE** /dns/{domain}/records/{recordId} | Delete DNS record |
| [**getDnsRecords()**](DNSApi.md#getDnsRecords) | **GET** /dns/{domain}/records | Get DNS records by domain |
| [**updateDnsRecord()**](DNSApi.md#updateDnsRecord) | **PATCH** /dns/{domain}/records/{recordId} | Update DNS record |


## `createDnsRecord()`

```php
createDnsRecord($domain, $create_dns_record_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Create DNS record

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\DNSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'domain_example'; // string | Domain name
$create_dns_record_request = new \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecordRequest(); // \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecordRequest | DNS record payload

try {
    $result = $apiInstance->createDnsRecord($domain, $create_dns_record_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DNSApi->createDnsRecord: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**| Domain name | |
| **create_dns_record_request** | [**\Platon\\ControlPanel\\Sdk\Model\CreateDnsRecordRequest**](../Model/CreateDnsRecordRequest.md)| DNS record payload | |

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

## `deleteDnsRecord()`

```php
deleteDnsRecord($domain, $record_id): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Delete DNS record

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\DNSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'domain_example'; // string | Domain name
$record_id = 56; // int | Record ID

try {
    $result = $apiInstance->deleteDnsRecord($domain, $record_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DNSApi->deleteDnsRecord: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**| Domain name | |
| **record_id** | **int**| Record ID | |

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

## `getDnsRecords()`

```php
getDnsRecords($domain, $type): \Platon\\ControlPanel\\Sdk\Model\GetDnsRecords200Response
```

Get DNS records by domain

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\DNSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'domain_example'; // string | Domain name
$type = 'type_example'; // string | Filter records by type

try {
    $result = $apiInstance->getDnsRecords($domain, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DNSApi->getDnsRecords: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**| Domain name | |
| **type** | **string**| Filter records by type | [optional] |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\GetDnsRecords200Response**](../Model/GetDnsRecords200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateDnsRecord()`

```php
updateDnsRecord($domain, $record_id, $update_dns_record_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Update DNS record

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\DNSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'domain_example'; // string | Domain name
$record_id = 56; // int | Record ID
$update_dns_record_request = new \Platon\\ControlPanel\\Sdk\Model\UpdateDnsRecordRequest(); // \Platon\\ControlPanel\\Sdk\Model\UpdateDnsRecordRequest | Partial DNS record payload

try {
    $result = $apiInstance->updateDnsRecord($domain, $record_id, $update_dns_record_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DNSApi->updateDnsRecord: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**| Domain name | |
| **record_id** | **int**| Record ID | |
| **update_dns_record_request** | [**\Platon\\ControlPanel\\Sdk\Model\UpdateDnsRecordRequest**](../Model/UpdateDnsRecordRequest.md)| Partial DNS record payload | |

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
