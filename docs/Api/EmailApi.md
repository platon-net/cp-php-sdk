# Platon\\ControlPanel\\Sdk\EmailApi



All URIs are relative to https://setup.platon.sk/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**changeMailboxPassword()**](EmailApi.md#changeMailboxPassword) | **PATCH** /email/{domain}/mailboxes/{username}/password | Change mailbox password |
| [**createMailbox()**](EmailApi.md#createMailbox) | **POST** /email/{domain}/mailboxes | Create mailbox |


## `changeMailboxPassword()`

```php
changeMailboxPassword($domain, $username, $change_mailbox_password_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Change mailbox password

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\EmailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'domain_example'; // string | Domain name
$username = 'username_example'; // string | Mailbox username
$change_mailbox_password_request = new \Platon\\ControlPanel\\Sdk\Model\ChangeMailboxPasswordRequest(); // \Platon\\ControlPanel\\Sdk\Model\ChangeMailboxPasswordRequest | Mailbox password payload

try {
    $result = $apiInstance->changeMailboxPassword($domain, $username, $change_mailbox_password_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailApi->changeMailboxPassword: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**| Domain name | |
| **username** | **string**| Mailbox username | |
| **change_mailbox_password_request** | [**\Platon\\ControlPanel\\Sdk\Model\ChangeMailboxPasswordRequest**](../Model/ChangeMailboxPasswordRequest.md)| Mailbox password payload | |

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

## `createMailbox()`

```php
createMailbox($domain, $create_mailbox_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Create mailbox

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\EmailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'domain_example'; // string | Domain name
$create_mailbox_request = new \Platon\\ControlPanel\\Sdk\Model\CreateMailboxRequest(); // \Platon\\ControlPanel\\Sdk\Model\CreateMailboxRequest | Mailbox payload

try {
    $result = $apiInstance->createMailbox($domain, $create_mailbox_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailApi->createMailbox: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**| Domain name | |
| **create_mailbox_request** | [**\Platon\\ControlPanel\\Sdk\Model\CreateMailboxRequest**](../Model/CreateMailboxRequest.md)| Mailbox payload | |

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
