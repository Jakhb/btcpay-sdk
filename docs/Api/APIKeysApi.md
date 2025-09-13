# OpenAPI\Client\APIKeysApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiKeysCreateApiKey()**](APIKeysApi.md#apiKeysCreateApiKey) | **POST** /api/v1/api-keys | Create a new API Key |
| [**apiKeysCreateUserApiKey()**](APIKeysApi.md#apiKeysCreateUserApiKey) | **POST** /api/v1/users/{idOrEmail}/api-keys | Create a new API Key for a user |
| [**apiKeysDeleteApiKey()**](APIKeysApi.md#apiKeysDeleteApiKey) | **DELETE** /api/v1/api-keys/{apikey} | Revoke an API Key |
| [**apiKeysDeleteCurrentApiKey()**](APIKeysApi.md#apiKeysDeleteCurrentApiKey) | **DELETE** /api/v1/api-keys/current | Revoke the current API Key |
| [**apiKeysDeleteUserApiKey()**](APIKeysApi.md#apiKeysDeleteUserApiKey) | **DELETE** /api/v1/users/{idOrEmail}/api-keys/{apikey} | Revoke an API Key of target user |
| [**apiKeysGetCurrentApiKey()**](APIKeysApi.md#apiKeysGetCurrentApiKey) | **GET** /api/v1/api-keys/current | Get the current API Key information |


## `apiKeysCreateApiKey()`

```php
apiKeysCreateApiKey($api_keys_create_api_key_request): \OpenAPI\Client\Model\ApiKeyData
```

Create a new API Key

Create a new API Key

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


$apiInstance = new OpenAPI\Client\Api\APIKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_keys_create_api_key_request = new \OpenAPI\Client\Model\ApiKeysCreateApiKeyRequest(); // \OpenAPI\Client\Model\ApiKeysCreateApiKeyRequest

try {
    $result = $apiInstance->apiKeysCreateApiKey($api_keys_create_api_key_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling APIKeysApi->apiKeysCreateApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_keys_create_api_key_request** | [**\OpenAPI\Client\Model\ApiKeysCreateApiKeyRequest**](../Model/ApiKeysCreateApiKeyRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ApiKeyData**](../Model/ApiKeyData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiKeysCreateUserApiKey()`

```php
apiKeysCreateUserApiKey($id_or_email, $api_keys_create_api_key_request): \OpenAPI\Client\Model\ApiKeyData
```

Create a new API Key for a user

Create a new API Key for a user

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


$apiInstance = new OpenAPI\Client\Api\APIKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id_or_email = 'id_or_email_example'; // string | The user's id or email
$api_keys_create_api_key_request = new \OpenAPI\Client\Model\ApiKeysCreateApiKeyRequest(); // \OpenAPI\Client\Model\ApiKeysCreateApiKeyRequest

try {
    $result = $apiInstance->apiKeysCreateUserApiKey($id_or_email, $api_keys_create_api_key_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling APIKeysApi->apiKeysCreateUserApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id_or_email** | **string**| The user&#39;s id or email | |
| **api_keys_create_api_key_request** | [**\OpenAPI\Client\Model\ApiKeysCreateApiKeyRequest**](../Model/ApiKeysCreateApiKeyRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ApiKeyData**](../Model/ApiKeyData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiKeysDeleteApiKey()`

```php
apiKeysDeleteApiKey($apikey)
```

Revoke an API Key

Revoke the current API key so that it cannot be used anymore

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


$apiInstance = new OpenAPI\Client\Api\APIKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$apikey = 'apikey_example'; // string | The API Key to revoke

try {
    $apiInstance->apiKeysDeleteApiKey($apikey);
} catch (Exception $e) {
    echo 'Exception when calling APIKeysApi->apiKeysDeleteApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **apikey** | **string**| The API Key to revoke | |

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

## `apiKeysDeleteCurrentApiKey()`

```php
apiKeysDeleteCurrentApiKey(): \OpenAPI\Client\Model\ApiKeyData
```

Revoke the current API Key

Revoke the current API key so that it cannot be used anymore

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: API_Key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\APIKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiKeysDeleteCurrentApiKey();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling APIKeysApi->apiKeysDeleteCurrentApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\ApiKeyData**](../Model/ApiKeyData.md)

### Authorization

[API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiKeysDeleteUserApiKey()`

```php
apiKeysDeleteUserApiKey($id_or_email, $apikey)
```

Revoke an API Key of target user

Revoke the API key of a target user so that it cannot be used anymore

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


$apiInstance = new OpenAPI\Client\Api\APIKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id_or_email = 'id_or_email_example'; // string | The user's id or email
$apikey = 'apikey_example'; // string | The API Key to revoke

try {
    $apiInstance->apiKeysDeleteUserApiKey($id_or_email, $apikey);
} catch (Exception $e) {
    echo 'Exception when calling APIKeysApi->apiKeysDeleteUserApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id_or_email** | **string**| The user&#39;s id or email | |
| **apikey** | **string**| The API Key to revoke | |

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

## `apiKeysGetCurrentApiKey()`

```php
apiKeysGetCurrentApiKey(): \OpenAPI\Client\Model\ApiKeyData
```

Get the current API Key information

View information about the current API key

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


$apiInstance = new OpenAPI\Client\Api\APIKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiKeysGetCurrentApiKey();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling APIKeysApi->apiKeysGetCurrentApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\ApiKeyData**](../Model/ApiKeyData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
