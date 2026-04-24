# Platon\\ControlPanel\\Sdk\DomainApi



All URIs are relative to https://setup.platon.sk/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**changeDomainNameservers()**](DomainApi.md#changeDomainNameservers) | **PATCH** /domains/{domain}/nameservers | Change domain nameservers |
| [**closeDomain()**](DomainApi.md#closeDomain) | **DELETE** /domains/{domain} | Close external customer domain product |
| [**getDomainInfo()**](DomainApi.md#getDomainInfo) | **GET** /domains/{domain} | Get domain information and availability |
| [**listDomains()**](DomainApi.md#listDomains) | **GET** /domains | List customer domains |
| [**registerDomain()**](DomainApi.md#registerDomain) | **POST** /domains/{domain}/register | Register domain |
| [**renewDomain()**](DomainApi.md#renewDomain) | **POST** /domains/{domain}/renew | Renew domain |


## `changeDomainNameservers()`

```php
changeDomainNameservers($domain, $change_domain_nameservers_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Change domain nameservers

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\DomainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'domain_example'; // string | Domain name
$change_domain_nameservers_request = new \Platon\\ControlPanel\\Sdk\Model\ChangeDomainNameserversRequest(); // \Platon\\ControlPanel\\Sdk\Model\ChangeDomainNameserversRequest | Nameserver payload

try {
    $result = $apiInstance->changeDomainNameservers($domain, $change_domain_nameservers_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainApi->changeDomainNameservers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**| Domain name | |
| **change_domain_nameservers_request** | [**\Platon\\ControlPanel\\Sdk\Model\ChangeDomainNameserversRequest**](../Model/ChangeDomainNameserversRequest.md)| Nameserver payload | |

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

## `closeDomain()`

```php
closeDomain($domain, $cname): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Close external customer domain product

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\DomainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'domain_example'; // string | Domain name
$cname = 'cname_example'; // string | Customer name

try {
    $result = $apiInstance->closeDomain($domain, $cname);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainApi->closeDomain: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**| Domain name | |
| **cname** | **string**| Customer name | |

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

## `getDomainInfo()`

```php
getDomainInfo($domain, $cname): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Get domain information and availability

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\DomainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'domain_example'; // string | Domain name
$cname = 'cname_example'; // string | Customer name for product context

try {
    $result = $apiInstance->getDomainInfo($domain, $cname);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainApi->getDomainInfo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**| Domain name | |
| **cname** | **string**| Customer name for product context | [optional] |

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

## `listDomains()`

```php
listDomains($cname): \Platon\\ControlPanel\\Sdk\Model\ListDomains200Response
```

List customer domains

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\DomainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$cname = 'cname_example'; // string | Customer name

try {
    $result = $apiInstance->listDomains($cname);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainApi->listDomains: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cname** | **string**| Customer name | |

### Return type

[**\Platon\\ControlPanel\\Sdk\Model\ListDomains200Response**](../Model/ListDomains200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `registerDomain()`

```php
registerDomain($domain, $register_domain_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Register domain

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\DomainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'domain_example'; // string | Domain name
$register_domain_request = new \Platon\\ControlPanel\\Sdk\Model\RegisterDomainRequest(); // \Platon\\ControlPanel\\Sdk\Model\RegisterDomainRequest | Domain registration payload

try {
    $result = $apiInstance->registerDomain($domain, $register_domain_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainApi->registerDomain: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**| Domain name | |
| **register_domain_request** | [**\Platon\\ControlPanel\\Sdk\Model\RegisterDomainRequest**](../Model/RegisterDomainRequest.md)| Domain registration payload | |

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

## `renewDomain()`

```php
renewDomain($domain, $renew_domain_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Renew domain

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\DomainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'domain_example'; // string | Domain name
$renew_domain_request = new \Platon\\ControlPanel\\Sdk\Model\RenewDomainRequest(); // \Platon\\ControlPanel\\Sdk\Model\RenewDomainRequest | Domain renewal payload

try {
    $result = $apiInstance->renewDomain($domain, $renew_domain_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainApi->renewDomain: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**| Domain name | |
| **renew_domain_request** | [**\Platon\\ControlPanel\\Sdk\Model\RenewDomainRequest**](../Model/RenewDomainRequest.md)| Domain renewal payload | [optional] |

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
