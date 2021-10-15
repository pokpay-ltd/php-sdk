# OpenAPI\Client\SdkOrdersApi

All URIs are relative to http://0.0.0.0:3000.

Method | HTTP request | Description
------------- | ------------- | -------------
[**confirmOrder()**](SdkOrdersApi.md#confirmOrder) | **POST** /sdk-orders/{sdkOrderId}/confirm | Confirm order.
[**getOrderById()**](SdkOrdersApi.md#getOrderById) | **GET** /sdk-orders/{sdkOrderId} | Retrieve an order
[**guestConfirmOrder()**](SdkOrdersApi.md#guestConfirmOrder) | **POST** /sdk-orders/{sdkOrderId}/guest-confirm | Confirm order with guest checkout


## `confirmOrder()`

```php
confirmOrder($sdk_order_id, $body): string
```

Confirm order.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SdkOrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$sdk_order_id = 'sdk_order_id_example'; // string
$body = new \OpenAPI\Client\Model\ConfirmSdkOrderPayload(); // \OpenAPI\Client\Model\ConfirmSdkOrderPayload

try {
    $result = $apiInstance->confirmOrder($sdk_order_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SdkOrdersApi->confirmOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sdk_order_id** | **string**|  |
 **body** | [**\OpenAPI\Client\Model\ConfirmSdkOrderPayload**](../Model/ConfirmSdkOrderPayload.md)|  | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrderById()`

```php
getOrderById($sdk_order_id): string
```

Retrieve an order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SdkOrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$sdk_order_id = 'sdk_order_id_example'; // string

try {
    $result = $apiInstance->getOrderById($sdk_order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SdkOrdersApi->getOrderById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sdk_order_id** | **string**|  |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `guestConfirmOrder()`

```php
guestConfirmOrder($sdk_order_id, $body): string
```

Confirm order with guest checkout

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SdkOrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$sdk_order_id = 'sdk_order_id_example'; // string
$body = new \OpenAPI\Client\Model\ConfirmSdkOrderGuestPayload(); // \OpenAPI\Client\Model\ConfirmSdkOrderGuestPayload

try {
    $result = $apiInstance->guestConfirmOrder($sdk_order_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SdkOrdersApi->guestConfirmOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sdk_order_id** | **string**|  |
 **body** | [**\OpenAPI\Client\Model\ConfirmSdkOrderGuestPayload**](../Model/ConfirmSdkOrderGuestPayload.md)|  | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
