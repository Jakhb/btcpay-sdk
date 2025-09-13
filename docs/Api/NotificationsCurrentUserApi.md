# OpenAPI\Client\NotificationsCurrentUserApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**notificationsDeleteNotification()**](NotificationsCurrentUserApi.md#notificationsDeleteNotification) | **DELETE** /api/v1/users/me/notifications/{id} | Remove Notification |
| [**notificationsGetNotification()**](NotificationsCurrentUserApi.md#notificationsGetNotification) | **GET** /api/v1/users/me/notifications/{id} | Get notification |
| [**notificationsGetNotificationSettings()**](NotificationsCurrentUserApi.md#notificationsGetNotificationSettings) | **GET** /api/v1/users/me/notification-settings | Get notification settings |
| [**notificationsGetNotifications()**](NotificationsCurrentUserApi.md#notificationsGetNotifications) | **GET** /api/v1/users/me/notifications | Get notifications |
| [**notificationsUpdateNotification()**](NotificationsCurrentUserApi.md#notificationsUpdateNotification) | **PUT** /api/v1/users/me/notifications/{id} | Update notification |
| [**notificationsUpdateNotificationSettings()**](NotificationsCurrentUserApi.md#notificationsUpdateNotificationSettings) | **PUT** /api/v1/users/me/notification-settings | Update notification settings |


## `notificationsDeleteNotification()`

```php
notificationsDeleteNotification($id)
```

Remove Notification

Removes the specified notification.

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


$apiInstance = new OpenAPI\Client\Api\NotificationsCurrentUserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The notification to remove

try {
    $apiInstance->notificationsDeleteNotification($id);
} catch (Exception $e) {
    echo 'Exception when calling NotificationsCurrentUserApi->notificationsDeleteNotification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The notification to remove | |

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

## `notificationsGetNotification()`

```php
notificationsGetNotification($id): \OpenAPI\Client\Model\NotificationData
```

Get notification

View information about the specified notification

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


$apiInstance = new OpenAPI\Client\Api\NotificationsCurrentUserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The notification to fetch

try {
    $result = $apiInstance->notificationsGetNotification($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationsCurrentUserApi->notificationsGetNotification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The notification to fetch | |

### Return type

[**\OpenAPI\Client\Model\NotificationData**](../Model/NotificationData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationsGetNotificationSettings()`

```php
notificationsGetNotificationSettings(): \OpenAPI\Client\Model\NotificationSettingsData
```

Get notification settings

View information about your notification settings

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


$apiInstance = new OpenAPI\Client\Api\NotificationsCurrentUserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->notificationsGetNotificationSettings();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationsCurrentUserApi->notificationsGetNotificationSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\NotificationSettingsData**](../Model/NotificationSettingsData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationsGetNotifications()`

```php
notificationsGetNotifications($store_id, $take, $skip, $seen): \OpenAPI\Client\Model\NotificationData
```

Get notifications

View current user's notifications

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


$apiInstance = new OpenAPI\Client\Api\NotificationsCurrentUserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = &storeId=ABCDE&storeId=FGHIJ; // string[] | Array of store ids to fetch the notifications for
$take = 3.4; // float | Number of records returned in response
$skip = 3.4; // float | Number of records to skip
$seen = 'seen_example'; // string | filter by seen notifications

try {
    $result = $apiInstance->notificationsGetNotifications($store_id, $take, $skip, $seen);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationsCurrentUserApi->notificationsGetNotifications: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | [**string[]**](../Model/string.md)| Array of store ids to fetch the notifications for | [optional] |
| **take** | **float**| Number of records returned in response | [optional] |
| **skip** | **float**| Number of records to skip | [optional] |
| **seen** | **string**| filter by seen notifications | [optional] |

### Return type

[**\OpenAPI\Client\Model\NotificationData**](../Model/NotificationData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationsUpdateNotification()`

```php
notificationsUpdateNotification($id, $update_notification): \OpenAPI\Client\Model\NotificationData
```

Update notification

Updates the notification

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


$apiInstance = new OpenAPI\Client\Api\NotificationsCurrentUserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The notification to update
$update_notification = new \OpenAPI\Client\Model\UpdateNotification(); // \OpenAPI\Client\Model\UpdateNotification

try {
    $result = $apiInstance->notificationsUpdateNotification($id, $update_notification);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationsCurrentUserApi->notificationsUpdateNotification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The notification to update | |
| **update_notification** | [**\OpenAPI\Client\Model\UpdateNotification**](../Model/UpdateNotification.md)|  | |

### Return type

[**\OpenAPI\Client\Model\NotificationData**](../Model/NotificationData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationsUpdateNotificationSettings()`

```php
notificationsUpdateNotificationSettings($update_notification_settings_request): \OpenAPI\Client\Model\NotificationSettingsData
```

Update notification settings

Updates the current user's notification settings

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


$apiInstance = new OpenAPI\Client\Api\NotificationsCurrentUserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$update_notification_settings_request = new \OpenAPI\Client\Model\UpdateNotificationSettingsRequest(); // \OpenAPI\Client\Model\UpdateNotificationSettingsRequest

try {
    $result = $apiInstance->notificationsUpdateNotificationSettings($update_notification_settings_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationsCurrentUserApi->notificationsUpdateNotificationSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **update_notification_settings_request** | [**\OpenAPI\Client\Model\UpdateNotificationSettingsRequest**](../Model/UpdateNotificationSettingsRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\NotificationSettingsData**](../Model/NotificationSettingsData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
