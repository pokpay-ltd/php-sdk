# OpenAPI\Client\AuthApi

All URIs are relative to *https://api.pokpay.io* in the production environment and *https://api-staging.pokpay.io* in the staging environment.

Method | HTTP request | Description
------------- | ------------- | -------------
[**login()**](AuthApi.md#login) | **POST** /auth/sdk/login | Login Sdk


## `login()`

```php
login($body): \OpenAPI\Client\Model\LoginResponse
```

Login Sdk

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Create the configuration for the API calls
// getDefaultConfiguration accepts a parameter to specify whether the production environment is used
// By default the staging environment is used
// The same configuration is later used for all the other API classes
$config = OpenAPI\Client\Configuration::getDefaultConfiguration(true);

$apiInstance = new OpenAPI\Client\Api\AuthApi(
    $config,
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \OpenAPI\Client\Model\LoginSdkPayload(); // \OpenAPI\Client\Model\LoginSdkPayload

try {
    $result = $apiInstance->login($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->login: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\OpenAPI\Client\Model\LoginSdkPayload**](../Model/LoginSdkPayload.md)|  | [optional]

### Return type

[**\OpenAPI\Client\Model\LoginResponse**](../Model/LoginResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
