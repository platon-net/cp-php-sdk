# Platon\\ControlPanel\\Sdk\AntispamApi



All URIs are relative to https://setup.platon.sk/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addAntispamMaildata()**](AntispamApi.md#addAntispamMaildata) | **POST** /antispam/maildata | Add maildata to antispam engine |
| [**checkAntispamMaildataRules()**](AntispamApi.md#checkAntispamMaildataRules) | **POST** /antispam/maildata/check | Check maildata against existing antispam rules |
| [**createAntispamEmailRule()**](AntispamApi.md#createAntispamEmailRule) | **POST** /antispam/rules | Create antispam email rule or increment existing rule hitcount |


## `addAntispamMaildata()`

```php
addAntispamMaildata($add_antispam_maildata_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Add maildata to antispam engine

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\AntispamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$add_antispam_maildata_request = new \Platon\\ControlPanel\\Sdk\Model\AddAntispamMaildataRequest(); // \Platon\\ControlPanel\\Sdk\Model\AddAntispamMaildataRequest | Maildata payload

try {
    $result = $apiInstance->addAntispamMaildata($add_antispam_maildata_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AntispamApi->addAntispamMaildata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **add_antispam_maildata_request** | [**\Platon\\ControlPanel\\Sdk\Model\AddAntispamMaildataRequest**](../Model/AddAntispamMaildataRequest.md)| Maildata payload | |

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

## `checkAntispamMaildataRules()`

```php
checkAntispamMaildataRules($check_antispam_maildata_rules_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Check maildata against existing antispam rules

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\AntispamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$check_antispam_maildata_rules_request = new \Platon\\ControlPanel\\Sdk\Model\CheckAntispamMaildataRulesRequest(); // \Platon\\ControlPanel\\Sdk\Model\CheckAntispamMaildataRulesRequest | Maildata payload

try {
    $result = $apiInstance->checkAntispamMaildataRules($check_antispam_maildata_rules_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AntispamApi->checkAntispamMaildataRules: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **check_antispam_maildata_rules_request** | [**\Platon\\ControlPanel\\Sdk\Model\CheckAntispamMaildataRulesRequest**](../Model/CheckAntispamMaildataRulesRequest.md)| Maildata payload | |

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

## `createAntispamEmailRule()`

```php
createAntispamEmailRule($create_antispam_email_rule_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Create antispam email rule or increment existing rule hitcount

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\AntispamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_antispam_email_rule_request = new \Platon\\ControlPanel\\Sdk\Model\CreateAntispamEmailRuleRequest(); // \Platon\\ControlPanel\\Sdk\Model\CreateAntispamEmailRuleRequest | Antispam email rule payload

try {
    $result = $apiInstance->createAntispamEmailRule($create_antispam_email_rule_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AntispamApi->createAntispamEmailRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_antispam_email_rule_request** | [**\Platon\\ControlPanel\\Sdk\Model\CreateAntispamEmailRuleRequest**](../Model/CreateAntispamEmailRuleRequest.md)| Antispam email rule payload | |

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
