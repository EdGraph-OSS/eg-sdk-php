# EdGraph\PlatformClient\MyProfileApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getMyProfile()**](MyProfileApi.md#getMyProfile) | **GET** /v2/me | Get the profile of the user that is currently logged in. |
| [**getMyTenant()**](MyProfileApi.md#getMyTenant) | **GET** /v2/me/tenants/{tenantId} | Get the tenant associated to the user. |
| [**getUserCacheAsync()**](MyProfileApi.md#getUserCacheAsync) | **GET** /me | Retrieves the profile of the user that is currently logged in, including the user&#39;s preferences and its associated tenants |


## `getMyProfile()`

```php
getMyProfile(): \EdGraph\PlatformClient\Model\IdentityApiUserV2UserMeProfile
```

Get the profile of the user that is currently logged in.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MyProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getMyProfile();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyProfileApi->getMyProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV2UserMeProfile**](../Model/IdentityApiUserV2UserMeProfile.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMyTenant()`

```php
getMyTenant($tenantId): \EdGraph\PlatformClient\Model\IdentityApiUserV2TenantMeProfile
```

Get the tenant associated to the user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MyProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string

try {
    $result = $apiInstance->getMyTenant($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyProfileApi->getMyTenant: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV2TenantMeProfile**](../Model/IdentityApiUserV2TenantMeProfile.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getUserCacheAsync()`

```php
getUserCacheAsync($numberOfTenants): \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheResponse
```

Retrieves the profile of the user that is currently logged in, including the user's preferences and its associated tenants

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MyProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$numberOfTenants = 10; // int

try {
    $result = $apiInstance->getUserCacheAsync($numberOfTenants);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyProfileApi->getUserCacheAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **numberOfTenants** | **int**|  | [optional] [default to 10] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheResponse**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
