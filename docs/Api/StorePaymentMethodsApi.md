# OpenAPI\Client\StorePaymentMethodsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**storePaymentMethodsDeleteStorePaymentMethod()**](StorePaymentMethodsApi.md#storePaymentMethodsDeleteStorePaymentMethod) | **DELETE** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId} | Delete store&#39;s payment method |
| [**storePaymentMethodsGetStorePaymentMethod()**](StorePaymentMethodsApi.md#storePaymentMethodsGetStorePaymentMethod) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId} | Get store payment method |
| [**storePaymentMethodsGetStorePaymentMethods()**](StorePaymentMethodsApi.md#storePaymentMethodsGetStorePaymentMethods) | **GET** /api/v1/stores/{storeId}/payment-methods | Get store payment methods |
| [**storePaymentMethodsUpdateStorePaymentMethod()**](StorePaymentMethodsApi.md#storePaymentMethodsUpdateStorePaymentMethod) | **PUT** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId} | Update store&#39;s payment method |


## `storePaymentMethodsDeleteStorePaymentMethod()`

```php
storePaymentMethodsDeleteStorePaymentMethod($payment_method_id, $store_id)
```

Delete store's payment method

Delete information about the stores' configured payment method

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


$apiInstance = new OpenAPI\Client\Api\StorePaymentMethodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID

try {
    $apiInstance->storePaymentMethodsDeleteStorePaymentMethod($payment_method_id, $store_id);
} catch (Exception $e) {
    echo 'Exception when calling StorePaymentMethodsApi->storePaymentMethodsDeleteStorePaymentMethod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |

### Return type

void (empty response body)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storePaymentMethodsGetStorePaymentMethod()`

```php
storePaymentMethodsGetStorePaymentMethod($payment_method_id, $store_id, $include_config): \OpenAPI\Client\Model\GenericPaymentMethodData
```

Get store payment method

View information about the stores' configured payment method

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


$apiInstance = new OpenAPI\Client\Api\StorePaymentMethodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$include_config = True; // bool | Fetch the config of the payment methods, if `true`, the permission `btcpay.store.canmodifystoresettings` is required.

try {
    $result = $apiInstance->storePaymentMethodsGetStorePaymentMethod($payment_method_id, $store_id, $include_config);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorePaymentMethodsApi->storePaymentMethodsGetStorePaymentMethod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **include_config** | **bool**| Fetch the config of the payment methods, if &#x60;true&#x60;, the permission &#x60;btcpay.store.canmodifystoresettings&#x60; is required. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GenericPaymentMethodData**](../Model/GenericPaymentMethodData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storePaymentMethodsGetStorePaymentMethods()`

```php
storePaymentMethodsGetStorePaymentMethods($store_id, $only_enabled, $include_config): \OpenAPI\Client\Model\GenericPaymentMethodData[]
```

Get store payment methods

View information about the stores' configured payment methods

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


$apiInstance = new OpenAPI\Client\Api\StorePaymentMethodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$only_enabled = True; // bool | Fetch payment methods that are enabled/disabled only
$include_config = True; // bool | Fetch the config of the payment methods, if `true`, the permission `btcpay.store.canmodifystoresettings` is required.

try {
    $result = $apiInstance->storePaymentMethodsGetStorePaymentMethods($store_id, $only_enabled, $include_config);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorePaymentMethodsApi->storePaymentMethodsGetStorePaymentMethods: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **only_enabled** | **bool**| Fetch payment methods that are enabled/disabled only | [optional] |
| **include_config** | **bool**| Fetch the config of the payment methods, if &#x60;true&#x60;, the permission &#x60;btcpay.store.canmodifystoresettings&#x60; is required. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GenericPaymentMethodData[]**](../Model/GenericPaymentMethodData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storePaymentMethodsUpdateStorePaymentMethod()`

```php
storePaymentMethodsUpdateStorePaymentMethod($payment_method_id, $store_id, $update_payment_method_config): \OpenAPI\Client\Model\GenericPaymentMethodData
```

Update store's payment method

Update information about the stores' configured payment method

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


$apiInstance = new OpenAPI\Client\Api\StorePaymentMethodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$update_payment_method_config = new \OpenAPI\Client\Model\UpdatePaymentMethodConfig(); // \OpenAPI\Client\Model\UpdatePaymentMethodConfig

try {
    $result = $apiInstance->storePaymentMethodsUpdateStorePaymentMethod($payment_method_id, $store_id, $update_payment_method_config);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorePaymentMethodsApi->storePaymentMethodsUpdateStorePaymentMethod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **update_payment_method_config** | [**\OpenAPI\Client\Model\UpdatePaymentMethodConfig**](../Model/UpdatePaymentMethodConfig.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GenericPaymentMethodData**](../Model/GenericPaymentMethodData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
