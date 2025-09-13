# OpenAPI\Client\PointOfSaleApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**appsGetPointOfSaleApp()**](PointOfSaleApi.md#appsGetPointOfSaleApp) | **GET** /api/v1/apps/pos/{appId} | Get Point of Sale app data |


## `appsGetPointOfSaleApp()`

```php
appsGetPointOfSaleApp($app_id): \OpenAPI\Client\Model\PointOfSaleAppData
```

Get Point of Sale app data

Returns POS app data

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


$apiInstance = new OpenAPI\Client\Api\PointOfSaleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | App ID

try {
    $result = $apiInstance->appsGetPointOfSaleApp($app_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PointOfSaleApi->appsGetPointOfSaleApp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| App ID | |

### Return type

[**\OpenAPI\Client\Model\PointOfSaleAppData**](../Model/PointOfSaleAppData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
