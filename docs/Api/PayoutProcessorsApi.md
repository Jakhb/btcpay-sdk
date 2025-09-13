# OpenAPI\Client\PayoutProcessorsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**payoutProcessorsGetPayoutProcessors()**](PayoutProcessorsApi.md#payoutProcessorsGetPayoutProcessors) | **GET** /api/v1/payout-processors | Get payout processors |


## `payoutProcessorsGetPayoutProcessors()`

```php
payoutProcessorsGetPayoutProcessors(): \OpenAPI\Client\Model\PayoutProcessorData[]
```

Get payout processors

Get payout processors available in this instance

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


$apiInstance = new OpenAPI\Client\Api\PayoutProcessorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->payoutProcessorsGetPayoutProcessors();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PayoutProcessorsApi->payoutProcessorsGetPayoutProcessors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\PayoutProcessorData[]**](../Model/PayoutProcessorData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
