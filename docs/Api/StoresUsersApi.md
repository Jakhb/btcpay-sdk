# OpenAPI\Client\StoresUsersApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**storesAddStoreUser()**](StoresUsersApi.md#storesAddStoreUser) | **POST** /api/v1/stores/{storeId}/users | Add a store user |
| [**storesGetStoreUsers()**](StoresUsersApi.md#storesGetStoreUsers) | **GET** /api/v1/stores/{storeId}/users | Get store users |
| [**storesRemoveStoreUser()**](StoresUsersApi.md#storesRemoveStoreUser) | **DELETE** /api/v1/stores/{storeId}/users/{idOrEmail} | Remove Store User |
| [**storesUpdateStoreUser()**](StoresUsersApi.md#storesUpdateStoreUser) | **PUT** /api/v1/stores/{storeId}/users/{idOrEmail} | Updates a store user |


## `storesAddStoreUser()`

```php
storesAddStoreUser($store_id, $store_user_data)
```

Add a store user

Add a store user

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


$apiInstance = new OpenAPI\Client\Api\StoresUsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$store_user_data = new \OpenAPI\Client\Model\StoreUserData(); // \OpenAPI\Client\Model\StoreUserData

try {
    $apiInstance->storesAddStoreUser($store_id, $store_user_data);
} catch (Exception $e) {
    echo 'Exception when calling StoresUsersApi->storesAddStoreUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **store_user_data** | [**\OpenAPI\Client\Model\StoreUserData**](../Model/StoreUserData.md)|  | |

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

## `storesGetStoreUsers()`

```php
storesGetStoreUsers($store_id): \OpenAPI\Client\Model\StoreUserData[]
```

Get store users

View users of the specified store

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


$apiInstance = new OpenAPI\Client\Api\StoresUsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID

try {
    $result = $apiInstance->storesGetStoreUsers($store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresUsersApi->storesGetStoreUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |

### Return type

[**\OpenAPI\Client\Model\StoreUserData[]**](../Model/StoreUserData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storesRemoveStoreUser()`

```php
storesRemoveStoreUser($store_id, $id_or_email)
```

Remove Store User

Removes the specified store user. If there is no other owner, this endpoint will fail.

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


$apiInstance = new OpenAPI\Client\Api\StoresUsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$id_or_email = 'id_or_email_example'; // string | The user's id or email

try {
    $apiInstance->storesRemoveStoreUser($store_id, $id_or_email);
} catch (Exception $e) {
    echo 'Exception when calling StoresUsersApi->storesRemoveStoreUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **id_or_email** | **string**| The user&#39;s id or email | |

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

## `storesUpdateStoreUser()`

```php
storesUpdateStoreUser($store_id, $id_or_email, $store_user_data)
```

Updates a store user

Updates a store user

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


$apiInstance = new OpenAPI\Client\Api\StoresUsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | The store ID
$id_or_email = 'id_or_email_example'; // string | The user's id or email
$store_user_data = new \OpenAPI\Client\Model\StoreUserData(); // \OpenAPI\Client\Model\StoreUserData

try {
    $apiInstance->storesUpdateStoreUser($store_id, $id_or_email, $store_user_data);
} catch (Exception $e) {
    echo 'Exception when calling StoresUsersApi->storesUpdateStoreUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| The store ID | |
| **id_or_email** | **string**| The user&#39;s id or email | |
| **store_user_data** | [**\OpenAPI\Client\Model\StoreUserData**](../Model/StoreUserData.md)|  | |

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
