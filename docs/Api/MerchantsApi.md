# OpenAPI\Client\MerchantsApi

All URIs are relative to http://0.0.0.0:3000.

Method | HTTP request | Description
------------- | ------------- | -------------
[**captureOrder()**](MerchantsApi.md#captureOrder) | **POST** /merchants/{merchantId}/sdk-orders/{sdkOrderId}/capture | Capture an sdk order
[**createOrder()**](MerchantsApi.md#createOrder) | **POST** /merchants/{merchantId}/sdk-orders | Create an sdk api order


## `captureOrder()`

```php
captureOrder($merchant_id, $sdk_order_id): string
```

Capture an sdk order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MerchantsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$merchant_id = 'merchant_id_example'; // string
$sdk_order_id = 'sdk_order_id_example'; // string

try {
    $result = $apiInstance->captureOrder($merchant_id, $sdk_order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MerchantsApi->captureOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchant_id** | **string**|  |
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

## `createOrder()`

```php
createOrder($merchant_id, $body): string
```

Create an sdk api order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MerchantsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$merchant_id = 'merchant_id_example'; // string
$body = new \OpenAPI\Client\Model\CreateSdkOrderPayload(); // \OpenAPI\Client\Model\CreateSdkOrderPayload

try {
    $result = $apiInstance->createOrder($merchant_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MerchantsApi->createOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchant_id** | **string**|  |
 **body** | [**\OpenAPI\Client\Model\CreateSdkOrderPayload**](../Model/CreateSdkOrderPayload.md)|  | [optional]

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
