# OpenAPI\Client\StoresEmailApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**storesGetStoreEmailSettings()**](StoresEmailApi.md#storesGetStoreEmailSettings) | **GET** /api/v1/stores/{storeId}/email | Get store email settings |
| [**storesSendStoreEmail()**](StoresEmailApi.md#storesSendStoreEmail) | **POST** /api/v1/stores/{storeId}/email/send | Send an email for a store |
| [**storesUpdateStoreEmailSettings()**](StoresEmailApi.md#storesUpdateStoreEmailSettings) | **PUT** /api/v1/stores/{storeId}/email | Update store email settings |


## `storesGetStoreEmailSettings()`

```php
storesGetStoreEmailSettings($store_id): \OpenAPI\Client\Model\GetEmailSettings
```

Get store email settings

Retrieve the email settings configured for specific store. The password field will be masked if present.

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


$apiInstance = new OpenAPI\Client\Api\StoresEmailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->storesGetStoreEmailSettings($store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresEmailApi->storesGetStoreEmailSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\GetEmailSettings**](../Model/GetEmailSettings.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storesSendStoreEmail()`

```php
storesSendStoreEmail($store_id, $stores_send_store_email_request)
```

Send an email for a store

Send an email using the store's SMTP server

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


$apiInstance = new OpenAPI\Client\Api\StoresEmailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$stores_send_store_email_request = new \OpenAPI\Client\Model\StoresSendStoreEmailRequest(); // \OpenAPI\Client\Model\StoresSendStoreEmailRequest

try {
    $apiInstance->storesSendStoreEmail($store_id, $stores_send_store_email_request);
} catch (Exception $e) {
    echo 'Exception when calling StoresEmailApi->storesSendStoreEmail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **stores_send_store_email_request** | [**\OpenAPI\Client\Model\StoresSendStoreEmailRequest**](../Model/StoresSendStoreEmailRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storesUpdateStoreEmailSettings()`

```php
storesUpdateStoreEmailSettings($store_id, $update_email_settings): \OpenAPI\Client\Model\GetEmailSettings
```

Update store email settings

Update a store's email settings

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


$apiInstance = new OpenAPI\Client\Api\StoresEmailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$update_email_settings = new \OpenAPI\Client\Model\UpdateEmailSettings(); // \OpenAPI\Client\Model\UpdateEmailSettings

try {
    $result = $apiInstance->storesUpdateStoreEmailSettings($store_id, $update_email_settings);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresEmailApi->storesUpdateStoreEmailSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **update_email_settings** | [**\OpenAPI\Client\Model\UpdateEmailSettings**](../Model/UpdateEmailSettings.md)|  | |

### Return type

[**\OpenAPI\Client\Model\GetEmailSettings**](../Model/GetEmailSettings.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
