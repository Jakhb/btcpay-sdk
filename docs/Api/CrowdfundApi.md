# OpenAPI\Client\CrowdfundApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**appsCreateCrowdfundApp()**](CrowdfundApi.md#appsCreateCrowdfundApp) | **POST** /api/v1/stores/{storeId}/apps/crowdfund | Create a new Crowdfund app |
| [**appsGetCrowdfundApp()**](CrowdfundApi.md#appsGetCrowdfundApp) | **GET** /api/v1/apps/crowdfund/{appId} | Get crowdfund app data |


## `appsCreateCrowdfundApp()`

```php
appsCreateCrowdfundApp($store_id, $crowdfund_app_request): \OpenAPI\Client\Model\CrowdfundAppData
```

Create a new Crowdfund app

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


$apiInstance = new OpenAPI\Client\Api\CrowdfundApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$crowdfund_app_request = new \OpenAPI\Client\Model\CrowdfundAppRequest(); // \OpenAPI\Client\Model\CrowdfundAppRequest

try {
    $result = $apiInstance->appsCreateCrowdfundApp($store_id, $crowdfund_app_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CrowdfundApi->appsCreateCrowdfundApp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **crowdfund_app_request** | [**\OpenAPI\Client\Model\CrowdfundAppRequest**](../Model/CrowdfundAppRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\CrowdfundAppData**](../Model/CrowdfundAppData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appsGetCrowdfundApp()`

```php
appsGetCrowdfundApp($app_id): \OpenAPI\Client\Model\CrowdfundAppData
```

Get crowdfund app data

Returns crowdfund app data

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


$apiInstance = new OpenAPI\Client\Api\CrowdfundApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | App ID

try {
    $result = $apiInstance->appsGetCrowdfundApp($app_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CrowdfundApi->appsGetCrowdfundApp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| App ID | |

### Return type

[**\OpenAPI\Client\Model\CrowdfundAppData**](../Model/CrowdfundAppData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
