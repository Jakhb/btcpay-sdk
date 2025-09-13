# OpenAPI\Client\AuthorizationApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiKeysAuthorize()**](AuthorizationApi.md#apiKeysAuthorize) | **GET** /api-keys/authorize | Authorize User |


## `apiKeysAuthorize()`

```php
apiKeysAuthorize($permissions, $strict, $application_identifier, $selective_stores, $application_name, $redirect)
```

Authorize User

Redirect the browser to this endpoint to request the user to generate an api-key with specific permissions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AuthorizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$permissions = array('permissions_example'); // string[] | The permissions to request. (See API Key authentication)
$strict = true; // bool | If permissions are specified, and strict is set to false, it will allow the user to reject some of permissions the application is requesting.
$application_identifier = 'application_identifier_example'; // string | If specified, BTCPay Server will check if there is an existing API key associated with the user that also has this application identifier, redirect host AND the permissions required match(takes selectiveStores and strict into account). `applicationIdentifier` is ignored if redirect is not specified.
$selective_stores = false; // bool | If the application is requesting the CanModifyStoreSettings permission and selectiveStores is set to true, this allows the user to only grant permissions to selected stores under the user's control.
$application_name = 'application_name_example'; // string | The name of your application
$redirect = 'redirect_example'; // string | The url to redirect to after the user consents, with the query parameters appended to it: permissions, user-id, api-key. If not specified, user is redirected to their API Key list.

try {
    $apiInstance->apiKeysAuthorize($permissions, $strict, $application_identifier, $selective_stores, $application_name, $redirect);
} catch (Exception $e) {
    echo 'Exception when calling AuthorizationApi->apiKeysAuthorize: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **permissions** | [**string[]**](../Model/string.md)| The permissions to request. (See API Key authentication) | [optional] |
| **strict** | **bool**| If permissions are specified, and strict is set to false, it will allow the user to reject some of permissions the application is requesting. | [optional] [default to true] |
| **application_identifier** | **string**| If specified, BTCPay Server will check if there is an existing API key associated with the user that also has this application identifier, redirect host AND the permissions required match(takes selectiveStores and strict into account). &#x60;applicationIdentifier&#x60; is ignored if redirect is not specified. | [optional] |
| **selective_stores** | **bool**| If the application is requesting the CanModifyStoreSettings permission and selectiveStores is set to true, this allows the user to only grant permissions to selected stores under the user&#39;s control. | [optional] [default to false] |
| **application_name** | **string**| The name of your application | [optional] |
| **redirect** | **string**| The url to redirect to after the user consents, with the query parameters appended to it: permissions, user-id, api-key. If not specified, user is redirected to their API Key list. | [optional] |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/html`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
