# Platon\\ControlPanel\\Sdk\CartApi



All URIs are relative to https://setup.platon.sk/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**checkCartCoupon()**](CartApi.md#checkCartCoupon) | **POST** /cart/coupons/check | Check and apply cart coupon |
| [**createCartItem()**](CartApi.md#createCartItem) | **POST** /cart/items | Add item to cart |
| [**deleteCartItem()**](CartApi.md#deleteCartItem) | **DELETE** /cart/items/{cartItemId} | Remove item from cart |
| [**getCartBillingAddress()**](CartApi.md#getCartBillingAddress) | **GET** /cart/billing-address | Get cart billing address |
| [**getCartCoupon()**](CartApi.md#getCartCoupon) | **GET** /cart/coupons/current | Get current cart coupon |
| [**getCartTotal()**](CartApi.md#getCartTotal) | **GET** /cart/total | Get cart total |
| [**listCartItems()**](CartApi.md#listCartItems) | **GET** /cart/items | List cart items |
| [**updateCartItem()**](CartApi.md#updateCartItem) | **PATCH** /cart/items/{cartItemId} | Update cart item data |
| [**updateCartItemCount()**](CartApi.md#updateCartItemCount) | **PATCH** /cart/items/by-product/count | Update cart item count by product and domain |


## `checkCartCoupon()`

```php
checkCartCoupon($check_cart_coupon_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Check and apply cart coupon

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\CartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$check_cart_coupon_request = new \Platon\\ControlPanel\\Sdk\Model\CheckCartCouponRequest(); // \Platon\\ControlPanel\\Sdk\Model\CheckCartCouponRequest | Cart coupon check payload

try {
    $result = $apiInstance->checkCartCoupon($check_cart_coupon_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CartApi->checkCartCoupon: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **check_cart_coupon_request** | [**\Platon\\ControlPanel\\Sdk\Model\CheckCartCouponRequest**](../Model/CheckCartCouponRequest.md)| Cart coupon check payload | |

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

## `createCartItem()`

```php
createCartItem($create_cart_item_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Add item to cart

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\CartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_cart_item_request = new \Platon\\ControlPanel\\Sdk\Model\CreateCartItemRequest(); // \Platon\\ControlPanel\\Sdk\Model\CreateCartItemRequest | Cart item add payload

try {
    $result = $apiInstance->createCartItem($create_cart_item_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CartApi->createCartItem: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_cart_item_request** | [**\Platon\\ControlPanel\\Sdk\Model\CreateCartItemRequest**](../Model/CreateCartItemRequest.md)| Cart item add payload | |

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

## `deleteCartItem()`

```php
deleteCartItem($cart_item_id, $cname): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Remove item from cart

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\CartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$cart_item_id = 56; // int | Cart item ID
$cname = 'cname_example'; // string | Customer name

try {
    $result = $apiInstance->deleteCartItem($cart_item_id, $cname);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CartApi->deleteCartItem: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cart_item_id** | **int**| Cart item ID | |
| **cname** | **string**| Customer name | [optional] |

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

## `getCartBillingAddress()`

```php
getCartBillingAddress($cname): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Get cart billing address

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\CartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$cname = 'cname_example'; // string | Customer name

try {
    $result = $apiInstance->getCartBillingAddress($cname);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CartApi->getCartBillingAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cname** | **string**| Customer name | [optional] |

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

## `getCartCoupon()`

```php
getCartCoupon($cname): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Get current cart coupon

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\CartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$cname = 'cname_example'; // string | Customer name

try {
    $result = $apiInstance->getCartCoupon($cname);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CartApi->getCartCoupon: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cname** | **string**| Customer name | [optional] |

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

## `getCartTotal()`

```php
getCartTotal($cname): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Get cart total

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\CartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$cname = 'cname_example'; // string | Customer name

try {
    $result = $apiInstance->getCartTotal($cname);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CartApi->getCartTotal: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cname** | **string**| Customer name | [optional] |

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

## `listCartItems()`

```php
listCartItems($cname, $lang): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

List cart items

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\CartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$cname = 'cname_example'; // string | Customer name
$lang = 'lang_example'; // string | Response language

try {
    $result = $apiInstance->listCartItems($cname, $lang);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CartApi->listCartItems: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cname** | **string**| Customer name | [optional] |
| **lang** | **string**| Response language | [optional] |

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

## `updateCartItem()`

```php
updateCartItem($cart_item_id, $update_cart_item_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Update cart item data

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\CartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$cart_item_id = 56; // int | Cart item ID
$update_cart_item_request = new \Platon\\ControlPanel\\Sdk\Model\UpdateCartItemRequest(); // \Platon\\ControlPanel\\Sdk\Model\UpdateCartItemRequest | Cart item update payload

try {
    $result = $apiInstance->updateCartItem($cart_item_id, $update_cart_item_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CartApi->updateCartItem: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cart_item_id** | **int**| Cart item ID | |
| **update_cart_item_request** | [**\Platon\\ControlPanel\\Sdk\Model\UpdateCartItemRequest**](../Model/UpdateCartItemRequest.md)| Cart item update payload | |

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

## `updateCartItemCount()`

```php
updateCartItemCount($update_cart_item_count_request): \Platon\\ControlPanel\\Sdk\Model\CreateDnsRecord200Response
```

Update cart item count by product and domain

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Platon\\ControlPanel\\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Platon\\ControlPanel\\Sdk\Api\CartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$update_cart_item_count_request = new \Platon\\ControlPanel\\Sdk\Model\UpdateCartItemCountRequest(); // \Platon\\ControlPanel\\Sdk\Model\UpdateCartItemCountRequest | Cart item count update payload

try {
    $result = $apiInstance->updateCartItemCount($update_cart_item_count_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CartApi->updateCartItemCount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **update_cart_item_count_request** | [**\Platon\\ControlPanel\\Sdk\Model\UpdateCartItemCountRequest**](../Model/UpdateCartItemCountRequest.md)| Cart item count update payload | |

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
