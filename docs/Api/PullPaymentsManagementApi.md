# OpenAPI\Client\PullPaymentsManagementApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**pullPaymentsArchivePullPayment()**](PullPaymentsManagementApi.md#pullPaymentsArchivePullPayment) | **DELETE** /api/v1/stores/{storeId}/pull-payments/{pullPaymentId} | Archive a pull payment |
| [**pullPaymentsCreatePullPayment()**](PullPaymentsManagementApi.md#pullPaymentsCreatePullPayment) | **POST** /api/v1/stores/{storeId}/pull-payments | Create a new pull payment |
| [**pullPaymentsGetPullPayments()**](PullPaymentsManagementApi.md#pullPaymentsGetPullPayments) | **GET** /api/v1/stores/{storeId}/pull-payments | Get store&#39;s pull payments |


## `pullPaymentsArchivePullPayment()`

```php
pullPaymentsArchivePullPayment($store_id, $pull_payment_id)
```

Archive a pull payment

Archive this pull payment (Will cancel all payouts awaiting for payment)

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


$apiInstance = new OpenAPI\Client\Api\PullPaymentsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$pull_payment_id = 'pull_payment_id_example'; // string | The ID of the pull payment

try {
    $apiInstance->pullPaymentsArchivePullPayment($store_id, $pull_payment_id);
} catch (Exception $e) {
    echo 'Exception when calling PullPaymentsManagementApi->pullPaymentsArchivePullPayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **pull_payment_id** | **string**| The ID of the pull payment | |

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

## `pullPaymentsCreatePullPayment()`

```php
pullPaymentsCreatePullPayment($store_id, $pull_payments_create_pull_payment_request): \OpenAPI\Client\Model\PullPaymentData
```

Create a new pull payment

A pull payment allows its receiver to ask for payouts up to `amount` of `currency` every `period`.

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


$apiInstance = new OpenAPI\Client\Api\PullPaymentsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$pull_payments_create_pull_payment_request = new \OpenAPI\Client\Model\PullPaymentsCreatePullPaymentRequest(); // \OpenAPI\Client\Model\PullPaymentsCreatePullPaymentRequest

try {
    $result = $apiInstance->pullPaymentsCreatePullPayment($store_id, $pull_payments_create_pull_payment_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PullPaymentsManagementApi->pullPaymentsCreatePullPayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **pull_payments_create_pull_payment_request** | [**\OpenAPI\Client\Model\PullPaymentsCreatePullPaymentRequest**](../Model/PullPaymentsCreatePullPaymentRequest.md)|  | [optional] |

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

## `pullPaymentsGetPullPayments()`

```php
pullPaymentsGetPullPayments($store_id, $include_archived): \OpenAPI\Client\Model\PullPaymentData[]
```

Get store's pull payments

Get the pull payments of a store

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


$apiInstance = new OpenAPI\Client\Api\PullPaymentsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$include_archived = false; // bool | Whether this should list archived pull payments

try {
    $result = $apiInstance->pullPaymentsGetPullPayments($store_id, $include_archived);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PullPaymentsManagementApi->pullPaymentsGetPullPayments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **include_archived** | **bool**| Whether this should list archived pull payments | [optional] [default to false] |

### Return type

[**\OpenAPI\Client\Model\PullPaymentData[]**](../Model/PullPaymentData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
