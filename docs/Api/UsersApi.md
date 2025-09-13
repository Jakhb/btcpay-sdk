# OpenAPI\Client\UsersApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**usersCreateUser()**](UsersApi.md#usersCreateUser) | **POST** /api/v1/users | Create user |
| [**usersDeleteCurrentUser()**](UsersApi.md#usersDeleteCurrentUser) | **DELETE** /api/v1/users/me | Deletes user profile |
| [**usersDeleteCurrentUserProfilePicture()**](UsersApi.md#usersDeleteCurrentUserProfilePicture) | **DELETE** /api/v1/users/me/picture | Deletes user profile picture |
| [**usersDeleteUser()**](UsersApi.md#usersDeleteUser) | **DELETE** /api/v1/users/{idOrEmail} | Delete user |
| [**usersGetCurrentUser()**](UsersApi.md#usersGetCurrentUser) | **GET** /api/v1/users/me | Get current user information |
| [**usersGetUser()**](UsersApi.md#usersGetUser) | **GET** /api/v1/users/{idOrEmail} | Get user by ID or Email |
| [**usersGetUsers()**](UsersApi.md#usersGetUsers) | **GET** /api/v1/users | Get all users |
| [**usersToggleUserApproval()**](UsersApi.md#usersToggleUserApproval) | **POST** /api/v1/users/{idOrEmail}/approve | Toggle user approval |
| [**usersToggleUserLock()**](UsersApi.md#usersToggleUserLock) | **POST** /api/v1/users/{idOrEmail}/lock | Toggle user lock out |
| [**usersUpdateCurrentUser()**](UsersApi.md#usersUpdateCurrentUser) | **PUT** /api/v1/users/me | Update current user information |
| [**usersUploadCurrentUserProfilePicture()**](UsersApi.md#usersUploadCurrentUserProfilePicture) | **POST** /api/v1/users/me/picture | Uploads a profile picture for the current user |


## `usersCreateUser()`

```php
usersCreateUser($users_create_user_request): \OpenAPI\Client\Model\ApplicationUserData
```

Create user

Create a new user.  This operation can be called without authentication in any of this cases: * There is not any administrator yet on the server, * User registrations are not disabled in the server's policies.  If the first administrator is created by this call, user registrations are automatically disabled.

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


$apiInstance = new OpenAPI\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$users_create_user_request = new \OpenAPI\Client\Model\UsersCreateUserRequest(); // \OpenAPI\Client\Model\UsersCreateUserRequest

try {
    $result = $apiInstance->usersCreateUser($users_create_user_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersCreateUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **users_create_user_request** | [**\OpenAPI\Client\Model\UsersCreateUserRequest**](../Model/UsersCreateUserRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ApplicationUserData**](../Model/ApplicationUserData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `usersDeleteCurrentUser()`

```php
usersDeleteCurrentUser()
```

Deletes user profile

Deletes user profile and associated user data for user making the request

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


$apiInstance = new OpenAPI\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $apiInstance->usersDeleteCurrentUser();
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersDeleteCurrentUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

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

## `usersDeleteCurrentUserProfilePicture()`

```php
usersDeleteCurrentUserProfilePicture()
```

Deletes user profile picture

Deletes the user profile picture

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


$apiInstance = new OpenAPI\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $apiInstance->usersDeleteCurrentUserProfilePicture();
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersDeleteCurrentUserProfilePicture: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

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

## `usersDeleteUser()`

```php
usersDeleteUser($id_or_email)
```

Delete user

Delete a user.  Must be an admin to perform this operation.  Attempting to delete the only admin user will not succeed.  All data associated with the user will be deleted as well if the operation succeeds.

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


$apiInstance = new OpenAPI\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id_or_email = 'id_or_email_example'; // string | The user's id or email

try {
    $apiInstance->usersDeleteUser($id_or_email);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersDeleteUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id_or_email** | **string**| The user&#39;s id or email | |

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

## `usersGetCurrentUser()`

```php
usersGetCurrentUser(): \OpenAPI\Client\Model\ApplicationUserData
```

Get current user information

View information about the current user

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


$apiInstance = new OpenAPI\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->usersGetCurrentUser();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersGetCurrentUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\ApplicationUserData**](../Model/ApplicationUserData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `usersGetUser()`

```php
usersGetUser($id_or_email): \OpenAPI\Client\Model\ApplicationUserData
```

Get user by ID or Email

Get 1 user by ID or Email.

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


$apiInstance = new OpenAPI\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id_or_email = 'id_or_email_example'; // string | The user's id or email

try {
    $result = $apiInstance->usersGetUser($id_or_email);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersGetUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id_or_email** | **string**| The user&#39;s id or email | |

### Return type

[**\OpenAPI\Client\Model\ApplicationUserData**](../Model/ApplicationUserData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `usersGetUsers()`

```php
usersGetUsers()
```

Get all users

Load all users that exist.

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


$apiInstance = new OpenAPI\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $apiInstance->usersGetUsers();
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersGetUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

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

## `usersToggleUserApproval()`

```php
usersToggleUserApproval($id_or_email, $approve_user_request)
```

Toggle user approval

Approve or unapprove a user.  Must be an admin to perform this operation.  Attempting to (un)approve a user for which this requirement does not exist will not succeed.

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


$apiInstance = new OpenAPI\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id_or_email = 'id_or_email_example'; // string | The user's id or email
$approve_user_request = new \OpenAPI\Client\Model\ApproveUserRequest(); // \OpenAPI\Client\Model\ApproveUserRequest

try {
    $apiInstance->usersToggleUserApproval($id_or_email, $approve_user_request);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersToggleUserApproval: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id_or_email** | **string**| The user&#39;s id or email | |
| **approve_user_request** | [**\OpenAPI\Client\Model\ApproveUserRequest**](../Model/ApproveUserRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `usersToggleUserLock()`

```php
usersToggleUserLock($id_or_email, $lock_user_request)
```

Toggle user lock out

Lock or unlock a user.  Must be an admin to perform this operation.  Attempting to lock the only admin user will not succeed.

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


$apiInstance = new OpenAPI\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id_or_email = 'id_or_email_example'; // string | The user's id or email
$lock_user_request = new \OpenAPI\Client\Model\LockUserRequest(); // \OpenAPI\Client\Model\LockUserRequest

try {
    $apiInstance->usersToggleUserLock($id_or_email, $lock_user_request);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersToggleUserLock: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id_or_email** | **string**| The user&#39;s id or email | |
| **lock_user_request** | [**\OpenAPI\Client\Model\LockUserRequest**](../Model/LockUserRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `usersUpdateCurrentUser()`

```php
usersUpdateCurrentUser($users_update_current_user_request): \OpenAPI\Client\Model\ApplicationUserData
```

Update current user information

Update the current user

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


$apiInstance = new OpenAPI\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$users_update_current_user_request = new \OpenAPI\Client\Model\UsersUpdateCurrentUserRequest(); // \OpenAPI\Client\Model\UsersUpdateCurrentUserRequest

try {
    $result = $apiInstance->usersUpdateCurrentUser($users_update_current_user_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersUpdateCurrentUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **users_update_current_user_request** | [**\OpenAPI\Client\Model\UsersUpdateCurrentUserRequest**](../Model/UsersUpdateCurrentUserRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ApplicationUserData**](../Model/ApplicationUserData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `usersUploadCurrentUserProfilePicture()`

```php
usersUploadCurrentUserProfilePicture($file): \OpenAPI\Client\Model\ApplicationUserData
```

Uploads a profile picture for the current user

Uploads a profile picture for the current user

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


$apiInstance = new OpenAPI\Client\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = '/path/to/file.txt'; // \SplFileObject | The profile picture

try {
    $result = $apiInstance->usersUploadCurrentUserProfilePicture($file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersUploadCurrentUserProfilePicture: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **\SplFileObject****\SplFileObject**| The profile picture | [optional] |

### Return type

[**\OpenAPI\Client\Model\ApplicationUserData**](../Model/ApplicationUserData.md)

### Authorization

[Basic](../../README.md#Basic), [API_Key](../../README.md#API_Key)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
