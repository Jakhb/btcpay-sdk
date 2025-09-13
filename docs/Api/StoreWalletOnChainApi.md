# OpenAPI\Client\StoreWalletOnChainApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**storeOnChainPaymentMethodsGenerateOnChainWallet()**](StoreWalletOnChainApi.md#storeOnChainPaymentMethodsGenerateOnChainWallet) | **POST** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/generate | Generate store on-chain wallet |
| [**storeOnChainPaymentMethodsGetOnChainPaymentMethodPreview()**](StoreWalletOnChainApi.md#storeOnChainPaymentMethodsGetOnChainPaymentMethodPreview) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/preview | Preview store on-chain payment method addresses |
| [**storeOnChainPaymentMethodsPOSTOnChainPaymentMethodPreview()**](StoreWalletOnChainApi.md#storeOnChainPaymentMethodsPOSTOnChainPaymentMethodPreview) | **POST** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/preview | Preview proposed store on-chain payment method addresses |
| [**storeOnChainWalletsAddOrUpdateOnChainWalletLink()**](StoreWalletOnChainApi.md#storeOnChainWalletsAddOrUpdateOnChainWalletLink) | **POST** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/objects/{objectType}/{objectId}/links | Add/Update store on-chain wallet object link |
| [**storeOnChainWalletsAddOrUpdateOnChainWalletObjects()**](StoreWalletOnChainApi.md#storeOnChainWalletsAddOrUpdateOnChainWalletObjects) | **POST** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/objects | Add/Update store on-chain wallet objects |
| [**storeOnChainWalletsCreateOnChainTransaction()**](StoreWalletOnChainApi.md#storeOnChainWalletsCreateOnChainTransaction) | **POST** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/transactions | Create store on-chain wallet transaction |
| [**storeOnChainWalletsGetOnChainFeeRate()**](StoreWalletOnChainApi.md#storeOnChainWalletsGetOnChainFeeRate) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/feerate | Get store on-chain wallet fee rate |
| [**storeOnChainWalletsGetOnChainWalletObject()**](StoreWalletOnChainApi.md#storeOnChainWalletsGetOnChainWalletObject) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/objects/{objectType}/{objectId} | Get store on-chain wallet object |
| [**storeOnChainWalletsGetOnChainWalletObjects()**](StoreWalletOnChainApi.md#storeOnChainWalletsGetOnChainWalletObjects) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/objects | Get store on-chain wallet objects |
| [**storeOnChainWalletsGetOnChainWalletReceiveAddress()**](StoreWalletOnChainApi.md#storeOnChainWalletsGetOnChainWalletReceiveAddress) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/address | Get store on-chain wallet address |
| [**storeOnChainWalletsGetOnChainWalletTransaction()**](StoreWalletOnChainApi.md#storeOnChainWalletsGetOnChainWalletTransaction) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/transactions/{transactionId} | Get store on-chain wallet transaction |
| [**storeOnChainWalletsGetOnChainWalletUTXOs()**](StoreWalletOnChainApi.md#storeOnChainWalletsGetOnChainWalletUTXOs) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/utxos | Get store on-chain wallet UTXOS |
| [**storeOnChainWalletsPatchOnChainWalletTransaction()**](StoreWalletOnChainApi.md#storeOnChainWalletsPatchOnChainWalletTransaction) | **PATCH** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/transactions/{transactionId} | Patch store on-chain wallet transaction info |
| [**storeOnChainWalletsRemoveOnChainWalletLink()**](StoreWalletOnChainApi.md#storeOnChainWalletsRemoveOnChainWalletLink) | **DELETE** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/objects/{objectType}/{objectId}/links/{linkType}/{linkId} | Remove store on-chain wallet object links |
| [**storeOnChainWalletsRemoveOnChainWalletObject()**](StoreWalletOnChainApi.md#storeOnChainWalletsRemoveOnChainWalletObject) | **DELETE** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/objects/{objectType}/{objectId} | Remove store on-chain wallet objects |
| [**storeOnChainWalletsShowOnChainWalletHistogram()**](StoreWalletOnChainApi.md#storeOnChainWalletsShowOnChainWalletHistogram) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/histogram | Get store on-chain wallet balance histogram |
| [**storeOnChainWalletsShowOnChainWalletOverview()**](StoreWalletOnChainApi.md#storeOnChainWalletsShowOnChainWalletOverview) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet | Get store on-chain wallet overview |
| [**storeOnChainWalletsShowOnChainWalletTransactions()**](StoreWalletOnChainApi.md#storeOnChainWalletsShowOnChainWalletTransactions) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/transactions | Get store on-chain wallet transactions |
| [**storeOnChainWalletsUnReserveOnChainWalletReceiveAddress()**](StoreWalletOnChainApi.md#storeOnChainWalletsUnReserveOnChainWalletReceiveAddress) | **DELETE** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/address | UnReserve last store on-chain wallet address |


## `storeOnChainPaymentMethodsGenerateOnChainWallet()`

```php
storeOnChainPaymentMethodsGenerateOnChainWallet($payment_method_id, $store_id, $generate_on_chain_wallet_request): \OpenAPI\Client\Model\StoreOnChainPaymentMethodsGenerateOnChainWallet200Response
```

Generate store on-chain wallet

Generate a wallet and update the specified store's payment method to it

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$generate_on_chain_wallet_request = new \OpenAPI\Client\Model\GenerateOnChainWalletRequest(); // \OpenAPI\Client\Model\GenerateOnChainWalletRequest

try {
    $result = $apiInstance->storeOnChainPaymentMethodsGenerateOnChainWallet($payment_method_id, $store_id, $generate_on_chain_wallet_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainPaymentMethodsGenerateOnChainWallet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **generate_on_chain_wallet_request** | [**\OpenAPI\Client\Model\GenerateOnChainWalletRequest**](../Model/GenerateOnChainWalletRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\StoreOnChainPaymentMethodsGenerateOnChainWallet200Response**](../Model/StoreOnChainPaymentMethodsGenerateOnChainWallet200Response.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainPaymentMethodsGetOnChainPaymentMethodPreview()`

```php
storeOnChainPaymentMethodsGetOnChainPaymentMethodPreview($store_id, $payment_method_id, $offset, $count): \OpenAPI\Client\Model\OnChainPaymentMethodPreviewResultData
```

Preview store on-chain payment method addresses

View addresses of the current payment method of the store

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$offset = 3.4; // float | From which index to fetch the addresses
$count = 3.4; // float | Number of addresses to preview

try {
    $result = $apiInstance->storeOnChainPaymentMethodsGetOnChainPaymentMethodPreview($store_id, $payment_method_id, $offset, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainPaymentMethodsGetOnChainPaymentMethodPreview: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **offset** | **float**| From which index to fetch the addresses | [optional] |
| **count** | **float**| Number of addresses to preview | [optional] |

### Return type

[**\OpenAPI\Client\Model\OnChainPaymentMethodPreviewResultData**](../Model/OnChainPaymentMethodPreviewResultData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainPaymentMethodsPOSTOnChainPaymentMethodPreview()`

```php
storeOnChainPaymentMethodsPOSTOnChainPaymentMethodPreview($payment_method_id, $store_id, $store_on_chain_payment_methods_poston_chain_payment_method_preview_request, $offset, $count): \OpenAPI\Client\Model\OnChainPaymentMethodPreviewResultData
```

Preview proposed store on-chain payment method addresses

View addresses of a proposed payment method of the store

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$store_on_chain_payment_methods_poston_chain_payment_method_preview_request = new \OpenAPI\Client\Model\StoreOnChainPaymentMethodsPOSTOnChainPaymentMethodPreviewRequest(); // \OpenAPI\Client\Model\StoreOnChainPaymentMethodsPOSTOnChainPaymentMethodPreviewRequest
$offset = 3.4; // float | From which index to fetch the addresses
$count = 3.4; // float | Number of addresses to preview

try {
    $result = $apiInstance->storeOnChainPaymentMethodsPOSTOnChainPaymentMethodPreview($payment_method_id, $store_id, $store_on_chain_payment_methods_poston_chain_payment_method_preview_request, $offset, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainPaymentMethodsPOSTOnChainPaymentMethodPreview: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **store_on_chain_payment_methods_poston_chain_payment_method_preview_request** | [**\OpenAPI\Client\Model\StoreOnChainPaymentMethodsPOSTOnChainPaymentMethodPreviewRequest**](../Model/StoreOnChainPaymentMethodsPOSTOnChainPaymentMethodPreviewRequest.md)|  | |
| **offset** | **float**| From which index to fetch the addresses | [optional] |
| **count** | **float**| Number of addresses to preview | [optional] |

### Return type

[**\OpenAPI\Client\Model\OnChainPaymentMethodPreviewResultData**](../Model/OnChainPaymentMethodPreviewResultData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainWalletsAddOrUpdateOnChainWalletLink()`

```php
storeOnChainWalletsAddOrUpdateOnChainWalletLink($payment_method_id, $store_id, $object_id, $object_type, $add_on_chain_wallet_object_link_request)
```

Add/Update store on-chain wallet object link

Add/Update wallet object link

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$object_id = abc392...; // string | The object id to fetch
$object_type = tx; // string | The object type to fetch
$add_on_chain_wallet_object_link_request = new \OpenAPI\Client\Model\AddOnChainWalletObjectLinkRequest(); // \OpenAPI\Client\Model\AddOnChainWalletObjectLinkRequest

try {
    $apiInstance->storeOnChainWalletsAddOrUpdateOnChainWalletLink($payment_method_id, $store_id, $object_id, $object_type, $add_on_chain_wallet_object_link_request);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsAddOrUpdateOnChainWalletLink: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **object_id** | **string**| The object id to fetch | |
| **object_type** | **string**| The object type to fetch | |
| **add_on_chain_wallet_object_link_request** | [**\OpenAPI\Client\Model\AddOnChainWalletObjectLinkRequest**](../Model/AddOnChainWalletObjectLinkRequest.md)|  | |

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

## `storeOnChainWalletsAddOrUpdateOnChainWalletObjects()`

```php
storeOnChainWalletsAddOrUpdateOnChainWalletObjects($payment_method_id, $store_id, $on_chain_wallet_object_data): \OpenAPI\Client\Model\OnChainWalletObjectData
```

Add/Update store on-chain wallet objects

Add/Update wallet objects

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$on_chain_wallet_object_data = new \OpenAPI\Client\Model\OnChainWalletObjectData(); // \OpenAPI\Client\Model\OnChainWalletObjectData

try {
    $result = $apiInstance->storeOnChainWalletsAddOrUpdateOnChainWalletObjects($payment_method_id, $store_id, $on_chain_wallet_object_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsAddOrUpdateOnChainWalletObjects: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **on_chain_wallet_object_data** | [**\OpenAPI\Client\Model\OnChainWalletObjectData**](../Model/OnChainWalletObjectData.md)|  | |

### Return type

[**\OpenAPI\Client\Model\OnChainWalletObjectData**](../Model/OnChainWalletObjectData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainWalletsCreateOnChainTransaction()`

```php
storeOnChainWalletsCreateOnChainTransaction($payment_method_id, $store_id, $create_on_chain_transaction_request): \OpenAPI\Client\Model\StoreOnChainWalletsCreateOnChainTransaction200Response
```

Create store on-chain wallet transaction

Create store on-chain wallet transaction

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$create_on_chain_transaction_request = new \OpenAPI\Client\Model\CreateOnChainTransactionRequest(); // \OpenAPI\Client\Model\CreateOnChainTransactionRequest

try {
    $result = $apiInstance->storeOnChainWalletsCreateOnChainTransaction($payment_method_id, $store_id, $create_on_chain_transaction_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsCreateOnChainTransaction: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **create_on_chain_transaction_request** | [**\OpenAPI\Client\Model\CreateOnChainTransactionRequest**](../Model/CreateOnChainTransactionRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\StoreOnChainWalletsCreateOnChainTransaction200Response**](../Model/StoreOnChainWalletsCreateOnChainTransaction200Response.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainWalletsGetOnChainFeeRate()`

```php
storeOnChainWalletsGetOnChainFeeRate($payment_method_id, $store_id, $block_target): \OpenAPI\Client\Model\OnChainWalletFeeRateData
```

Get store on-chain wallet fee rate

Get wallet onchain fee rate

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$block_target = 3.4; // float | The number of blocks away you are willing to target for confirmation. Defaults to the wallet's configured `RecommendedFeeBlockTarget`

try {
    $result = $apiInstance->storeOnChainWalletsGetOnChainFeeRate($payment_method_id, $store_id, $block_target);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsGetOnChainFeeRate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **block_target** | **float**| The number of blocks away you are willing to target for confirmation. Defaults to the wallet&#39;s configured &#x60;RecommendedFeeBlockTarget&#x60; | [optional] |

### Return type

[**\OpenAPI\Client\Model\OnChainWalletFeeRateData**](../Model/OnChainWalletFeeRateData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainWalletsGetOnChainWalletObject()`

```php
storeOnChainWalletsGetOnChainWalletObject($payment_method_id, $store_id, $object_id, $object_type, $include_neighbour_data): \OpenAPI\Client\Model\OnChainWalletObjectData
```

Get store on-chain wallet object

View wallet object

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$object_id = abc392...; // string | The object id to fetch
$object_type = tx; // string | The object type to fetch
$include_neighbour_data = true; // bool | Whether or not you should include neighbour's node data in the result (ie, `links.objectData`)

try {
    $result = $apiInstance->storeOnChainWalletsGetOnChainWalletObject($payment_method_id, $store_id, $object_id, $object_type, $include_neighbour_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsGetOnChainWalletObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **object_id** | **string**| The object id to fetch | |
| **object_type** | **string**| The object type to fetch | |
| **include_neighbour_data** | **bool**| Whether or not you should include neighbour&#39;s node data in the result (ie, &#x60;links.objectData&#x60;) | [optional] [default to true] |

### Return type

[**\OpenAPI\Client\Model\OnChainWalletObjectData**](../Model/OnChainWalletObjectData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainWalletsGetOnChainWalletObjects()`

```php
storeOnChainWalletsGetOnChainWalletObjects($payment_method_id, $store_id, $ids, $type, $include_neighbour_data): \OpenAPI\Client\Model\OnChainWalletObjectData[]
```

Get store on-chain wallet objects

View wallet objects

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$ids = 03abcde...; // string[] | The ids of objects to fetch, if used, type should be specified
$type = tx; // string | The type of object to fetch
$include_neighbour_data = true; // bool | Whether or not you should include neighbour's node data in the result (ie, `links.objectData`)

try {
    $result = $apiInstance->storeOnChainWalletsGetOnChainWalletObjects($payment_method_id, $store_id, $ids, $type, $include_neighbour_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsGetOnChainWalletObjects: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **ids** | [**string[]**](../Model/string.md)| The ids of objects to fetch, if used, type should be specified | [optional] |
| **type** | **string**| The type of object to fetch | [optional] |
| **include_neighbour_data** | **bool**| Whether or not you should include neighbour&#39;s node data in the result (ie, &#x60;links.objectData&#x60;) | [optional] [default to true] |

### Return type

[**\OpenAPI\Client\Model\OnChainWalletObjectData[]**](../Model/OnChainWalletObjectData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainWalletsGetOnChainWalletReceiveAddress()`

```php
storeOnChainWalletsGetOnChainWalletReceiveAddress($payment_method_id, $store_id, $force_generate): \OpenAPI\Client\Model\OnChainWalletAddressData
```

Get store on-chain wallet address

Get or generate address for wallet

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$force_generate = false; // bool | Whether to generate a new address for this request even if the previous one was not used

try {
    $result = $apiInstance->storeOnChainWalletsGetOnChainWalletReceiveAddress($payment_method_id, $store_id, $force_generate);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsGetOnChainWalletReceiveAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **force_generate** | **bool**| Whether to generate a new address for this request even if the previous one was not used | [optional] [default to false] |

### Return type

[**\OpenAPI\Client\Model\OnChainWalletAddressData**](../Model/OnChainWalletAddressData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainWalletsGetOnChainWalletTransaction()`

```php
storeOnChainWalletsGetOnChainWalletTransaction($payment_method_id, $store_id, $transaction_id): \OpenAPI\Client\Model\OnChainWalletTransactionData
```

Get store on-chain wallet transaction

Get store on-chain wallet transaction

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$transaction_id = 'transaction_id_example'; // string | The transaction id to fetch

try {
    $result = $apiInstance->storeOnChainWalletsGetOnChainWalletTransaction($payment_method_id, $store_id, $transaction_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsGetOnChainWalletTransaction: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **transaction_id** | **string**| The transaction id to fetch | |

### Return type

[**\OpenAPI\Client\Model\OnChainWalletTransactionData**](../Model/OnChainWalletTransactionData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainWalletsGetOnChainWalletUTXOs()`

```php
storeOnChainWalletsGetOnChainWalletUTXOs($payment_method_id, $store_id): \OpenAPI\Client\Model\OnChainWalletUTXOData[]
```

Get store on-chain wallet UTXOS

Get store on-chain wallet utxos

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->storeOnChainWalletsGetOnChainWalletUTXOs($payment_method_id, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsGetOnChainWalletUTXOs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\OnChainWalletUTXOData[]**](../Model/OnChainWalletUTXOData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainWalletsPatchOnChainWalletTransaction()`

```php
storeOnChainWalletsPatchOnChainWalletTransaction($payment_method_id, $store_id, $transaction_id, $patch_on_chain_transaction_request, $force): \OpenAPI\Client\Model\OnChainWalletTransactionData
```

Patch store on-chain wallet transaction info

Patch store on-chain wallet transaction info

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$transaction_id = 'transaction_id_example'; // string | The transaction id to fetch
$patch_on_chain_transaction_request = new \OpenAPI\Client\Model\PatchOnChainTransactionRequest(); // \OpenAPI\Client\Model\PatchOnChainTransactionRequest
$force = 'force_example'; // string | Whether to update the label/comments even if the transaction does not yet exist

try {
    $result = $apiInstance->storeOnChainWalletsPatchOnChainWalletTransaction($payment_method_id, $store_id, $transaction_id, $patch_on_chain_transaction_request, $force);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsPatchOnChainWalletTransaction: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **transaction_id** | **string**| The transaction id to fetch | |
| **patch_on_chain_transaction_request** | [**\OpenAPI\Client\Model\PatchOnChainTransactionRequest**](../Model/PatchOnChainTransactionRequest.md)|  | |
| **force** | **string**| Whether to update the label/comments even if the transaction does not yet exist | [optional] |

### Return type

[**\OpenAPI\Client\Model\OnChainWalletTransactionData**](../Model/OnChainWalletTransactionData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainWalletsRemoveOnChainWalletLink()`

```php
storeOnChainWalletsRemoveOnChainWalletLink($payment_method_id, $store_id, $link_id, $object_id, $link_type, $object_type)
```

Remove store on-chain wallet object links

Remove wallet object link

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$link_id = abc392...; // string | The object id of the linked neighbour
$object_id = abc392...; // string | The object id to fetch
$link_type = tx; // string | The object type of the linked neighbour
$object_type = tx; // string | The object type to fetch

try {
    $apiInstance->storeOnChainWalletsRemoveOnChainWalletLink($payment_method_id, $store_id, $link_id, $object_id, $link_type, $object_type);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsRemoveOnChainWalletLink: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **link_id** | **string**| The object id of the linked neighbour | |
| **object_id** | **string**| The object id to fetch | |
| **link_type** | **string**| The object type of the linked neighbour | |
| **object_type** | **string**| The object type to fetch | |

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

## `storeOnChainWalletsRemoveOnChainWalletObject()`

```php
storeOnChainWalletsRemoveOnChainWalletObject($payment_method_id, $store_id, $object_id, $object_type)
```

Remove store on-chain wallet objects

Remove wallet object

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$object_id = abc392...; // string | The object id to fetch
$object_type = tx; // string | The object type to fetch

try {
    $apiInstance->storeOnChainWalletsRemoveOnChainWalletObject($payment_method_id, $store_id, $object_id, $object_type);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsRemoveOnChainWalletObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **object_id** | **string**| The object id to fetch | |
| **object_type** | **string**| The object type to fetch | |

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

## `storeOnChainWalletsShowOnChainWalletHistogram()`

```php
storeOnChainWalletsShowOnChainWalletHistogram($payment_method_id, $store_id): \OpenAPI\Client\Model\HistogramData
```

Get store on-chain wallet balance histogram

View the balance histogram of the specified wallet

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->storeOnChainWalletsShowOnChainWalletHistogram($payment_method_id, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsShowOnChainWalletHistogram: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\HistogramData**](../Model/HistogramData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainWalletsShowOnChainWalletOverview()`

```php
storeOnChainWalletsShowOnChainWalletOverview($payment_method_id, $store_id): \OpenAPI\Client\Model\OnChainWalletOverviewData
```

Get store on-chain wallet overview

View information about the specified wallet

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->storeOnChainWalletsShowOnChainWalletOverview($payment_method_id, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsShowOnChainWalletOverview: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\OnChainWalletOverviewData**](../Model/OnChainWalletOverviewData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainWalletsShowOnChainWalletTransactions()`

```php
storeOnChainWalletsShowOnChainWalletTransactions($payment_method_id, $store_id, $label_filter, $limit, $skip, $status_filter): \OpenAPI\Client\Model\OnChainWalletTransactionData[]
```

Get store on-chain wallet transactions

Get store on-chain wallet transactions

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID
$label_filter = invoice; // string | Transaction label to filter by
$limit = 56; // int | Maximum number of transactions to return
$skip = 56; // int | Number of transactions to skip from the start
$status_filter = array(new \OpenAPI\Client\Model\\OpenAPI\Client\Model\TransactionStatus()); // \OpenAPI\Client\Model\TransactionStatus[] | Statuses to filter the transactions with

try {
    $result = $apiInstance->storeOnChainWalletsShowOnChainWalletTransactions($payment_method_id, $store_id, $label_filter, $limit, $skip, $status_filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsShowOnChainWalletTransactions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |
| **label_filter** | **string**| Transaction label to filter by | [optional] |
| **limit** | **int**| Maximum number of transactions to return | [optional] |
| **skip** | **int**| Number of transactions to skip from the start | [optional] |
| **status_filter** | [**\OpenAPI\Client\Model\TransactionStatus[]**](../Model/\OpenAPI\Client\Model\TransactionStatus.md)| Statuses to filter the transactions with | [optional] |

### Return type

[**\OpenAPI\Client\Model\OnChainWalletTransactionData[]**](../Model/OnChainWalletTransactionData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeOnChainWalletsUnReserveOnChainWalletReceiveAddress()`

```php
storeOnChainWalletsUnReserveOnChainWalletReceiveAddress($payment_method_id, $store_id)
```

UnReserve last store on-chain wallet address

UnReserve address

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


$apiInstance = new OpenAPI\Client\Api\StoreWalletOnChainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID

try {
    $apiInstance->storeOnChainWalletsUnReserveOnChainWalletReceiveAddress($payment_method_id, $store_id);
} catch (Exception $e) {
    echo 'Exception when calling StoreWalletOnChainApi->storeOnChainWalletsUnReserveOnChainWalletReceiveAddress: ', $e->getMessage(), PHP_EOL;
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
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
