# OpenAPI\Client\SdkOrdersApi

All URIs are relative to *https://api.pokpay.io* in the production environment and *https://api-staging.pokpay.io* in the staging environment.

Method | HTTP request | Description
------------- | ------------- | -------------
[**confirmOrder()**](SdkOrdersApi.md#confirmOrder) | **POST** /sdk-orders/{sdkOrderId}/confirm | Confirm order.
[**confirmOrderAsGuest()**](SdkOrdersApi.md#confirmOrderAsGuest) | **POST** /sdk-orders/{sdkOrderId}/guest-confirm | Confirm order with guest checkout
[**getSdkOrderById()**](SdkOrdersApi.md#getSdkOrderById) | **GET** /sdk-orders/{sdkOrderId} | Retrieve an order


## `confirmOrder()`

```php
confirmOrder($sdkOrderId, $body): \OpenAPI\Client\Model\SdkOrderResponse
```

Confirm order.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new OpenAPI\Client\Api\SdkOrdersApi(
    $config,
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
);

$sdkOrderId = 'sdkOrderId_example'; // string
$body = new \OpenAPI\Client\Model\ConfirmSdkOrderPayload(); // \OpenAPI\Client\Model\ConfirmSdkOrderPayload

try {
    $result = $apiInstance->confirmOrder($sdkOrderId, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SdkOrdersApi->confirmOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sdkOrderId** | **string**|  |
 **body** | [**\OpenAPI\Client\Model\ConfirmSdkOrderPayload**](../Model/ConfirmSdkOrderPayload.md)|  | [optional]

### Return type

[**\OpenAPI\Client\Model\SdkOrderResponse**](../Model/SdkOrderResponse.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `confirmOrderAsGuest()`

```php
confirmOrderAsGuest($sdkOrderId, $body): \OpenAPI\Client\Model\SdkOrderResponse
```

Confirm order with guest checkout

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = OpenAPI\Client\Configuration::getDefaultConfiguration();

$apiInstance = new OpenAPI\Client\Api\SdkOrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$sdkOrderId = 'sdkOrderId_example'; // string
$body = new \OpenAPI\Client\Model\ConfirmSdkOrderGuestPayload(); // \OpenAPI\Client\Model\ConfirmSdkOrderGuestPayload

try {
    $result = $apiInstance->confirmOrderAsGuest($sdkOrderId, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SdkOrdersApi->confirmOrderAsGuest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sdkOrderId** | **string**|  |
 **body** | [**\OpenAPI\Client\Model\ConfirmSdkOrderGuestPayload**](../Model/ConfirmSdkOrderGuestPayload.md)|  | [optional]

### Return type

[**\OpenAPI\Client\Model\SdkOrderResponse**](../Model/SdkOrderResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSdkOrderById()`

```php
getSdkOrderById($sdkOrderId): \OpenAPI\Client\Model\SdkOrderResponse
```

Retrieve an order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = OpenAPI\Client\Configuration::getDefaultConfiguration();

$apiInstance = new OpenAPI\Client\Api\SdkOrdersApi(
    $config,
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
);
$sdkOrderId = 'sdkOrderId_example'; // string

try {
    $result = $apiInstance->getSdkOrderById($sdkOrderId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SdkOrdersApi->getSdkOrderById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sdkOrderId** | **string**|  |

### Return type

[**\OpenAPI\Client\Model\SdkOrderResponse**](../Model/SdkOrderResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
