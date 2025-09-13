# OpenAPI\Client\ServerEmailApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**serverEmailGetSettings()**](ServerEmailApi.md#serverEmailGetSettings) | **GET** /api/v1/server/email | Get server email settings |
| [**serverEmailUpdateSettings()**](ServerEmailApi.md#serverEmailUpdateSettings) | **PUT** /api/v1/server/email | Update server email settings |


## `serverEmailGetSettings()`

```php
serverEmailGetSettings(): \OpenAPI\Client\Model\GetServerEmailSettings
```

Get server email settings

Retrieve the email settings configured for the server. The password field will be masked if present.

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


$apiInstance = new OpenAPI\Client\Api\ServerEmailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->serverEmailGetSettings();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServerEmailApi->serverEmailGetSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetServerEmailSettings**](../Model/GetServerEmailSettings.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `serverEmailUpdateSettings()`

```php
serverEmailUpdateSettings($update_server_email_settings): \OpenAPI\Client\Model\GetServerEmailSettings
```

Update server email settings

Update server's email settings.

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


$apiInstance = new OpenAPI\Client\Api\ServerEmailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$update_server_email_settings = new \OpenAPI\Client\Model\UpdateServerEmailSettings(); // \OpenAPI\Client\Model\UpdateServerEmailSettings

try {
    $result = $apiInstance->serverEmailUpdateSettings($update_server_email_settings);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServerEmailApi->serverEmailUpdateSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **update_server_email_settings** | [**\OpenAPI\Client\Model\UpdateServerEmailSettings**](../Model/UpdateServerEmailSettings.md)|  | |

### Return type

[**\OpenAPI\Client\Model\GetServerEmailSettings**](../Model/GetServerEmailSettings.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
