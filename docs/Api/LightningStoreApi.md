# OpenAPI\Client\LightningStoreApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**storeLightningNodeApiConnectToNode()**](LightningStoreApi.md#storeLightningNodeApiConnectToNode) | **POST** /api/v1/stores/{storeId}/lightning/{cryptoCode}/connect | Connect to lightning node |
| [**storeLightningNodeApiCreateInvoice()**](LightningStoreApi.md#storeLightningNodeApiCreateInvoice) | **POST** /api/v1/stores/{storeId}/lightning/{cryptoCode}/invoices | Create lightning invoice |
| [**storeLightningNodeApiGetBalance()**](LightningStoreApi.md#storeLightningNodeApiGetBalance) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/balance | Get node balance |
| [**storeLightningNodeApiGetChannels()**](LightningStoreApi.md#storeLightningNodeApiGetChannels) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/channels | Get channels |
| [**storeLightningNodeApiGetDepositAddress()**](LightningStoreApi.md#storeLightningNodeApiGetDepositAddress) | **POST** /api/v1/stores/{storeId}/lightning/{cryptoCode}/address | Get deposit address |
| [**storeLightningNodeApiGetHistogram()**](LightningStoreApi.md#storeLightningNodeApiGetHistogram) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/histogram | Get node balance histogram |
| [**storeLightningNodeApiGetInfo()**](LightningStoreApi.md#storeLightningNodeApiGetInfo) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/info | Get node information |
| [**storeLightningNodeApiGetInvoice()**](LightningStoreApi.md#storeLightningNodeApiGetInvoice) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/invoices/{id} | Get invoice |
| [**storeLightningNodeApiGetInvoices()**](LightningStoreApi.md#storeLightningNodeApiGetInvoices) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/invoices | Get invoices |
| [**storeLightningNodeApiGetPayment()**](LightningStoreApi.md#storeLightningNodeApiGetPayment) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/payments/{paymentHash} | Get payment |
| [**storeLightningNodeApiGetPayments()**](LightningStoreApi.md#storeLightningNodeApiGetPayments) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/payments | Get payments |
| [**storeLightningNodeApiOpenChannel()**](LightningStoreApi.md#storeLightningNodeApiOpenChannel) | **POST** /api/v1/stores/{storeId}/lightning/{cryptoCode}/channels | Open channel |
| [**storeLightningNodeApiPayInvoice()**](LightningStoreApi.md#storeLightningNodeApiPayInvoice) | **POST** /api/v1/stores/{storeId}/lightning/{cryptoCode}/invoices/pay | Pay Lightning Invoice |


## `storeLightningNodeApiConnectToNode()`

```php
storeLightningNodeApiConnectToNode($crypto_code, $store_id, $connect_to_node_request)
```

Connect to lightning node

Connect to another lightning node.

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


$apiInstance = new OpenAPI\Client\Api\LightningStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$store_id = 'store_id_example'; // string | The store ID
$connect_to_node_request = new \OpenAPI\Client\Model\ConnectToNodeRequest(); // \OpenAPI\Client\Model\ConnectToNodeRequest

try {
    $apiInstance->storeLightningNodeApiConnectToNode($crypto_code, $store_id, $connect_to_node_request);
} catch (Exception $e) {
    echo 'Exception when calling LightningStoreApi->storeLightningNodeApiConnectToNode: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
| **store_id** | **string**| The store ID | |
| **connect_to_node_request** | [**\OpenAPI\Client\Model\ConnectToNodeRequest**](../Model/ConnectToNodeRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningNodeApiCreateInvoice()`

```php
storeLightningNodeApiCreateInvoice($crypto_code, $store_id, $create_lightning_invoice_request): \OpenAPI\Client\Model\LightningInvoiceData
```

Create lightning invoice

Create a lightning invoice.

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


$apiInstance = new OpenAPI\Client\Api\LightningStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$store_id = 'store_id_example'; // string | The store ID
$create_lightning_invoice_request = new \OpenAPI\Client\Model\CreateLightningInvoiceRequest(); // \OpenAPI\Client\Model\CreateLightningInvoiceRequest

try {
    $result = $apiInstance->storeLightningNodeApiCreateInvoice($crypto_code, $store_id, $create_lightning_invoice_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningStoreApi->storeLightningNodeApiCreateInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
| **store_id** | **string**| The store ID | |
| **create_lightning_invoice_request** | [**\OpenAPI\Client\Model\CreateLightningInvoiceRequest**](../Model/CreateLightningInvoiceRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\LightningInvoiceData**](../Model/LightningInvoiceData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningNodeApiGetBalance()`

```php
storeLightningNodeApiGetBalance($crypto_code, $store_id): \OpenAPI\Client\Model\LightningNodeBalanceData
```

Get node balance

View balance of the lightning node

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


$apiInstance = new OpenAPI\Client\Api\LightningStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->storeLightningNodeApiGetBalance($crypto_code, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningStoreApi->storeLightningNodeApiGetBalance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\LightningNodeBalanceData**](../Model/LightningNodeBalanceData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningNodeApiGetChannels()`

```php
storeLightningNodeApiGetChannels($crypto_code, $store_id): \OpenAPI\Client\Model\LightningChannelData[]
```

Get channels

View information about the current channels of the lightning node

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


$apiInstance = new OpenAPI\Client\Api\LightningStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->storeLightningNodeApiGetChannels($crypto_code, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningStoreApi->storeLightningNodeApiGetChannels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\LightningChannelData[]**](../Model/LightningChannelData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningNodeApiGetDepositAddress()`

```php
storeLightningNodeApiGetDepositAddress($store_id, $crypto_code): string
```

Get deposit address

Get an on-chain deposit address for the lightning node

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


$apiInstance = new OpenAPI\Client\Api\LightningStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query

try {
    $result = $apiInstance->storeLightningNodeApiGetDepositAddress($store_id, $crypto_code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningStoreApi->storeLightningNodeApiGetDepositAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |

### Return type

**string**

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningNodeApiGetHistogram()`

```php
storeLightningNodeApiGetHistogram($crypto_code, $store_id): \OpenAPI\Client\Model\HistogramData
```

Get node balance histogram

View balance histogram of the lightning node

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


$apiInstance = new OpenAPI\Client\Api\LightningStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->storeLightningNodeApiGetHistogram($crypto_code, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningStoreApi->storeLightningNodeApiGetHistogram: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
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

## `storeLightningNodeApiGetInfo()`

```php
storeLightningNodeApiGetInfo($crypto_code, $store_id): \OpenAPI\Client\Model\LightningNodeInformationData
```

Get node information

View information about the lightning node

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


$apiInstance = new OpenAPI\Client\Api\LightningStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->storeLightningNodeApiGetInfo($crypto_code, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningStoreApi->storeLightningNodeApiGetInfo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\LightningNodeInformationData**](../Model/LightningNodeInformationData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningNodeApiGetInvoice()`

```php
storeLightningNodeApiGetInvoice($crypto_code, $store_id, $id): \OpenAPI\Client\Model\LightningInvoiceData
```

Get invoice

View information about the requested lightning invoice

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


$apiInstance = new OpenAPI\Client\Api\LightningStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$store_id = 'store_id_example'; // string | The store ID
$id = 'id_example'; // string | The id of the lightning invoice.

try {
    $result = $apiInstance->storeLightningNodeApiGetInvoice($crypto_code, $store_id, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningStoreApi->storeLightningNodeApiGetInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
| **store_id** | **string**| The store ID | |
| **id** | **string**| The id of the lightning invoice. | |

### Return type

[**\OpenAPI\Client\Model\LightningInvoiceData**](../Model/LightningInvoiceData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningNodeApiGetInvoices()`

```php
storeLightningNodeApiGetInvoices($crypto_code, $store_id, $pending_only, $offset_index): \OpenAPI\Client\Model\LightningInvoiceData[]
```

Get invoices

View information about the lightning invoices

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


$apiInstance = new OpenAPI\Client\Api\LightningStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$store_id = 'store_id_example'; // string | The store ID
$pending_only = false; // bool | Limit to pending invoices only
$offset_index = 0; // float | The index of an invoice that will be used as the start of the list

try {
    $result = $apiInstance->storeLightningNodeApiGetInvoices($crypto_code, $store_id, $pending_only, $offset_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningStoreApi->storeLightningNodeApiGetInvoices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
| **store_id** | **string**| The store ID | |
| **pending_only** | **bool**| Limit to pending invoices only | [optional] [default to false] |
| **offset_index** | **float**| The index of an invoice that will be used as the start of the list | [optional] [default to 0] |

### Return type

[**\OpenAPI\Client\Model\LightningInvoiceData[]**](../Model/LightningInvoiceData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningNodeApiGetPayment()`

```php
storeLightningNodeApiGetPayment($crypto_code, $store_id, $payment_hash): \OpenAPI\Client\Model\LightningPaymentData
```

Get payment

View information about the requested lightning payment

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


$apiInstance = new OpenAPI\Client\Api\LightningStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$store_id = 'store_id_example'; // string | The store ID
$payment_hash = 'payment_hash_example'; // string | The payment hash of the lightning payment.

try {
    $result = $apiInstance->storeLightningNodeApiGetPayment($crypto_code, $store_id, $payment_hash);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningStoreApi->storeLightningNodeApiGetPayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
| **store_id** | **string**| The store ID | |
| **payment_hash** | **string**| The payment hash of the lightning payment. | |

### Return type

[**\OpenAPI\Client\Model\LightningPaymentData**](../Model/LightningPaymentData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningNodeApiGetPayments()`

```php
storeLightningNodeApiGetPayments($crypto_code, $store_id, $include_pending, $offset_index): \OpenAPI\Client\Model\LightningPaymentData[]
```

Get payments

View information about the lightning payments

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


$apiInstance = new OpenAPI\Client\Api\LightningStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$store_id = 'store_id_example'; // string | The store ID
$include_pending = false; // bool | Also include pending payments
$offset_index = 0; // float | The index of an invoice that will be used as the start of the list

try {
    $result = $apiInstance->storeLightningNodeApiGetPayments($crypto_code, $store_id, $include_pending, $offset_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningStoreApi->storeLightningNodeApiGetPayments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
| **store_id** | **string**| The store ID | |
| **include_pending** | **bool**| Also include pending payments | [optional] [default to false] |
| **offset_index** | **float**| The index of an invoice that will be used as the start of the list | [optional] [default to 0] |

### Return type

[**\OpenAPI\Client\Model\LightningPaymentData[]**](../Model/LightningPaymentData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningNodeApiOpenChannel()`

```php
storeLightningNodeApiOpenChannel($crypto_code, $store_id, $open_lightning_channel_request)
```

Open channel

Open a channel with another lightning node. You should connect to that node first.

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


$apiInstance = new OpenAPI\Client\Api\LightningStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$store_id = 'store_id_example'; // string | The store ID
$open_lightning_channel_request = new \OpenAPI\Client\Model\OpenLightningChannelRequest(); // \OpenAPI\Client\Model\OpenLightningChannelRequest

try {
    $apiInstance->storeLightningNodeApiOpenChannel($crypto_code, $store_id, $open_lightning_channel_request);
} catch (Exception $e) {
    echo 'Exception when calling LightningStoreApi->storeLightningNodeApiOpenChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
| **store_id** | **string**| The store ID | |
| **open_lightning_channel_request** | [**\OpenAPI\Client\Model\OpenLightningChannelRequest**](../Model/OpenLightningChannelRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storeLightningNodeApiPayInvoice()`

```php
storeLightningNodeApiPayInvoice($crypto_code, $store_id, $pay_lightning_invoice_request): \OpenAPI\Client\Model\LightningPaymentData
```

Pay Lightning Invoice

Pay a lightning invoice. In case the payment response times out, the status will be reported as pending and the final status can be resolved using the [Get payment](#operation/StoreLightningNodeApi_GetPayment) endpoint. The default wait time for payment responses is 30 seconds — it might take longer if multiple routes are tried or a hold invoice is getting paid.

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


$apiInstance = new OpenAPI\Client\Api\LightningStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$store_id = 'store_id_example'; // string | The store ID
$pay_lightning_invoice_request = new \OpenAPI\Client\Model\PayLightningInvoiceRequest(); // \OpenAPI\Client\Model\PayLightningInvoiceRequest

try {
    $result = $apiInstance->storeLightningNodeApiPayInvoice($crypto_code, $store_id, $pay_lightning_invoice_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningStoreApi->storeLightningNodeApiPayInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
| **store_id** | **string**| The store ID | |
| **pay_lightning_invoice_request** | [**\OpenAPI\Client\Model\PayLightningInvoiceRequest**](../Model/PayLightningInvoiceRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\LightningPaymentData**](../Model/LightningPaymentData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
