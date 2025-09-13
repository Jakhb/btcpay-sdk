# OpenAPI\Client\StoresPayoutProcessorsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutProcessorsForPaymentMethod()**](StoresPayoutProcessorsApi.md#greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutProcessorsForPaymentMethod) | **GET** /api/v1/stores/{storeId}/payout-processors/LightningAutomatedPayoutSenderFactory/{payoutMethodId} | Get configured store Lightning automated payout processors |
| [**greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutSenderFactory()**](StoresPayoutProcessorsApi.md#greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutSenderFactory) | **GET** /api/v1/stores/{storeId}/payout-processors/LightningAutomatedPayoutSenderFactory | Get configured store Lightning automated payout processors |
| [**greenfieldStoreAutomatedLightningPayoutProcessorsControllerUpdateStoreLightningAutomatedPayoutProcessor()**](StoresPayoutProcessorsApi.md#greenfieldStoreAutomatedLightningPayoutProcessorsControllerUpdateStoreLightningAutomatedPayoutProcessor) | **PUT** /api/v1/stores/{storeId}/payout-processors/LightningAutomatedPayoutSenderFactory/{payoutMethodId} | Update configured store Lightning automated payout processors |
| [**greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedPayoutProcessorsForPaymentMethod()**](StoresPayoutProcessorsApi.md#greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedPayoutProcessorsForPaymentMethod) | **GET** /api/v1/stores/{storeId}/payout-processors/OnChainAutomatedPayoutSenderFactory/{paymentMethodId} | Get configured store onchain automated payout processors |
| [**greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedTransferSenderFactory()**](StoresPayoutProcessorsApi.md#greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedTransferSenderFactory) | **GET** /api/v1/stores/{storeId}/payout-processors/OnChainAutomatedTransferSenderFactory | Get configured store onchain automated payout processors |
| [**greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedPayoutProcessorForPaymentMethod()**](StoresPayoutProcessorsApi.md#greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedPayoutProcessorForPaymentMethod) | **PUT** /api/v1/stores/{storeId}/payout-processors/OnChainAutomatedPayoutSenderFactory/{paymentMethodId} | Update configured store onchain automated payout processors |
| [**greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedTransferSenderFactory()**](StoresPayoutProcessorsApi.md#greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedTransferSenderFactory) | **PUT** /api/v1/stores/{storeId}/payout-processors/OnChainAutomatedTransferSenderFactory | Update configured store onchain automated payout processors |
| [**storePayoutProcessorsGetStorePayoutProcessors()**](StoresPayoutProcessorsApi.md#storePayoutProcessorsGetStorePayoutProcessors) | **GET** /api/v1/stores/{storeId}/payout-processors | Get store configured payout processors |
| [**storePayoutProcessorsRemoveStorePayoutProcessor()**](StoresPayoutProcessorsApi.md#storePayoutProcessorsRemoveStorePayoutProcessor) | **DELETE** /api/v1/stores/{storeId}/payout-processors/{processor}/{paymentMethodId} | Remove store configured payout processor |


## `greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutProcessorsForPaymentMethod()`

```php
greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutProcessorsForPaymentMethod($payout_method_id, $store_id): \OpenAPI\Client\Model\LightningAutomatedTransferSettings[]
```

Get configured store Lightning automated payout processors

Get configured store Lightning automated payout processors

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutProcessorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payout_method_id = BTC-CHAIN; // string | The payout method id
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutProcessorsForPaymentMethod($payout_method_id, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutProcessorsApi->greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutProcessorsForPaymentMethod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payout_method_id** | **string**| The payout method id | |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\LightningAutomatedTransferSettings[]**](../Model/LightningAutomatedTransferSettings.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutSenderFactory()`

```php
greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutSenderFactory($store_id): \OpenAPI\Client\Model\LightningAutomatedTransferSettings[]
```

Get configured store Lightning automated payout processors

Get configured store Lightning automated payout processors

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutProcessorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutSenderFactory($store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutProcessorsApi->greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutSenderFactory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\LightningAutomatedTransferSettings[]**](../Model/LightningAutomatedTransferSettings.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `greenfieldStoreAutomatedLightningPayoutProcessorsControllerUpdateStoreLightningAutomatedPayoutProcessor()`

```php
greenfieldStoreAutomatedLightningPayoutProcessorsControllerUpdateStoreLightningAutomatedPayoutProcessor($payout_method_id, $store_id, $update_lightning_automated_transfer_settings): \OpenAPI\Client\Model\LightningAutomatedTransferSettings
```

Update configured store Lightning automated payout processors

Update configured store Lightning automated payout processors

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutProcessorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payout_method_id = BTC-CHAIN; // string | The payout method id
$store_id = 'store_id_example'; // string | The store ID
$update_lightning_automated_transfer_settings = new \OpenAPI\Client\Model\UpdateLightningAutomatedTransferSettings(); // \OpenAPI\Client\Model\UpdateLightningAutomatedTransferSettings

try {
    $result = $apiInstance->greenfieldStoreAutomatedLightningPayoutProcessorsControllerUpdateStoreLightningAutomatedPayoutProcessor($payout_method_id, $store_id, $update_lightning_automated_transfer_settings);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutProcessorsApi->greenfieldStoreAutomatedLightningPayoutProcessorsControllerUpdateStoreLightningAutomatedPayoutProcessor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payout_method_id** | **string**| The payout method id | |
| **store_id** | **string**| The store ID | |
| **update_lightning_automated_transfer_settings** | [**\OpenAPI\Client\Model\UpdateLightningAutomatedTransferSettings**](../Model/UpdateLightningAutomatedTransferSettings.md)|  | |

### Return type

[**\OpenAPI\Client\Model\LightningAutomatedTransferSettings**](../Model/LightningAutomatedTransferSettings.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedPayoutProcessorsForPaymentMethod()`

```php
greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedPayoutProcessorsForPaymentMethod($payment_method_id, $store_id): \OpenAPI\Client\Model\OnChainAutomatedTransferSettings[]
```

Get configured store onchain automated payout processors

Get configured store onchain automated payout processors

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutProcessorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedPayoutProcessorsForPaymentMethod($payment_method_id, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutProcessorsApi->greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedPayoutProcessorsForPaymentMethod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\OnChainAutomatedTransferSettings[]**](../Model/OnChainAutomatedTransferSettings.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedTransferSenderFactory()`

```php
greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedTransferSenderFactory($store_id): \OpenAPI\Client\Model\OnChainAutomatedTransferSettings[]
```

Get configured store onchain automated payout processors

Get configured store onchain automated payout processors

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutProcessorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedTransferSenderFactory($store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutProcessorsApi->greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedTransferSenderFactory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\OnChainAutomatedTransferSettings[]**](../Model/OnChainAutomatedTransferSettings.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedPayoutProcessorForPaymentMethod()`

```php
greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedPayoutProcessorForPaymentMethod($payment_method_id, $store_id, $update_on_chain_automated_transfer_settings): \OpenAPI\Client\Model\OnChainAutomatedTransferSettings
```

Update configured store onchain automated payout processors

Update configured store onchain automated payout processors

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutProcessorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$update_on_chain_automated_transfer_settings = new \OpenAPI\Client\Model\UpdateOnChainAutomatedTransferSettings(); // \OpenAPI\Client\Model\UpdateOnChainAutomatedTransferSettings

try {
    $result = $apiInstance->greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedPayoutProcessorForPaymentMethod($payment_method_id, $store_id, $update_on_chain_automated_transfer_settings);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutProcessorsApi->greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedPayoutProcessorForPaymentMethod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **update_on_chain_automated_transfer_settings** | [**\OpenAPI\Client\Model\UpdateOnChainAutomatedTransferSettings**](../Model/UpdateOnChainAutomatedTransferSettings.md)|  | |

### Return type

[**\OpenAPI\Client\Model\OnChainAutomatedTransferSettings**](../Model/OnChainAutomatedTransferSettings.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedTransferSenderFactory()`

```php
greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedTransferSenderFactory($store_id, $update_on_chain_automated_transfer_settings): \OpenAPI\Client\Model\OnChainAutomatedTransferSettings
```

Update configured store onchain automated payout processors

Update configured store onchain automated payout processors

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutProcessorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$update_on_chain_automated_transfer_settings = new \OpenAPI\Client\Model\UpdateOnChainAutomatedTransferSettings(); // \OpenAPI\Client\Model\UpdateOnChainAutomatedTransferSettings

try {
    $result = $apiInstance->greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedTransferSenderFactory($store_id, $update_on_chain_automated_transfer_settings);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutProcessorsApi->greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedTransferSenderFactory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **update_on_chain_automated_transfer_settings** | [**\OpenAPI\Client\Model\UpdateOnChainAutomatedTransferSettings**](../Model/UpdateOnChainAutomatedTransferSettings.md)|  | |

### Return type

[**\OpenAPI\Client\Model\OnChainAutomatedTransferSettings**](../Model/OnChainAutomatedTransferSettings.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storePayoutProcessorsGetStorePayoutProcessors()`

```php
storePayoutProcessorsGetStorePayoutProcessors($store_id): \OpenAPI\Client\Model\PayoutProcessorData[]
```

Get store configured payout processors

Get store configured payout processors

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutProcessorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->storePayoutProcessorsGetStorePayoutProcessors($store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutProcessorsApi->storePayoutProcessorsGetStorePayoutProcessors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\PayoutProcessorData[]**](../Model/PayoutProcessorData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storePayoutProcessorsRemoveStorePayoutProcessor()`

```php
storePayoutProcessorsRemoveStorePayoutProcessor($payment_method_id, $store_id, $processor)
```

Remove store configured payout processor

Remove store configured payout processor

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutProcessorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$processor = 'processor_example'; // string | The processor

try {
    $apiInstance->storePayoutProcessorsRemoveStorePayoutProcessor($payment_method_id, $store_id, $processor);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutProcessorsApi->storePayoutProcessorsRemoveStorePayoutProcessor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **processor** | **string**| The processor | |

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
