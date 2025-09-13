# OpenAPI\Client\InvoicesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**invoicesActivatePaymentMethod()**](InvoicesApi.md#invoicesActivatePaymentMethod) | **POST** /api/v1/stores/{storeId}/invoices/{invoiceId}/payment-methods/{paymentMethodId}/activate | Activate Payment Method |
| [**invoicesArchiveInvoice()**](InvoicesApi.md#invoicesArchiveInvoice) | **DELETE** /api/v1/stores/{storeId}/invoices/{invoiceId} | Archive invoice |
| [**invoicesCreateInvoice()**](InvoicesApi.md#invoicesCreateInvoice) | **POST** /api/v1/stores/{storeId}/invoices | Create a new invoice |
| [**invoicesGetInvoice()**](InvoicesApi.md#invoicesGetInvoice) | **GET** /api/v1/stores/{storeId}/invoices/{invoiceId} | Get invoice |
| [**invoicesGetInvoicePaymentMethods()**](InvoicesApi.md#invoicesGetInvoicePaymentMethods) | **GET** /api/v1/stores/{storeId}/invoices/{invoiceId}/payment-methods | Get invoice payment methods |
| [**invoicesGetInvoiceRefundTriggerData()**](InvoicesApi.md#invoicesGetInvoiceRefundTriggerData) | **GET** /api/v1/stores/{storeId}/invoices/{invoiceId}/refund/{paymentMethodId} | Get invoice refund trigger data |
| [**invoicesGetInvoices()**](InvoicesApi.md#invoicesGetInvoices) | **GET** /api/v1/stores/{storeId}/invoices | Get invoices |
| [**invoicesMarkInvoiceStatus()**](InvoicesApi.md#invoicesMarkInvoiceStatus) | **POST** /api/v1/stores/{storeId}/invoices/{invoiceId}/status | Mark invoice status |
| [**invoicesRefund()**](InvoicesApi.md#invoicesRefund) | **POST** /api/v1/stores/{storeId}/invoices/{invoiceId}/refund | Refund invoice |
| [**invoicesUnarchiveInvoice()**](InvoicesApi.md#invoicesUnarchiveInvoice) | **POST** /api/v1/stores/{storeId}/invoices/{invoiceId}/unarchive | Unarchive invoice |
| [**invoicesUpdateInvoice()**](InvoicesApi.md#invoicesUpdateInvoice) | **PUT** /api/v1/stores/{storeId}/invoices/{invoiceId} | Update invoice |


## `invoicesActivatePaymentMethod()`

```php
invoicesActivatePaymentMethod($invoice_id, $payment_method_id, $store_id)
```

Activate Payment Method

Activate an invoice payment method (if lazy payments mode is enabled)

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


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string | The invoice ID
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID

try {
    $apiInstance->invoicesActivatePaymentMethod($invoice_id, $payment_method_id, $store_id);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesActivatePaymentMethod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**| The invoice ID | |
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

## `invoicesArchiveInvoice()`

```php
invoicesArchiveInvoice($invoice_id, $store_id)
```

Archive invoice

Archives the specified invoice.

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


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string | The invoice ID
$store_id = 'store_id_example'; // string | The store ID

try {
    $apiInstance->invoicesArchiveInvoice($invoice_id, $store_id);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesArchiveInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**| The invoice ID | |
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

## `invoicesCreateInvoice()`

```php
invoicesCreateInvoice($store_id, $create_invoice_request): \OpenAPI\Client\Model\InvoiceData
```

Create a new invoice

Create a new invoice

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


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$create_invoice_request = new \OpenAPI\Client\Model\CreateInvoiceRequest(); // \OpenAPI\Client\Model\CreateInvoiceRequest

try {
    $result = $apiInstance->invoicesCreateInvoice($store_id, $create_invoice_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesCreateInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **create_invoice_request** | [**\OpenAPI\Client\Model\CreateInvoiceRequest**](../Model/CreateInvoiceRequest.md)|  | |

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

## `invoicesGetInvoice()`

```php
invoicesGetInvoice($invoice_id, $store_id): \OpenAPI\Client\Model\InvoiceData
```

Get invoice

View information about the specified invoice

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


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string | The invoice ID
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->invoicesGetInvoice($invoice_id, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesGetInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**| The invoice ID | |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\InvoiceData**](../Model/InvoiceData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `invoicesGetInvoicePaymentMethods()`

```php
invoicesGetInvoicePaymentMethods($invoice_id, $store_id, $include_sensitive, $only_accounted_payments): \OpenAPI\Client\Model\InvoicePaymentMethodDataModel[]
```

Get invoice payment methods

View information about the specified invoice's payment methods

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


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string | The invoice ID
$store_id = 'store_id_example'; // string | The store ID
$include_sensitive = false; // bool | If `true`, `additionalData` might include sensitive data (such as xpub). Requires the permission `btcpay.store.canmodifystoresettings`.
$only_accounted_payments = true; // bool | If default or true, only returns payments which are accounted (in Bitcoin, this mean not returning RBF'd or double spent payments)

try {
    $result = $apiInstance->invoicesGetInvoicePaymentMethods($invoice_id, $store_id, $include_sensitive, $only_accounted_payments);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesGetInvoicePaymentMethods: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**| The invoice ID | |
| **store_id** | **string**| The store ID | |
| **include_sensitive** | **bool**| If &#x60;true&#x60;, &#x60;additionalData&#x60; might include sensitive data (such as xpub). Requires the permission &#x60;btcpay.store.canmodifystoresettings&#x60;. | [optional] [default to false] |
| **only_accounted_payments** | **bool**| If default or true, only returns payments which are accounted (in Bitcoin, this mean not returning RBF&#39;d or double spent payments) | [optional] [default to true] |

### Return type

[**\OpenAPI\Client\Model\InvoicePaymentMethodDataModel[]**](../Model/InvoicePaymentMethodDataModel.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `invoicesGetInvoiceRefundTriggerData()`

```php
invoicesGetInvoiceRefundTriggerData($invoice_id, $payment_method_id, $store_id): \OpenAPI\Client\Model\InvoiceRefundTriggerData
```

Get invoice refund trigger data

View calculated refund amounts (payment then/now, invoice, overpaid) for the specified invoice/payment-method. This can be used preceding the POST /refund call.

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


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string | The invoice ID
$payment_method_id = BTC-CHAIN; // string | The payment method id of the payment method to update
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->invoicesGetInvoiceRefundTriggerData($invoice_id, $payment_method_id, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesGetInvoiceRefundTriggerData: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**| The invoice ID | |
| **payment_method_id** | **string**| The payment method id of the payment method to update | |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\InvoiceRefundTriggerData**](../Model/InvoiceRefundTriggerData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `invoicesGetInvoices()`

```php
invoicesGetInvoices($store_id, $order_id, $text_search, $status, $end_date, $take, $skip, $start_date): \OpenAPI\Client\Model\InvoiceData[]
```

Get invoices

View information about the existing invoices

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


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$order_id = 1000&orderId=1001&orderId=1002; // string[] | Array of OrderIds to fetch the invoices for
$text_search = 'text_search_example'; // string | A term that can help locating specific invoices.
$status = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\InvoiceStatus(); // \OpenAPI\Client\Model\InvoiceStatus | Array of statuses of invoices to be fetched
$end_date = 3.4; // float | End date of the period to retrieve invoices
$take = 3.4; // float | Number of records returned in response
$skip = 3.4; // float | Number of records to skip
$start_date = 3.4; // float | Start date of the period to retrieve invoices

try {
    $result = $apiInstance->invoicesGetInvoices($store_id, $order_id, $text_search, $status, $end_date, $take, $skip, $start_date);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesGetInvoices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **order_id** | [**string[]**](../Model/string.md)| Array of OrderIds to fetch the invoices for | [optional] |
| **text_search** | **string**| A term that can help locating specific invoices. | [optional] |
| **status** | [**\OpenAPI\Client\Model\InvoiceStatus**](../Model/.md)| Array of statuses of invoices to be fetched | [optional] |
| **end_date** | **float**| End date of the period to retrieve invoices | [optional] |
| **take** | **float**| Number of records returned in response | [optional] |
| **skip** | **float**| Number of records to skip | [optional] |
| **start_date** | **float**| Start date of the period to retrieve invoices | [optional] |

### Return type

[**\OpenAPI\Client\Model\InvoiceData[]**](../Model/InvoiceData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `invoicesMarkInvoiceStatus()`

```php
invoicesMarkInvoiceStatus($invoice_id, $store_id, $mark_invoice_status_request): \OpenAPI\Client\Model\InvoiceData
```

Mark invoice status

Mark an invoice as invalid or settled.

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


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string | The invoice ID
$store_id = 'store_id_example'; // string | The store ID
$mark_invoice_status_request = new \OpenAPI\Client\Model\MarkInvoiceStatusRequest(); // \OpenAPI\Client\Model\MarkInvoiceStatusRequest

try {
    $result = $apiInstance->invoicesMarkInvoiceStatus($invoice_id, $store_id, $mark_invoice_status_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesMarkInvoiceStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**| The invoice ID | |
| **store_id** | **string**| The store ID | |
| **mark_invoice_status_request** | [**\OpenAPI\Client\Model\MarkInvoiceStatusRequest**](../Model/MarkInvoiceStatusRequest.md)|  | |

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

## `invoicesRefund()`

```php
invoicesRefund($invoice_id, $store_id, $invoices_refund_request): \OpenAPI\Client\Model\PullPaymentData
```

Refund invoice

Refund invoice

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


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string | The invoice ID
$store_id = 'store_id_example'; // string | The store ID
$invoices_refund_request = new \OpenAPI\Client\Model\InvoicesRefundRequest(); // \OpenAPI\Client\Model\InvoicesRefundRequest

try {
    $result = $apiInstance->invoicesRefund($invoice_id, $store_id, $invoices_refund_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesRefund: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**| The invoice ID | |
| **store_id** | **string**| The store ID | |
| **invoices_refund_request** | [**\OpenAPI\Client\Model\InvoicesRefundRequest**](../Model/InvoicesRefundRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PullPaymentData**](../Model/PullPaymentData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `invoicesUnarchiveInvoice()`

```php
invoicesUnarchiveInvoice($invoice_id, $store_id): \OpenAPI\Client\Model\InvoiceData
```

Unarchive invoice

Unarchive an invoice

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


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string | The invoice ID
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->invoicesUnarchiveInvoice($invoice_id, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesUnarchiveInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**| The invoice ID | |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\InvoiceData**](../Model/InvoiceData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `invoicesUpdateInvoice()`

```php
invoicesUpdateInvoice($invoice_id, $store_id, $update_invoice_request): \OpenAPI\Client\Model\InvoiceData
```

Update invoice

Updates the specified invoice.

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


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string | The invoice ID
$store_id = 'store_id_example'; // string | The store ID
$update_invoice_request = new \OpenAPI\Client\Model\UpdateInvoiceRequest(); // \OpenAPI\Client\Model\UpdateInvoiceRequest

try {
    $result = $apiInstance->invoicesUpdateInvoice($invoice_id, $store_id, $update_invoice_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesUpdateInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**| The invoice ID | |
| **store_id** | **string**| The store ID | |
| **update_invoice_request** | [**\OpenAPI\Client\Model\UpdateInvoiceRequest**](../Model/UpdateInvoiceRequest.md)|  | |

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
