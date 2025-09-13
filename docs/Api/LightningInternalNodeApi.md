# OpenAPI\Client\LightningInternalNodeApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**internalLightningNodeApiConnectToNode()**](LightningInternalNodeApi.md#internalLightningNodeApiConnectToNode) | **POST** /api/v1/server/lightning/{cryptoCode}/connect | Connect to lightning node |
| [**internalLightningNodeApiCreateInvoice()**](LightningInternalNodeApi.md#internalLightningNodeApiCreateInvoice) | **POST** /api/v1/server/lightning/{cryptoCode}/invoices | Create lightning invoice |
| [**internalLightningNodeApiGetBalance()**](LightningInternalNodeApi.md#internalLightningNodeApiGetBalance) | **GET** /api/v1/server/lightning/{cryptoCode}/balance | Get node balance |
| [**internalLightningNodeApiGetChannels()**](LightningInternalNodeApi.md#internalLightningNodeApiGetChannels) | **GET** /api/v1/server/lightning/{cryptoCode}/channels | Get channels |
| [**internalLightningNodeApiGetDepositAddress()**](LightningInternalNodeApi.md#internalLightningNodeApiGetDepositAddress) | **POST** /api/v1/server/lightning/{cryptoCode}/address | Get deposit address |
| [**internalLightningNodeApiGetHistogram()**](LightningInternalNodeApi.md#internalLightningNodeApiGetHistogram) | **GET** /api/v1/server/lightning/{cryptoCode}/histogram | Get node balance histogram |
| [**internalLightningNodeApiGetInfo()**](LightningInternalNodeApi.md#internalLightningNodeApiGetInfo) | **GET** /api/v1/server/lightning/{cryptoCode}/info | Get node information |
| [**internalLightningNodeApiGetInvoice()**](LightningInternalNodeApi.md#internalLightningNodeApiGetInvoice) | **GET** /api/v1/server/lightning/{cryptoCode}/invoices/{id} | Get invoice |
| [**internalLightningNodeApiGetInvoices()**](LightningInternalNodeApi.md#internalLightningNodeApiGetInvoices) | **GET** /api/v1/server/lightning/{cryptoCode}/invoices | Get invoices |
| [**internalLightningNodeApiGetPayment()**](LightningInternalNodeApi.md#internalLightningNodeApiGetPayment) | **GET** /api/v1/server/lightning/{cryptoCode}/payments/{paymentHash} | Get payment |
| [**internalLightningNodeApiGetPayments()**](LightningInternalNodeApi.md#internalLightningNodeApiGetPayments) | **GET** /api/v1/server/lightning/{cryptoCode}/payments | Get payments |
| [**internalLightningNodeApiOpenChannel()**](LightningInternalNodeApi.md#internalLightningNodeApiOpenChannel) | **POST** /api/v1/server/lightning/{cryptoCode}/channels | Open channel |
| [**internalLightningNodeApiPayInvoice()**](LightningInternalNodeApi.md#internalLightningNodeApiPayInvoice) | **POST** /api/v1/server/lightning/{cryptoCode}/invoices/pay | Pay Lightning Invoice |


## `internalLightningNodeApiConnectToNode()`

```php
internalLightningNodeApiConnectToNode($crypto_code, $connect_to_node_request)
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


$apiInstance = new OpenAPI\Client\Api\LightningInternalNodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$connect_to_node_request = new \OpenAPI\Client\Model\ConnectToNodeRequest(); // \OpenAPI\Client\Model\ConnectToNodeRequest

try {
    $apiInstance->internalLightningNodeApiConnectToNode($crypto_code, $connect_to_node_request);
} catch (Exception $e) {
    echo 'Exception when calling LightningInternalNodeApi->internalLightningNodeApiConnectToNode: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
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

## `internalLightningNodeApiCreateInvoice()`

```php
internalLightningNodeApiCreateInvoice($crypto_code, $create_lightning_invoice_request): \OpenAPI\Client\Model\LightningInvoiceData
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


$apiInstance = new OpenAPI\Client\Api\LightningInternalNodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$create_lightning_invoice_request = new \OpenAPI\Client\Model\CreateLightningInvoiceRequest(); // \OpenAPI\Client\Model\CreateLightningInvoiceRequest

try {
    $result = $apiInstance->internalLightningNodeApiCreateInvoice($crypto_code, $create_lightning_invoice_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningInternalNodeApi->internalLightningNodeApiCreateInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
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

## `internalLightningNodeApiGetBalance()`

```php
internalLightningNodeApiGetBalance($crypto_code): \OpenAPI\Client\Model\LightningNodeBalanceData
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


$apiInstance = new OpenAPI\Client\Api\LightningInternalNodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query

try {
    $result = $apiInstance->internalLightningNodeApiGetBalance($crypto_code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningInternalNodeApi->internalLightningNodeApiGetBalance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |

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

## `internalLightningNodeApiGetChannels()`

```php
internalLightningNodeApiGetChannels($crypto_code): \OpenAPI\Client\Model\LightningChannelData[]
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


$apiInstance = new OpenAPI\Client\Api\LightningInternalNodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query

try {
    $result = $apiInstance->internalLightningNodeApiGetChannels($crypto_code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningInternalNodeApi->internalLightningNodeApiGetChannels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |

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

## `internalLightningNodeApiGetDepositAddress()`

```php
internalLightningNodeApiGetDepositAddress($crypto_code): string
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


$apiInstance = new OpenAPI\Client\Api\LightningInternalNodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query

try {
    $result = $apiInstance->internalLightningNodeApiGetDepositAddress($crypto_code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningInternalNodeApi->internalLightningNodeApiGetDepositAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
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

## `internalLightningNodeApiGetHistogram()`

```php
internalLightningNodeApiGetHistogram($crypto_code): \OpenAPI\Client\Model\HistogramData
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


$apiInstance = new OpenAPI\Client\Api\LightningInternalNodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query

try {
    $result = $apiInstance->internalLightningNodeApiGetHistogram($crypto_code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningInternalNodeApi->internalLightningNodeApiGetHistogram: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |

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

## `internalLightningNodeApiGetInfo()`

```php
internalLightningNodeApiGetInfo($crypto_code): \OpenAPI\Client\Model\LightningNodeInformationData
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


$apiInstance = new OpenAPI\Client\Api\LightningInternalNodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query

try {
    $result = $apiInstance->internalLightningNodeApiGetInfo($crypto_code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningInternalNodeApi->internalLightningNodeApiGetInfo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |

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

## `internalLightningNodeApiGetInvoice()`

```php
internalLightningNodeApiGetInvoice($crypto_code, $id): \OpenAPI\Client\Model\LightningInvoiceData
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


$apiInstance = new OpenAPI\Client\Api\LightningInternalNodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$id = 'id_example'; // string | The id of the lightning invoice.

try {
    $result = $apiInstance->internalLightningNodeApiGetInvoice($crypto_code, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningInternalNodeApi->internalLightningNodeApiGetInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
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

## `internalLightningNodeApiGetInvoices()`

```php
internalLightningNodeApiGetInvoices($crypto_code, $pending_only, $offset_index): \OpenAPI\Client\Model\LightningInvoiceData[]
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


$apiInstance = new OpenAPI\Client\Api\LightningInternalNodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$pending_only = false; // bool | Limit to pending invoices only
$offset_index = 0; // float | The index of an invoice that will be used as the start of the list

try {
    $result = $apiInstance->internalLightningNodeApiGetInvoices($crypto_code, $pending_only, $offset_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningInternalNodeApi->internalLightningNodeApiGetInvoices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
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

## `internalLightningNodeApiGetPayment()`

```php
internalLightningNodeApiGetPayment($crypto_code, $payment_hash): \OpenAPI\Client\Model\LightningPaymentData
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


$apiInstance = new OpenAPI\Client\Api\LightningInternalNodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$payment_hash = 'payment_hash_example'; // string | The payment hash of the lightning payment.

try {
    $result = $apiInstance->internalLightningNodeApiGetPayment($crypto_code, $payment_hash);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningInternalNodeApi->internalLightningNodeApiGetPayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
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

## `internalLightningNodeApiGetPayments()`

```php
internalLightningNodeApiGetPayments($crypto_code, $include_pending, $offset_index): \OpenAPI\Client\Model\LightningPaymentData[]
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


$apiInstance = new OpenAPI\Client\Api\LightningInternalNodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$include_pending = false; // bool | Also include pending payments
$offset_index = 0; // float | The index of a payment that will be used as the start of the list

try {
    $result = $apiInstance->internalLightningNodeApiGetPayments($crypto_code, $include_pending, $offset_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningInternalNodeApi->internalLightningNodeApiGetPayments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
| **include_pending** | **bool**| Also include pending payments | [optional] [default to false] |
| **offset_index** | **float**| The index of a payment that will be used as the start of the list | [optional] [default to 0] |

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

## `internalLightningNodeApiOpenChannel()`

```php
internalLightningNodeApiOpenChannel($crypto_code, $open_lightning_channel_request)
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


$apiInstance = new OpenAPI\Client\Api\LightningInternalNodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$open_lightning_channel_request = new \OpenAPI\Client\Model\OpenLightningChannelRequest(); // \OpenAPI\Client\Model\OpenLightningChannelRequest

try {
    $apiInstance->internalLightningNodeApiOpenChannel($crypto_code, $open_lightning_channel_request);
} catch (Exception $e) {
    echo 'Exception when calling LightningInternalNodeApi->internalLightningNodeApiOpenChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
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

## `internalLightningNodeApiPayInvoice()`

```php
internalLightningNodeApiPayInvoice($crypto_code, $pay_lightning_invoice_request): \OpenAPI\Client\Model\LightningPaymentData
```

Pay Lightning Invoice

Pay a lightning invoice. In case the payment response times out, the status will be reported as pending and the final status can be resolved using the [Get payment](#operation/InternalLightningNodeApi_GetPayment) endpoint. The default wait time for payment responses is 30 seconds — it might take longer if multiple routes are tried or a hold invoice is getting paid.

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


$apiInstance = new OpenAPI\Client\Api\LightningInternalNodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$crypto_code = BTC; // string | The cryptoCode of the lightning-node to query
$pay_lightning_invoice_request = new \OpenAPI\Client\Model\PayLightningInvoiceRequest(); // \OpenAPI\Client\Model\PayLightningInvoiceRequest

try {
    $result = $apiInstance->internalLightningNodeApiPayInvoice($crypto_code, $pay_lightning_invoice_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LightningInternalNodeApi->internalLightningNodeApiPayInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **crypto_code** | **string**| The cryptoCode of the lightning-node to query | |
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
