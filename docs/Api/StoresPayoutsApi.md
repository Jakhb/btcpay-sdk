# OpenAPI\Client\StoresPayoutsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getStorePayout()**](StoresPayoutsApi.md#getStorePayout) | **GET** /api/v1/stores/{storeId}/payouts/{payoutId} | Get Payout |
| [**payoutsCreatePayoutThroughStore()**](StoresPayoutsApi.md#payoutsCreatePayoutThroughStore) | **POST** /api/v1/stores/{storeId}/payouts | Create Payout |
| [**pullPaymentsApprovePayout()**](StoresPayoutsApi.md#pullPaymentsApprovePayout) | **POST** /api/v1/stores/{storeId}/payouts/{payoutId} | Approve Payout |
| [**pullPaymentsCancelPayout()**](StoresPayoutsApi.md#pullPaymentsCancelPayout) | **DELETE** /api/v1/stores/{storeId}/payouts/{payoutId} | Cancel Payout |
| [**pullPaymentsGetStorePayouts()**](StoresPayoutsApi.md#pullPaymentsGetStorePayouts) | **GET** /api/v1/stores/{storeId}/payouts | Get Store Payouts |
| [**pullPaymentsMarkPayout()**](StoresPayoutsApi.md#pullPaymentsMarkPayout) | **POST** /api/v1/stores/{storeId}/payouts/{payoutId}/mark | Mark Payout |
| [**pullPaymentsMarkPayoutPaid()**](StoresPayoutsApi.md#pullPaymentsMarkPayoutPaid) | **POST** /api/v1/stores/{storeId}/payouts/{payoutId}/mark-paid | Mark Payout as Paid |


## `getStorePayout()`

```php
getStorePayout($store_id, $payout_id): \OpenAPI\Client\Model\PayoutData
```

Get Payout

Get payout

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$payout_id = 'payout_id_example'; // string | The ID of the payout

try {
    $result = $apiInstance->getStorePayout($store_id, $payout_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutsApi->getStorePayout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **payout_id** | **string**| The ID of the payout | |

### Return type

[**\OpenAPI\Client\Model\PayoutData**](../Model/PayoutData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `payoutsCreatePayoutThroughStore()`

```php
payoutsCreatePayoutThroughStore($store_id, $create_payout_through_store_request): \OpenAPI\Client\Model\PayoutData
```

Create Payout

Create a new payout

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$create_payout_through_store_request = new \OpenAPI\Client\Model\CreatePayoutThroughStoreRequest(); // \OpenAPI\Client\Model\CreatePayoutThroughStoreRequest

try {
    $result = $apiInstance->payoutsCreatePayoutThroughStore($store_id, $create_payout_through_store_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutsApi->payoutsCreatePayoutThroughStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **create_payout_through_store_request** | [**\OpenAPI\Client\Model\CreatePayoutThroughStoreRequest**](../Model/CreatePayoutThroughStoreRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PayoutData**](../Model/PayoutData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pullPaymentsApprovePayout()`

```php
pullPaymentsApprovePayout($store_id, $payout_id, $pull_payments_approve_payout_request): \OpenAPI\Client\Model\PayoutData
```

Approve Payout

Approve a payout

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$payout_id = 'payout_id_example'; // string | The ID of the payout
$pull_payments_approve_payout_request = new \OpenAPI\Client\Model\PullPaymentsApprovePayoutRequest(); // \OpenAPI\Client\Model\PullPaymentsApprovePayoutRequest

try {
    $result = $apiInstance->pullPaymentsApprovePayout($store_id, $payout_id, $pull_payments_approve_payout_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutsApi->pullPaymentsApprovePayout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **payout_id** | **string**| The ID of the payout | |
| **pull_payments_approve_payout_request** | [**\OpenAPI\Client\Model\PullPaymentsApprovePayoutRequest**](../Model/PullPaymentsApprovePayoutRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PayoutData**](../Model/PayoutData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pullPaymentsCancelPayout()`

```php
pullPaymentsCancelPayout($store_id, $payout_id)
```

Cancel Payout

Cancel the payout

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$payout_id = 'payout_id_example'; // string | The ID of the payout

try {
    $apiInstance->pullPaymentsCancelPayout($store_id, $payout_id);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutsApi->pullPaymentsCancelPayout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **payout_id** | **string**| The ID of the payout | |

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

## `pullPaymentsGetStorePayouts()`

```php
pullPaymentsGetStorePayouts($store_id, $include_cancelled): \OpenAPI\Client\Model\PayoutData[]
```

Get Store Payouts

Get payouts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StoresPayoutsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$store_id = 'store_id_example'; // string | The store ID
$include_cancelled = false; // bool | Whether this should list cancelled payouts

try {
    $result = $apiInstance->pullPaymentsGetStorePayouts($store_id, $include_cancelled);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutsApi->pullPaymentsGetStorePayouts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **include_cancelled** | **bool**| Whether this should list cancelled payouts | [optional] [default to false] |

### Return type

[**\OpenAPI\Client\Model\PayoutData[]**](../Model/PayoutData.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pullPaymentsMarkPayout()`

```php
pullPaymentsMarkPayout($store_id, $payout_id, $pull_payments_mark_payout_request)
```

Mark Payout

Mark a payout with a state

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$payout_id = 'payout_id_example'; // string | The ID of the payout
$pull_payments_mark_payout_request = new \OpenAPI\Client\Model\PullPaymentsMarkPayoutRequest(); // \OpenAPI\Client\Model\PullPaymentsMarkPayoutRequest

try {
    $apiInstance->pullPaymentsMarkPayout($store_id, $payout_id, $pull_payments_mark_payout_request);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutsApi->pullPaymentsMarkPayout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **payout_id** | **string**| The ID of the payout | |
| **pull_payments_mark_payout_request** | [**\OpenAPI\Client\Model\PullPaymentsMarkPayoutRequest**](../Model/PullPaymentsMarkPayoutRequest.md)|  | [optional] |

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

## `pullPaymentsMarkPayoutPaid()`

```php
pullPaymentsMarkPayoutPaid($store_id, $payout_id)
```

Mark Payout as Paid

Mark a payout as paid

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


$apiInstance = new OpenAPI\Client\Api\StoresPayoutsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$payout_id = 'payout_id_example'; // string | The ID of the payout

try {
    $apiInstance->pullPaymentsMarkPayoutPaid($store_id, $payout_id);
} catch (Exception $e) {
    echo 'Exception when calling StoresPayoutsApi->pullPaymentsMarkPayoutPaid: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **payout_id** | **string**| The ID of the payout | |

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
