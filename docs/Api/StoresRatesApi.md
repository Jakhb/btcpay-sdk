# OpenAPI\Client\StoresRatesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**storesGetStoreRateConfiguration()**](StoresRatesApi.md#storesGetStoreRateConfiguration) | **GET** /api/v1/stores/{storeId}/rates/configuration/{rateSource} | Get store rate settings for the specified rate source |
| [**storesGetStoreRates()**](StoresRatesApi.md#storesGetStoreRates) | **GET** /api/v1/stores/{storeId}/rates | Get rates |
| [**storesPreviewStoreRateConfiguration()**](StoresRatesApi.md#storesPreviewStoreRateConfiguration) | **POST** /api/v1/stores/{storeId}/rates/configuration/preview | Preview rate configuration results |
| [**storesUpdateStoreRateConfiguration()**](StoresRatesApi.md#storesUpdateStoreRateConfiguration) | **PUT** /api/v1/stores/{storeId}/rates/configuration/{rateSource} | Get store rate settings for the specified rate source |


## `storesGetStoreRateConfiguration()`

```php
storesGetStoreRateConfiguration($rate_source, $store_id): \OpenAPI\Client\Model\StoreRateConfiguration
```

Get store rate settings for the specified rate source

View rate settings for the specified store and rate source (`primary` or `fallback`).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: Basic
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure API key authorization: API_Key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\StoresRatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rate_source = primary; // string | The rate source to configure (`primary` or `fallback`)
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->storesGetStoreRateConfiguration($rate_source, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresRatesApi->storesGetStoreRateConfiguration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rate_source** | **string**| The rate source to configure (&#x60;primary&#x60; or &#x60;fallback&#x60;) | [default to &#39;primary&#39;] |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\StoreRateConfiguration**](../Model/StoreRateConfiguration.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storesGetStoreRates()`

```php
storesGetStoreRates($store_id, $currency_pair): \OpenAPI\Client\Model\StoreRateResult[]
```

Get rates

Get rates on the store

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: Basic
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure API key authorization: API_Key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\StoresRatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$currency_pair = ["BTC_USD","BTC_EUR"]; // string[] | The currency pairs to fetch rates for

try {
    $result = $apiInstance->storesGetStoreRates($store_id, $currency_pair);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresRatesApi->storesGetStoreRates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **currency_pair** | [**string[]**](../Model/string.md)| The currency pairs to fetch rates for | [optional] |

### Return type

[**\OpenAPI\Client\Model\StoreRateResult[]**](../Model/StoreRateResult.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storesPreviewStoreRateConfiguration()`

```php
storesPreviewStoreRateConfiguration($store_id, $store_rate_configuration, $currency_pair): \OpenAPI\Client\Model\StoreRateResult[]
```

Preview rate configuration results

Preview rate configuration results before you set it on the store

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: Basic
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure API key authorization: API_Key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\StoresRatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$store_rate_configuration = new \OpenAPI\Client\Model\StoreRateConfiguration(); // \OpenAPI\Client\Model\StoreRateConfiguration
$currency_pair = array('currency_pair_example'); // string[] | The currency pairs to preview

try {
    $result = $apiInstance->storesPreviewStoreRateConfiguration($store_id, $store_rate_configuration, $currency_pair);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresRatesApi->storesPreviewStoreRateConfiguration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **store_rate_configuration** | [**\OpenAPI\Client\Model\StoreRateConfiguration**](../Model/StoreRateConfiguration.md)|  | |
| **currency_pair** | [**string[]**](../Model/string.md)| The currency pairs to preview | [optional] |

### Return type

[**\OpenAPI\Client\Model\StoreRateResult[]**](../Model/StoreRateResult.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storesUpdateStoreRateConfiguration()`

```php
storesUpdateStoreRateConfiguration($rate_source, $store_id, $store_rate_configuration): \OpenAPI\Client\Model\StoreRateConfiguration
```

Get store rate settings for the specified rate source

Update rate settings for the specified store and rate source (`primary` or `fallback`).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: Basic
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure API key authorization: API_Key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\StoresRatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rate_source = primary; // string | The rate source to configure (`primary` or `fallback`)
$store_id = 'store_id_example'; // string | The store ID
$store_rate_configuration = new \OpenAPI\Client\Model\StoreRateConfiguration(); // \OpenAPI\Client\Model\StoreRateConfiguration

try {
    $result = $apiInstance->storesUpdateStoreRateConfiguration($rate_source, $store_id, $store_rate_configuration);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresRatesApi->storesUpdateStoreRateConfiguration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rate_source** | **string**| The rate source to configure (&#x60;primary&#x60; or &#x60;fallback&#x60;) | [default to &#39;primary&#39;] |
| **store_id** | **string**| The store ID | |
| **store_rate_configuration** | [**\OpenAPI\Client\Model\StoreRateConfiguration**](../Model/StoreRateConfiguration.md)|  | |

### Return type

[**\OpenAPI\Client\Model\StoreRateConfiguration**](../Model/StoreRateConfiguration.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
