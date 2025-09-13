# OpenAPI\Client\PaymentRequestsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**paymentRequestsArchivePaymentRequest()**](PaymentRequestsApi.md#paymentRequestsArchivePaymentRequest) | **DELETE** /api/v1/stores/{storeId}/payment-requests/{paymentRequestId} | Archive payment request |
| [**paymentRequestsCreatePaymentRequest()**](PaymentRequestsApi.md#paymentRequestsCreatePaymentRequest) | **POST** /api/v1/stores/{storeId}/payment-requests | Create a new payment request |
| [**paymentRequestsGetPaymentRequest()**](PaymentRequestsApi.md#paymentRequestsGetPaymentRequest) | **GET** /api/v1/stores/{storeId}/payment-requests/{paymentRequestId} | Get payment request |
| [**paymentRequestsGetPaymentRequests()**](PaymentRequestsApi.md#paymentRequestsGetPaymentRequests) | **GET** /api/v1/stores/{storeId}/payment-requests | Get payment requests |
| [**paymentRequestsPay()**](PaymentRequestsApi.md#paymentRequestsPay) | **POST** /api/v1/stores/{storeId}/payment-requests/{paymentRequestId}/pay | Create a new invoice for the payment request |
| [**paymentRequestsUpdatePaymentRequest()**](PaymentRequestsApi.md#paymentRequestsUpdatePaymentRequest) | **PUT** /api/v1/stores/{storeId}/payment-requests/{paymentRequestId} | Update payment request |


## `paymentRequestsArchivePaymentRequest()`

```php
paymentRequestsArchivePaymentRequest($store_id, $payment_request_id)
```

Archive payment request

Archives the specified payment request.

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


$apiInstance = new OpenAPI\Client\Api\PaymentRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$payment_request_id = 'payment_request_id_example'; // string | The payment request to remove

try {
    $apiInstance->paymentRequestsArchivePaymentRequest($store_id, $payment_request_id);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestsApi->paymentRequestsArchivePaymentRequest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **payment_request_id** | **string**| The payment request to remove | |

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

## `paymentRequestsCreatePaymentRequest()`

```php
paymentRequestsCreatePaymentRequest($store_id, $payment_request_base_data): \OpenAPI\Client\Model\PaymentRequestData
```

Create a new payment request

Create a new payment request

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


$apiInstance = new OpenAPI\Client\Api\PaymentRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$payment_request_base_data = new \OpenAPI\Client\Model\PaymentRequestBaseData(); // \OpenAPI\Client\Model\PaymentRequestBaseData

try {
    $result = $apiInstance->paymentRequestsCreatePaymentRequest($store_id, $payment_request_base_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestsApi->paymentRequestsCreatePaymentRequest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **payment_request_base_data** | [**\OpenAPI\Client\Model\PaymentRequestBaseData**](../Model/PaymentRequestBaseData.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PaymentRequestData**](../Model/PaymentRequestData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentRequestsGetPaymentRequest()`

```php
paymentRequestsGetPaymentRequest($store_id, $payment_request_id): \OpenAPI\Client\Model\PaymentRequestData
```

Get payment request

View information about the specified payment request

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


$apiInstance = new OpenAPI\Client\Api\PaymentRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$payment_request_id = 'payment_request_id_example'; // string | The payment request to fetch

try {
    $result = $apiInstance->paymentRequestsGetPaymentRequest($store_id, $payment_request_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestsApi->paymentRequestsGetPaymentRequest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **payment_request_id** | **string**| The payment request to fetch | |

### Return type

[**\OpenAPI\Client\Model\PaymentRequestData**](../Model/PaymentRequestData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentRequestsGetPaymentRequests()`

```php
paymentRequestsGetPaymentRequests($store_id): \OpenAPI\Client\Model\PaymentRequestData[]
```

Get payment requests

View information about the existing payment requests

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


$apiInstance = new OpenAPI\Client\Api\PaymentRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->paymentRequestsGetPaymentRequests($store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestsApi->paymentRequestsGetPaymentRequests: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\PaymentRequestData[]**](../Model/PaymentRequestData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentRequestsPay()`

```php
paymentRequestsPay($store_id, $payment_request_id, $payment_requests_pay_request): \OpenAPI\Client\Model\InvoiceData
```

Create a new invoice for the payment request

Create a new invoice for the payment request, or reuse an existing one

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


$apiInstance = new OpenAPI\Client\Api\PaymentRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$payment_request_id = 'payment_request_id_example'; // string | The payment request to create
$payment_requests_pay_request = new \OpenAPI\Client\Model\PaymentRequestsPayRequest(); // \OpenAPI\Client\Model\PaymentRequestsPayRequest | Invoice creation request

try {
    $result = $apiInstance->paymentRequestsPay($store_id, $payment_request_id, $payment_requests_pay_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestsApi->paymentRequestsPay: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **payment_request_id** | **string**| The payment request to create | |
| **payment_requests_pay_request** | [**\OpenAPI\Client\Model\PaymentRequestsPayRequest**](../Model/PaymentRequestsPayRequest.md)| Invoice creation request | [optional] |

### Return type

[**\OpenAPI\Client\Model\InvoiceData**](../Model/InvoiceData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentRequestsUpdatePaymentRequest()`

```php
paymentRequestsUpdatePaymentRequest($store_id, $payment_request_id, $payment_request_base_data): \OpenAPI\Client\Model\PaymentRequestData
```

Update payment request

Update a payment request

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


$apiInstance = new OpenAPI\Client\Api\PaymentRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$payment_request_id = 'payment_request_id_example'; // string | The payment request to update
$payment_request_base_data = new \OpenAPI\Client\Model\PaymentRequestBaseData(); // \OpenAPI\Client\Model\PaymentRequestBaseData

try {
    $result = $apiInstance->paymentRequestsUpdatePaymentRequest($store_id, $payment_request_id, $payment_request_base_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestsApi->paymentRequestsUpdatePaymentRequest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **payment_request_id** | **string**| The payment request to update | |
| **payment_request_base_data** | [**\OpenAPI\Client\Model\PaymentRequestBaseData**](../Model/PaymentRequestBaseData.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PaymentRequestData**](../Model/PaymentRequestData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
