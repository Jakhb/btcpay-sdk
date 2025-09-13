# OpenAPI\Client\WebhooksApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**webhooksCreateWebhook()**](WebhooksApi.md#webhooksCreateWebhook) | **POST** /api/v1/stores/{storeId}/webhooks | Create a new webhook |
| [**webhooksDeleteWebhook()**](WebhooksApi.md#webhooksDeleteWebhook) | **DELETE** /api/v1/stores/{storeId}/webhooks/{webhookId} | Delete a webhook |
| [**webhooksGetWebhook()**](WebhooksApi.md#webhooksGetWebhook) | **GET** /api/v1/stores/{storeId}/webhooks/{webhookId} | Get a webhook of a store |
| [**webhooksGetWebhookDeliveries()**](WebhooksApi.md#webhooksGetWebhookDeliveries) | **GET** /api/v1/stores/{storeId}/webhooks/{webhookId}/deliveries | Get latest deliveries |
| [**webhooksGetWebhookDelivery()**](WebhooksApi.md#webhooksGetWebhookDelivery) | **GET** /api/v1/stores/{storeId}/webhooks/{webhookId}/deliveries/{deliveryId} | Get a webhook delivery |
| [**webhooksGetWebhookDeliveryRequests()**](WebhooksApi.md#webhooksGetWebhookDeliveryRequests) | **GET** /api/v1/stores/{storeId}/webhooks/{webhookId}/deliveries/{deliveryId}/request | Get the delivery&#39;s request |
| [**webhooksGetWebhooks()**](WebhooksApi.md#webhooksGetWebhooks) | **GET** /api/v1/stores/{storeId}/webhooks | Get webhooks of a store |
| [**webhooksRedeliverWebhookDelivery()**](WebhooksApi.md#webhooksRedeliverWebhookDelivery) | **POST** /api/v1/stores/{storeId}/webhooks/{webhookId}/deliveries/{deliveryId}/redeliver | Redeliver the delivery |
| [**webhooksUpdateWebhook()**](WebhooksApi.md#webhooksUpdateWebhook) | **PUT** /api/v1/stores/{storeId}/webhooks/{webhookId} | Update a webhook |


## `webhooksCreateWebhook()`

```php
webhooksCreateWebhook($store_id, $webhook_data_create): \OpenAPI\Client\Model\WebhookDataCreateResult
```

Create a new webhook

Create a new webhook

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


$apiInstance = new OpenAPI\Client\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$webhook_data_create = new \OpenAPI\Client\Model\WebhookDataCreate(); // \OpenAPI\Client\Model\WebhookDataCreate

try {
    $result = $apiInstance->webhooksCreateWebhook($store_id, $webhook_data_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->webhooksCreateWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **webhook_data_create** | [**\OpenAPI\Client\Model\WebhookDataCreate**](../Model/WebhookDataCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\WebhookDataCreateResult**](../Model/WebhookDataCreateResult.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhooksDeleteWebhook()`

```php
webhooksDeleteWebhook($store_id, $webhook_id)
```

Delete a webhook

Delete a webhook

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


$apiInstance = new OpenAPI\Client\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$webhook_id = 'webhook_id_example'; // string | The webhook id

try {
    $apiInstance->webhooksDeleteWebhook($store_id, $webhook_id);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->webhooksDeleteWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **webhook_id** | **string**| The webhook id | |

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

## `webhooksGetWebhook()`

```php
webhooksGetWebhook($store_id, $webhook_id): \OpenAPI\Client\Model\WebhookData
```

Get a webhook of a store

View webhook of a store

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


$apiInstance = new OpenAPI\Client\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$webhook_id = 'webhook_id_example'; // string | The webhook id

try {
    $result = $apiInstance->webhooksGetWebhook($store_id, $webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->webhooksGetWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **webhook_id** | **string**| The webhook id | |

### Return type

[**\OpenAPI\Client\Model\WebhookData**](../Model/WebhookData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhooksGetWebhookDeliveries()`

```php
webhooksGetWebhookDeliveries($store_id, $webhook_id, $count): \OpenAPI\Client\Model\WebhookDeliveryData[]
```

Get latest deliveries

List the latest deliveries to the webhook, ordered from the most recent

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


$apiInstance = new OpenAPI\Client\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$webhook_id = 'webhook_id_example'; // string | The webhook id
$count = 'count_example'; // string | The number of latest deliveries to fetch

try {
    $result = $apiInstance->webhooksGetWebhookDeliveries($store_id, $webhook_id, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->webhooksGetWebhookDeliveries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **webhook_id** | **string**| The webhook id | |
| **count** | **string**| The number of latest deliveries to fetch | [optional] |

### Return type

[**\OpenAPI\Client\Model\WebhookDeliveryData[]**](../Model/WebhookDeliveryData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhooksGetWebhookDelivery()`

```php
webhooksGetWebhookDelivery($delivery_id, $store_id, $webhook_id): \OpenAPI\Client\Model\WebhookDeliveryData
```

Get a webhook delivery

Information about a webhook delivery

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


$apiInstance = new OpenAPI\Client\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_id = 'delivery_id_example'; // string | The id of the delivery
$store_id = 'store_id_example'; // string | The store ID
$webhook_id = 'webhook_id_example'; // string | The webhook id

try {
    $result = $apiInstance->webhooksGetWebhookDelivery($delivery_id, $store_id, $webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->webhooksGetWebhookDelivery: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delivery_id** | **string**| The id of the delivery | |
| **store_id** | **string**| The store ID | |
| **webhook_id** | **string**| The webhook id | |

### Return type

[**\OpenAPI\Client\Model\WebhookDeliveryData**](../Model/WebhookDeliveryData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhooksGetWebhookDeliveryRequests()`

```php
webhooksGetWebhookDeliveryRequests($delivery_id, $store_id, $webhook_id): array<string,mixed>
```

Get the delivery's request

The delivery's JSON request sent to the endpoint

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


$apiInstance = new OpenAPI\Client\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_id = 'delivery_id_example'; // string | The id of the delivery
$store_id = 'store_id_example'; // string | The store ID
$webhook_id = 'webhook_id_example'; // string | The webhook id

try {
    $result = $apiInstance->webhooksGetWebhookDeliveryRequests($delivery_id, $store_id, $webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->webhooksGetWebhookDeliveryRequests: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delivery_id** | **string**| The id of the delivery | |
| **store_id** | **string**| The store ID | |
| **webhook_id** | **string**| The webhook id | |

### Return type

**array<string,mixed>**

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhooksGetWebhooks()`

```php
webhooksGetWebhooks($store_id): \OpenAPI\Client\Model\WebhookData[]
```

Get webhooks of a store

View webhooks of a store

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


$apiInstance = new OpenAPI\Client\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->webhooksGetWebhooks($store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->webhooksGetWebhooks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\WebhookData[]**](../Model/WebhookData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhooksRedeliverWebhookDelivery()`

```php
webhooksRedeliverWebhookDelivery($delivery_id, $store_id, $webhook_id): string
```

Redeliver the delivery

Redeliver the delivery

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


$apiInstance = new OpenAPI\Client\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_id = 'delivery_id_example'; // string | The id of the delivery
$store_id = 'store_id_example'; // string | The store ID
$webhook_id = 'webhook_id_example'; // string | The webhook id

try {
    $result = $apiInstance->webhooksRedeliverWebhookDelivery($delivery_id, $store_id, $webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->webhooksRedeliverWebhookDelivery: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delivery_id** | **string**| The id of the delivery | |
| **store_id** | **string**| The store ID | |
| **webhook_id** | **string**| The webhook id | |

### Return type

**string**

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhooksUpdateWebhook()`

```php
webhooksUpdateWebhook($store_id, $webhook_id, $webhook_data_update): \OpenAPI\Client\Model\WebhookData
```

Update a webhook

Update a webhook

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


$apiInstance = new OpenAPI\Client\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$webhook_id = 'webhook_id_example'; // string | The webhook id
$webhook_data_update = new \OpenAPI\Client\Model\WebhookDataUpdate(); // \OpenAPI\Client\Model\WebhookDataUpdate

try {
    $result = $apiInstance->webhooksUpdateWebhook($store_id, $webhook_id, $webhook_data_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->webhooksUpdateWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **webhook_id** | **string**| The webhook id | |
| **webhook_data_update** | [**\OpenAPI\Client\Model\WebhookDataUpdate**](../Model/WebhookDataUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\WebhookData**](../Model/WebhookData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
