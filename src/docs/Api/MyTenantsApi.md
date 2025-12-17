# EdGraph\PlatformClient\MyTenantsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getUserTenants()**](MyTenantsApi.md#getUserTenants) | **GET** /me/tenants | Retrieves the Tenants of the User that is currently logged in. |
| [**searchMyLicenses()**](MyTenantsApi.md#searchMyLicenses) | **GET** /v2/me/tenants/{tenantId}/licenses | Search the user&#39;s licenses. |
| [**searchMyTenants()**](MyTenantsApi.md#searchMyTenants) | **GET** /v2/me/tenants | Searches tenants associated to the user. |


## `getUserTenants()`

```php
getUserTenants($pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel
```

Retrieves the Tenants of the User that is currently logged in.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MyTenantsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$pageIndex = 0; // int
$pageSize = 10; // int
$filter = ''; // string
$orderBy = ''; // string

try {
    $result = $apiInstance->getUserTenants($pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyTenantsApi->getUserTenants: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel**](../Model/IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchMyLicenses()`

```php
searchMyLicenses($tenantId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel
```

Search the user's licenses.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MyTenantsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$pageIndex = 0; // int
$pageSize = 10; // int
$filter = ''; // string
$orderBy = ''; // string

try {
    $result = $apiInstance->searchMyLicenses($tenantId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyTenantsApi->searchMyLicenses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel**](../Model/IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchMyTenants()`

```php
searchMyTenants($pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel
```

Searches tenants associated to the user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MyTenantsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$pageIndex = 0; // int
$pageSize = 10; // int
$filter = ''; // string
$orderBy = ''; // string

try {
    $result = $apiInstance->searchMyTenants($pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyTenantsApi->searchMyTenants: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel**](../Model/IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
