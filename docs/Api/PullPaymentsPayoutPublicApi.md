# OpenAPI\Client\PullPaymentsPayoutPublicApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**pullPaymentsGetPayout()**](PullPaymentsPayoutPublicApi.md#pullPaymentsGetPayout) | **GET** /api/v1/pull-payments/{pullPaymentId}/payouts/{payoutId} | Get Payout |


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



$apiInstance = new OpenAPI\Client\Api\PullPaymentsPayoutPublicApi(
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
    echo 'Exception when calling PullPaymentsPayoutPublicApi->pullPaymentsGetPayout: ', $e->getMessage(), PHP_EOL;
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
