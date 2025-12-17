# EdGraph\PlatformClient\UsersApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**activateTenantUserAsync()**](UsersApi.md#activateTenantUserAsync) | **PUT** /tenants/{tenantId}/users/{userId}/activate | Activates a user |
| [**createTenantLocalUserAsync()**](UsersApi.md#createTenantLocalUserAsync) | **POST** /tenants/{tenantId}/users | Creates a user in the local identity provider |
| [**deactivateTenantUserAsync()**](UsersApi.md#deactivateTenantUserAsync) | **PUT** /tenants/{tenantId}/users/{userId}/deactivate | Deactivates a user |
| [**deleteTenantUserAsync()**](UsersApi.md#deleteTenantUserAsync) | **DELETE** /tenants/{tenantId}/users/{userId} | Deletes a user |
| [**getAllTenantUsersAsync()**](UsersApi.md#getAllTenantUsersAsync) | **GET** /tenants/{tenantId}/users | Retrieves a list of users associated to this tenant |
| [**getAllUsers()**](UsersApi.md#getAllUsers) | **GET** /tenants/{tenantId}/statereporting/users | Get All Users |
| [**getTenantUser()**](UsersApi.md#getTenantUser) | **GET** /v2/tenants/{tenantId}/users/{userId} | Get User |
| [**getTenantUserProfileByIdAsync()**](UsersApi.md#getTenantUserProfileByIdAsync) | **GET** /tenants/{tenantId}/users/{userId} | Retrieves a user |
| [**getUserTenant()**](UsersApi.md#getUserTenant) | **GET** /v2/tenants/{tenantId}/users/{userId}/tenant | Get User Tenant |
| [**getUserTenantStatusProfile()**](UsersApi.md#getUserTenantStatusProfile) | **GET** /tenants/{tenantId}/users/{email}/status | Searches a user by email and retrieves it&#39;s minimal information and status. |
| [**resetMfaStatusAsync()**](UsersApi.md#resetMfaStatusAsync) | **PUT** /tenants/{tenantId}/users/{userId}/resetmfa | Reset the MFA Status for the User |
| [**resetPasswordTenantUserAsync()**](UsersApi.md#resetPasswordTenantUserAsync) | **PUT** /tenants/{tenantId}/users/{userId}/resetpassword | Resets a user&#39;s password |
| [**searchTenantUsers()**](UsersApi.md#searchTenantUsers) | **GET** /v2/tenants/{tenantId}/users | Search Users |
| [**searchUserLicenses()**](UsersApi.md#searchUserLicenses) | **GET** /v2/tenants/{tenantId}/users/{userId}/licenses | Search User Licenses |
| [**searchUserLicensesBulk()**](UsersApi.md#searchUserLicensesBulk) | **GET** /v2/tenants/{tenantId}/users/licensesBulk | Search user licenses in bulk. |
| [**updateTenantUserAsync()**](UsersApi.md#updateTenantUserAsync) | **PUT** /tenants/{tenantId}/users/{userId} | Creates or updates a user |


## `activateTenantUserAsync()`

```php
activateTenantUserAsync($tenantId, $userId, $identityApiUserV1ActivateUserRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1UserActivatedResponse
```

Activates a user

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$identityApiUserV1ActivateUserRequest = new \EdGraph\PlatformClient\Model\IdentityApiUserV1ActivateUserRequest(); // \EdGraph\PlatformClient\Model\IdentityApiUserV1ActivateUserRequest | 

try {
    $result = $apiInstance->activateTenantUserAsync($tenantId, $userId, $identityApiUserV1ActivateUserRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->activateTenantUserAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **identityApiUserV1ActivateUserRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiUserV1ActivateUserRequest**](../Model/IdentityApiUserV1ActivateUserRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1UserActivatedResponse**](../Model/IdentityApiUserV1UserActivatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createTenantLocalUserAsync()`

```php
createTenantLocalUserAsync($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1LocalUserCreatedResponse
```

Creates a user in the local identity provider

Note: This is only used to create a user in the local identity provider, i.e. this cannot be used to create a user in an external identity providers such as Microsoft or Google.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest | 

try {
    $result = $apiInstance->createTenantLocalUserAsync($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->createTenantLocalUserAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1LocalUserCreatedResponse**](../Model/IdentityApiUserV1LocalUserCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deactivateTenantUserAsync()`

```php
deactivateTenantUserAsync($tenantId, $userId, $identityApiUserV1DeactivateUserRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1UserDeactivatedResponse
```

Deactivates a user

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$identityApiUserV1DeactivateUserRequest = new \EdGraph\PlatformClient\Model\IdentityApiUserV1DeactivateUserRequest(); // \EdGraph\PlatformClient\Model\IdentityApiUserV1DeactivateUserRequest | 

try {
    $result = $apiInstance->deactivateTenantUserAsync($tenantId, $userId, $identityApiUserV1DeactivateUserRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->deactivateTenantUserAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **identityApiUserV1DeactivateUserRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiUserV1DeactivateUserRequest**](../Model/IdentityApiUserV1DeactivateUserRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1UserDeactivatedResponse**](../Model/IdentityApiUserV1UserDeactivatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteTenantUserAsync()`

```php
deleteTenantUserAsync($tenantId, $userId)
```

Deletes a user

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 

try {
    $apiInstance->deleteTenantUserAsync($tenantId, $userId);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->deleteTenantUserAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllTenantUsersAsync()`

```php
getAllTenantUsersAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicensePaginatedItemsViewModel
```

Retrieves a list of users associated to this tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getAllTenantUsersAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->getAllTenantUsersAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicensePaginatedItemsViewModel**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicensePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllUsers()`

```php
getAllUsers($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponsePaginatedItemsViewModel
```

Get All Users

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int
$pageIndex = 0; // int
$orderBy = ''; // string
$filter = ''; // string

try {
    $result = $apiInstance->getAllUsers($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->getAllUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponsePaginatedItemsViewModel**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantUser()`

```php
getTenantUser($tenantId, $userId): \EdGraph\PlatformClient\Model\IdentityApiUserV2UserProfileResponse
```

Get User

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 

try {
    $result = $apiInstance->getTenantUser($tenantId, $userId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->getTenantUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV2UserProfileResponse**](../Model/IdentityApiUserV2UserProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantUserProfileByIdAsync()`

```php
getTenantUserProfileByIdAsync($tenantId, $userId): \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfileResponseWithApplicationLicense
```

Retrieves a user

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 

try {
    $result = $apiInstance->getTenantUserProfileByIdAsync($tenantId, $userId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->getTenantUserProfileByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfileResponseWithApplicationLicense**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfileResponseWithApplicationLicense.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getUserTenant()`

```php
getUserTenant($tenantId, $userId): \EdGraph\PlatformClient\Model\IdentityApiUserV2UserTenantProfileResponse
```

Get User Tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 

try {
    $result = $apiInstance->getUserTenant($tenantId, $userId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->getUserTenant: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV2UserTenantProfileResponse**](../Model/IdentityApiUserV2UserTenantProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getUserTenantStatusProfile()`

```php
getUserTenantStatusProfile($tenantId, $email): \EdGraph\PlatformClient\Model\IdentityApiUserV1UserTenantStatusProfile
```

Searches a user by email and retrieves it's minimal information and status.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$email = 'email_example'; // string | 

try {
    $result = $apiInstance->getUserTenantStatusProfile($tenantId, $email);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->getUserTenantStatusProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **email** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1UserTenantStatusProfile**](../Model/IdentityApiUserV1UserTenantStatusProfile.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `resetMfaStatusAsync()`

```php
resetMfaStatusAsync($tenantId, $userId)
```

Reset the MFA Status for the User

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$userId = 'userId_example'; // string

try {
    $apiInstance->resetMfaStatusAsync($tenantId, $userId);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->resetMfaStatusAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `resetPasswordTenantUserAsync()`

```php
resetPasswordTenantUserAsync($tenantId, $userId, $identityApiUserV1ResetPasswordRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1PasswordResettedResponse
```

Resets a user's password

Note: This is only applicable to user created in the local identity provider.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$identityApiUserV1ResetPasswordRequest = new \EdGraph\PlatformClient\Model\IdentityApiUserV1ResetPasswordRequest(); // \EdGraph\PlatformClient\Model\IdentityApiUserV1ResetPasswordRequest | 

try {
    $result = $apiInstance->resetPasswordTenantUserAsync($tenantId, $userId, $identityApiUserV1ResetPasswordRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->resetPasswordTenantUserAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **identityApiUserV1ResetPasswordRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiUserV1ResetPasswordRequest**](../Model/IdentityApiUserV1ResetPasswordRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1PasswordResettedResponse**](../Model/IdentityApiUserV1PasswordResettedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchTenantUsers()`

```php
searchTenantUsers($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\IdentityApiUserV2UsersSearchResponse
```

Search Users

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->searchTenantUsers($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->searchTenantUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV2UsersSearchResponse**](../Model/IdentityApiUserV2UsersSearchResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchUserLicenses()`

```php
searchUserLicenses($tenantId, $userId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\IdentityApiUserV2UserLicensesResponse
```

Search User Licenses

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->searchUserLicenses($tenantId, $userId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->searchUserLicenses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV2UserLicensesResponse**](../Model/IdentityApiUserV2UserLicensesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchUserLicensesBulk()`

```php
searchUserLicensesBulk($tenantId, $userId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResultBulk[]
```

Search user licenses in bulk.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = array('userId_example'); // string[] | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->searchUserLicensesBulk($tenantId, $userId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->searchUserLicensesBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | [**string[]**](../Model/string.md)|  | [optional] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResultBulk[]**](../Model/EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResultBulk.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTenantUserAsync()`

```php
updateTenantUserAsync($tenantId, $userId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1UserUpdatedResponse
```

Creates or updates a user

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest | 

try {
    $result = $apiInstance->updateTenantUserAsync($tenantId, $userId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->updateTenantUserAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1UserUpdatedResponse**](../Model/IdentityApiUserV1UserUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
