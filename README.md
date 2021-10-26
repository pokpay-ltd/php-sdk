# OpenAPIClient-php

No description provided (generated by Openapi Generator https://github.com/openapitools/openapi-generator)


## Installation & Usage

### Requirements

PHP 7.3 and later.
Should also work with PHP 8.0 but has not been tested.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');




$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \OpenAPI\Client\Model\LoginSdk(); // \OpenAPI\Client\Model\LoginSdk

try {
    $result = $apiInstance->login($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->login: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *http://0.0.0.0:3000*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthApi* | [**login**](docs/Api/AuthApi.md#login) | **POST** /auth/sdk/login | Login Sdk
*MerchantsApi* | [**captureOrder**](docs/Api/MerchantsApi.md#captureorder) | **POST** /merchants/{merchantId}/sdk-orders/{sdkOrderId}/capture | Capture an sdk order
*MerchantsApi* | [**createOrder**](docs/Api/MerchantsApi.md#createorder) | **POST** /merchants/{merchantId}/sdk-orders | Create an sdk api order
*SdkOrdersApi* | [**confirmOrder**](docs/Api/SdkOrdersApi.md#confirmorder) | **POST** /sdk-orders/{sdkOrderId}/confirm | Confirm order.
*SdkOrdersApi* | [**getOrderById**](docs/Api/SdkOrdersApi.md#getorderbyid) | **GET** /sdk-orders/{sdkOrderId} | Retrieve an order
*SdkOrdersApi* | [**guestConfirmOrder**](docs/Api/SdkOrdersApi.md#guestconfirmorder) | **POST** /sdk-orders/{sdkOrderId}/guest-confirm | Confirm order with guest checkout

## Models

- [ConfirmSdkOrderGuestPayload](docs/Model/ConfirmSdkOrderGuestPayload.md)
- [ConfirmSdkOrderPayload](docs/Model/ConfirmSdkOrderPayload.md)
- [CreateSdkOrderPayload](docs/Model/CreateSdkOrderPayload.md)
- [CreateSdkOrderProductsObject](docs/Model/CreateSdkOrderProductsObject.md)
- [LoginSdk](docs/Model/LoginSdk.md)

## Authorization
All endpoints do not require authorization.
## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`