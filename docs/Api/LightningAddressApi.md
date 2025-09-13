# OpenAPI\Client\LightningAddressApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**storeLightningAddressesAddOrUpdateStoreLightningAddress()**](LightningAddressApi.md#storeLightningAddressesAddOrUpdateStoreLightningAddress) | **POST** /api/v1/stores/{storeId}/lightning-addresses/{username} | Add or update store configured lightning address |
| [**storeLightningAddressesGetStoreLightningAddress()**](LightningAddressApi.md#storeLightningAddressesGetStoreLightningAddress) | **GET** /api/v1/stores/{storeId}/lightning-addresses/{username} | Get store configured lightning address |
| [**storeLightningAddressesGetStoreLightningAddresses()**](LightningAddressApi.md#storeLightningAddressesGetStoreLightningAddresses) | **GET** /api/v1/stores/{storeId}/lightning-addresses | Get store configured lightning addresses |
| [**storeLightningAddressesRemoveStoreLightningAddress()**](LightningAddressApi.md#storeLightningAddressesRemoveStoreLightningAddress) | **DELETE** /api/v1/stores/{storeId}/lightning-addresses/{username} | Remove configured lightning address |


## `storeLightningAddressesAddOrUpdateStoreLightningAddress()`

```php
storeLightningAddressesAddOrUpdateStoreLightningAddress($store_id, $username, $lightning_address_data): \OpenAPI\Client\Model\LightningAddressData
```

Add or update store configured lightning address

Add or update store configured lightning address

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


$apiInstance = new OpenAPI\Client\Api\LightningAddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$username = 'username_example'; // string | the lightning address username
$lightning_address_data = new \OpenAPI\Client\Model\LightningAddressData(); // \OpenAPI\Client\Model\LightningAddressData

try {
    $result = $apiInstance->storeLightningAddressesAddOrUpdateStoreLightningAddress($store_id, $username, $lightning_address_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningAddressApi->storeLightningAddressesAddOrUpdateStoreLightningAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **username** | **string**| the lightning address username | |
| **lightning_address_data** | [**\OpenAPI\Client\Model\LightningAddressData**](../Model/LightningAddressData.md)|  | |

### Return type

[**\OpenAPI\Client\Model\LightningAddressData**](../Model/LightningAddressData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningAddressesGetStoreLightningAddress()`

```php
storeLightningAddressesGetStoreLightningAddress($store_id, $username): \OpenAPI\Client\Model\LightningAddressData
```

Get store configured lightning address

Get store configured lightning address

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


$apiInstance = new OpenAPI\Client\Api\LightningAddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$username = 'username_example'; // string | The lightning address username

try {
    $result = $apiInstance->storeLightningAddressesGetStoreLightningAddress($store_id, $username);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningAddressApi->storeLightningAddressesGetStoreLightningAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **username** | **string**| The lightning address username | |

### Return type

[**\OpenAPI\Client\Model\LightningAddressData**](../Model/LightningAddressData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningAddressesGetStoreLightningAddresses()`

```php
storeLightningAddressesGetStoreLightningAddresses($store_id): \OpenAPI\Client\Model\LightningAddressData[]
```

Get store configured lightning addresses

Get store configured lightning addresses

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


$apiInstance = new OpenAPI\Client\Api\LightningAddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->storeLightningAddressesGetStoreLightningAddresses($store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningAddressApi->storeLightningAddressesGetStoreLightningAddresses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\LightningAddressData[]**](../Model/LightningAddressData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningAddressesRemoveStoreLightningAddress()`

```php
storeLightningAddressesRemoveStoreLightningAddress($store_id, $username)
```

Remove configured lightning address

Remove store configured lightning address

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


$apiInstance = new OpenAPI\Client\Api\LightningAddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$username = 'username_example'; // string | The lightning address username

try {
    $apiInstance->storeLightningAddressesRemoveStoreLightningAddress($store_id, $username);
} catch (Exception $e) {
    echo 'Exception when calling LightningAddressApi->storeLightningAddressesRemoveStoreLightningAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **username** | **string**| The lightning address username | |

### Return type

void (empty response body)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
