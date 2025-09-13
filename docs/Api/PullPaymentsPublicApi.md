# OpenAPI\Client\PullPaymentsPublicApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**pullPaymentsCreatePayout()**](PullPaymentsPublicApi.md#pullPaymentsCreatePayout) | **POST** /api/v1/pull-payments/{pullPaymentId}/payouts | Create Payout |
| [**pullPaymentsGetPayout()**](PullPaymentsPublicApi.md#pullPaymentsGetPayout) | **GET** /api/v1/pull-payments/{pullPaymentId}/payouts/{payoutId} | Get Payout |
| [**pullPaymentsGetPayouts()**](PullPaymentsPublicApi.md#pullPaymentsGetPayouts) | **GET** /api/v1/pull-payments/{pullPaymentId}/payouts | Get Payouts |
| [**pullPaymentsGetPullPayment()**](PullPaymentsPublicApi.md#pullPaymentsGetPullPayment) | **GET** /api/v1/pull-payments/{pullPaymentId} | Get Pull Payment |
| [**pullPaymentsGetPullPaymentLNURL()**](PullPaymentsPublicApi.md#pullPaymentsGetPullPaymentLNURL) | **GET** /api/v1/pull-payments/{pullPaymentId}/lnurl | Get Pull Payment LNURL details |
| [**pullPaymentsLinkBoltcard()**](PullPaymentsPublicApi.md#pullPaymentsLinkBoltcard) | **POST** /api/v1/pull-payments/{pullPaymentId}/boltcards | Link a boltcard to a pull payment |


## `pullPaymentsCreatePayout()`

```php
pullPaymentsCreatePayout($pull_payment_id, $create_payout_request): \OpenAPI\Client\Model\PayoutData
```

Create Payout

Create a new payout

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PullPaymentsPublicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$pull_payment_id = 'pull_payment_id_example'; // string | The ID of the pull payment
$create_payout_request = new \OpenAPI\Client\Model\CreatePayoutRequest(); // \OpenAPI\Client\Model\CreatePayoutRequest

try {
    $result = $apiInstance->pullPaymentsCreatePayout($pull_payment_id, $create_payout_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PullPaymentsPublicApi->pullPaymentsCreatePayout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pull_payment_id** | **string**| The ID of the pull payment | |
| **create_payout_request** | [**\OpenAPI\Client\Model\CreatePayoutRequest**](../Model/CreatePayoutRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PayoutData**](../Model/PayoutData.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pullPaymentsGetPayout()`

```php
pullPaymentsGetPayout($pull_payment_id, $payout_id): \OpenAPI\Client\Model\PayoutData
```

Get Payout

Get payout

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PullPaymentsPublicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$pull_payment_id = 'pull_payment_id_example'; // string | The ID of the pull payment
$payout_id = 'payout_id_example'; // string | The ID of the pull payment payout

try {
    $result = $apiInstance->pullPaymentsGetPayout($pull_payment_id, $payout_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PullPaymentsPublicApi->pullPaymentsGetPayout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pull_payment_id** | **string**| The ID of the pull payment | |
| **payout_id** | **string**| The ID of the pull payment payout | |

### Return type

[**\OpenAPI\Client\Model\PayoutData**](../Model/PayoutData.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pullPaymentsGetPayouts()`

```php
pullPaymentsGetPayouts($pull_payment_id, $include_cancelled): \OpenAPI\Client\Model\PayoutData[]
```

Get Payouts

Get payouts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PullPaymentsPublicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$pull_payment_id = 'pull_payment_id_example'; // string | The ID of the pull payment
$include_cancelled = false; // bool | Whether this should list cancelled payouts

try {
    $result = $apiInstance->pullPaymentsGetPayouts($pull_payment_id, $include_cancelled);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PullPaymentsPublicApi->pullPaymentsGetPayouts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pull_payment_id** | **string**| The ID of the pull payment | |
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

## `pullPaymentsGetPullPayment()`

```php
pullPaymentsGetPullPayment($pull_payment_id): \OpenAPI\Client\Model\PullPaymentData
```

Get Pull Payment

Get a pull payment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PullPaymentsPublicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$pull_payment_id = 'pull_payment_id_example'; // string | The ID of the pull payment

try {
    $result = $apiInstance->pullPaymentsGetPullPayment($pull_payment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PullPaymentsPublicApi->pullPaymentsGetPullPayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pull_payment_id** | **string**| The ID of the pull payment | |

### Return type

[**\OpenAPI\Client\Model\PullPaymentData**](../Model/PullPaymentData.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pullPaymentsGetPullPaymentLNURL()`

```php
pullPaymentsGetPullPaymentLNURL($pull_payment_id): \OpenAPI\Client\Model\LNURLData
```

Get Pull Payment LNURL details

Get Pull Payment LNURL details

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PullPaymentsPublicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$pull_payment_id = 'pull_payment_id_example'; // string | The ID of the pull payment

try {
    $result = $apiInstance->pullPaymentsGetPullPaymentLNURL($pull_payment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PullPaymentsPublicApi->pullPaymentsGetPullPaymentLNURL: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pull_payment_id** | **string**| The ID of the pull payment | |

### Return type

[**\OpenAPI\Client\Model\LNURLData**](../Model/LNURLData.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pullPaymentsLinkBoltcard()`

```php
pullPaymentsLinkBoltcard($pull_payment_id, $pull_payments_link_boltcard_request): \OpenAPI\Client\Model\PullPaymentsLinkBoltcard200Response
```

Link a boltcard to a pull payment

Linking a boltcard to a pull payment will allow you to pay via NFC with it, the money will be sent from the pull payment. The boltcard keys are generated using [Deterministic Boltcard Key Generation](https://github.com/boltcard/boltcard/blob/main/docs/DETERMINISTIC.md).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PullPaymentsPublicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$pull_payment_id = 'pull_payment_id_example'; // string | The ID of the pull payment
$pull_payments_link_boltcard_request = new \OpenAPI\Client\Model\PullPaymentsLinkBoltcardRequest(); // \OpenAPI\Client\Model\PullPaymentsLinkBoltcardRequest

try {
    $result = $apiInstance->pullPaymentsLinkBoltcard($pull_payment_id, $pull_payments_link_boltcard_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PullPaymentsPublicApi->pullPaymentsLinkBoltcard: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pull_payment_id** | **string**| The ID of the pull payment | |
| **pull_payments_link_boltcard_request** | [**\OpenAPI\Client\Model\PullPaymentsLinkBoltcardRequest**](../Model/PullPaymentsLinkBoltcardRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PullPaymentsLinkBoltcard200Response**](../Model/PullPaymentsLinkBoltcard200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
