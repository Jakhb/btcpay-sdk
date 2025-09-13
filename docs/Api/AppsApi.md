# OpenAPI\Client\AppsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**appDeleteAppItemImage()**](AppsApi.md#appDeleteAppItemImage) | **DELETE** /api/v1/apps/{appId}/image/{fileId} | Deletes the app item image |
| [**appsCreateCrowdfundApp()**](AppsApi.md#appsCreateCrowdfundApp) | **POST** /api/v1/stores/{storeId}/apps/crowdfund | Create a new Crowdfund app |
| [**appsCreatePointOfSaleApp()**](AppsApi.md#appsCreatePointOfSaleApp) | **POST** /api/v1/stores/{storeId}/apps/pos | Create a new Point of Sale app |
| [**appsDeleteApp()**](AppsApi.md#appsDeleteApp) | **DELETE** /api/v1/apps/{appId} | Delete app |
| [**appsGetAllApps()**](AppsApi.md#appsGetAllApps) | **GET** /api/v1/apps | Get basic app data for all apps for all stores for a user |
| [**appsGetAllAppsForStore()**](AppsApi.md#appsGetAllAppsForStore) | **GET** /api/v1/stores/{storeId}/apps | Get basic app data for all apps for a store |
| [**appsGetApp()**](AppsApi.md#appsGetApp) | **GET** /api/v1/apps/{appId} | Get basic app data |
| [**appsGetAppSales()**](AppsApi.md#appsGetAppSales) | **GET** /api/v1/apps/{appId}/sales | Get app sales statistics |
| [**appsGetAppTopItems()**](AppsApi.md#appsGetAppTopItems) | **GET** /api/v1/apps/{appId}/top-items | Get app top items statistics |
| [**appsGetCrowdfundApp()**](AppsApi.md#appsGetCrowdfundApp) | **GET** /api/v1/apps/crowdfund/{appId} | Get crowdfund app data |
| [**appsGetPointOfSaleApp()**](AppsApi.md#appsGetPointOfSaleApp) | **GET** /api/v1/apps/pos/{appId} | Get Point of Sale app data |
| [**appsPutPointOfSaleApp()**](AppsApi.md#appsPutPointOfSaleApp) | **PUT** /api/v1/apps/pos/{appId} | Update a Point of Sale app |
| [**appsUploadAppItemImage()**](AppsApi.md#appsUploadAppItemImage) | **POST** /api/v1/apps/{appId}/image | Uploads an image for a app item |


## `appDeleteAppItemImage()`

```php
appDeleteAppItemImage($app_id, $file_id)
```

Deletes the app item image

Deletes the app item image

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


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | App ID
$file_id = 'file_id_example'; // string | The file ID

try {
    $apiInstance->appDeleteAppItemImage($app_id, $file_id);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->appDeleteAppItemImage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| App ID | |
| **file_id** | **string**| The file ID | |

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


$apiInstance = new OpenAPI\Client\Api\AppsApi(
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
    echo 'Exception when calling AppsApi->appsCreateCrowdfundApp: ', $e->getMessage(), PHP_EOL;
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

## `appsCreatePointOfSaleApp()`

```php
appsCreatePointOfSaleApp($store_id, $point_of_sale_app_request): \OpenAPI\Client\Model\PointOfSaleAppData
```

Create a new Point of Sale app

Point of Sale app allows accepting payments for items in a virtual store

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


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$point_of_sale_app_request = new \OpenAPI\Client\Model\PointOfSaleAppRequest(); // \OpenAPI\Client\Model\PointOfSaleAppRequest

try {
    $result = $apiInstance->appsCreatePointOfSaleApp($store_id, $point_of_sale_app_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->appsCreatePointOfSaleApp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **point_of_sale_app_request** | [**\OpenAPI\Client\Model\PointOfSaleAppRequest**](../Model/PointOfSaleAppRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PointOfSaleAppData**](../Model/PointOfSaleAppData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appsDeleteApp()`

```php
appsDeleteApp($app_id)
```

Delete app

Deletes apps with specified ID

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


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | App ID

try {
    $apiInstance->appsDeleteApp($app_id);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->appsDeleteApp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| App ID | |

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

## `appsGetAllApps()`

```php
appsGetAllApps(): \OpenAPI\Client\Model\AppBaseData[]
```

Get basic app data for all apps for all stores for a user

Returns basic app data for all apps for all stores

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


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->appsGetAllApps();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->appsGetAllApps: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\AppBaseData[]**](../Model/AppBaseData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appsGetAllAppsForStore()`

```php
appsGetAllAppsForStore($store_id): \OpenAPI\Client\Model\AppBaseData[]
```

Get basic app data for all apps for a store

Returns basic app data for all apps for a store

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


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->appsGetAllAppsForStore($store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->appsGetAllAppsForStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\AppBaseData[]**](../Model/AppBaseData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appsGetApp()`

```php
appsGetApp($app_id): \OpenAPI\Client\Model\AppBaseData
```

Get basic app data

Returns basic app data shared between all types of apps

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


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | App ID

try {
    $result = $apiInstance->appsGetApp($app_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->appsGetApp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| App ID | |

### Return type

[**\OpenAPI\Client\Model\AppBaseData**](../Model/AppBaseData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appsGetAppSales()`

```php
appsGetAppSales($app_id, $number_of_days): \OpenAPI\Client\Model\AppSalesStats
```

Get app sales statistics

Returns sales statistics for the app

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


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | App ID
$number_of_days = 7; // float | How many of the last days

try {
    $result = $apiInstance->appsGetAppSales($app_id, $number_of_days);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->appsGetAppSales: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| App ID | |
| **number_of_days** | **float**| How many of the last days | [optional] [default to 7] |

### Return type

[**\OpenAPI\Client\Model\AppSalesStats**](../Model/AppSalesStats.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appsGetAppTopItems()`

```php
appsGetAppTopItems($app_id, $count, $offset): \OpenAPI\Client\Model\AppItemStats[]
```

Get app top items statistics

Returns top items statistics for the app

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


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | App ID
$count = 5; // float | How many of the items
$offset = 0; // float | Offset for paging

try {
    $result = $apiInstance->appsGetAppTopItems($app_id, $count, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->appsGetAppTopItems: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| App ID | |
| **count** | **float**| How many of the items | [optional] [default to 5] |
| **offset** | **float**| Offset for paging | [optional] [default to 0] |

### Return type

[**\OpenAPI\Client\Model\AppItemStats[]**](../Model/AppItemStats.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
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


$apiInstance = new OpenAPI\Client\Api\AppsApi(
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
    echo 'Exception when calling AppsApi->appsGetCrowdfundApp: ', $e->getMessage(), PHP_EOL;
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


$apiInstance = new OpenAPI\Client\Api\AppsApi(
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
    echo 'Exception when calling AppsApi->appsGetPointOfSaleApp: ', $e->getMessage(), PHP_EOL;
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

## `appsPutPointOfSaleApp()`

```php
appsPutPointOfSaleApp($app_id, $point_of_sale_app_request): \OpenAPI\Client\Model\PointOfSaleAppData
```

Update a Point of Sale app

Use this endpoint for updating the properties of a POS app

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


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | App ID
$point_of_sale_app_request = new \OpenAPI\Client\Model\PointOfSaleAppRequest(); // \OpenAPI\Client\Model\PointOfSaleAppRequest

try {
    $result = $apiInstance->appsPutPointOfSaleApp($app_id, $point_of_sale_app_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->appsPutPointOfSaleApp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| App ID | |
| **point_of_sale_app_request** | [**\OpenAPI\Client\Model\PointOfSaleAppRequest**](../Model/PointOfSaleAppRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PointOfSaleAppData**](../Model/PointOfSaleAppData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appsUploadAppItemImage()`

```php
appsUploadAppItemImage($app_id, $file): \OpenAPI\Client\Model\FileData
```

Uploads an image for a app item

Uploads an image for a app item

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


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | App ID
$file = '/path/to/file.txt'; // \SplFileObject | The image

try {
    $result = $apiInstance->appsUploadAppItemImage($app_id, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->appsUploadAppItemImage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| App ID | |
| **file** | **\SplFileObject****\SplFileObject**| The image | [optional] |

### Return type

[**\OpenAPI\Client\Model\FileData**](../Model/FileData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
