# OpenAPI\Client\MiscelleneousApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getRateSources()**](MiscelleneousApi.md#getRateSources) | **GET** /misc/rate-sources | Get available rate sources |
| [**invoiceCheckout()**](MiscelleneousApi.md#invoiceCheckout) | **GET** /i/{invoiceId} | Invoice checkout |
| [**langCodes()**](MiscelleneousApi.md#langCodes) | **GET** /misc/lang | Language codes |
| [**permissionsMetadata()**](MiscelleneousApi.md#permissionsMetadata) | **GET** /misc/permissions | Permissions metadata |


## `getRateSources()`

```php
getRateSources(): \OpenAPI\Client\Model\GetRateSources200ResponseInner[]
```

Get available rate sources

View available rate providers that you can use in stores

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MiscelleneousApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getRateSources();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MiscelleneousApi->getRateSources: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetRateSources200ResponseInner[]**](../Model/GetRateSources200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `invoiceCheckout()`

```php
invoiceCheckout($invoice_id, $lang)
```

Invoice checkout

View the checkout page of an invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MiscelleneousApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$invoice_id = 'invoice_id_example'; // string | The invoice ID
$lang = 'lang_example'; // string | The preferred language of the checkout page. You can use \"auto\" to use the language of the customer's browser or see the list of language codes with [this operation](#operation/langCodes).

try {
    $apiInstance->invoiceCheckout($invoice_id, $lang);
} catch (Exception $e) {
    echo 'Exception when calling MiscelleneousApi->invoiceCheckout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**| The invoice ID | |
| **lang** | **string**| The preferred language of the checkout page. You can use \&quot;auto\&quot; to use the language of the customer&#39;s browser or see the list of language codes with [this operation](#operation/langCodes). | [optional] |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/html`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `langCodes()`

```php
langCodes(): \OpenAPI\Client\Model\LangCodes200ResponseInner[]
```

Language codes

The supported language codes

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MiscelleneousApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->langCodes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MiscelleneousApi->langCodes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\LangCodes200ResponseInner[]**](../Model/LangCodes200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `permissionsMetadata()`

```php
permissionsMetadata(): \OpenAPI\Client\Model\PermissionsMetadata200ResponseInner[]
```

Permissions metadata

The metadata of available permissions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MiscelleneousApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->permissionsMetadata();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MiscelleneousApi->permissionsMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\PermissionsMetadata200ResponseInner[]**](../Model/PermissionsMetadata200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
