# EdGraph\PlatformClient\UsersLicensesApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**assignLicenseTenantUserAsync()**](UsersLicensesApi.md#assignLicenseTenantUserAsync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/assign | Assigns a license to a user in the context of a specific tenant |
| [**assignLicenseTenantUserBulkAsync()**](UsersLicensesApi.md#assignLicenseTenantUserBulkAsync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/assignbulk | Assigns one or more licenses to a user in the context of a specific tenant |
| [**getAllTenantUserApplicationLicensesAsync()**](UsersLicensesApi.md#getAllTenantUserApplicationLicensesAsync) | **GET** /tenants/{tenantId}/users/{userId}/licenses | Retrieves a list of user licenses in the context of a specific tenant |
| [**revokeLicenseTenantUserAsync()**](UsersLicensesApi.md#revokeLicenseTenantUserAsync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/revoke | Revokes a license from a user in the context of a specific tenant |
| [**revokeLicenseTenantUserBulkAsync()**](UsersLicensesApi.md#revokeLicenseTenantUserBulkAsync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/revokebulk | Revokes one or more licenses from a user in the context of a specific tenant |


## `assignLicenseTenantUserAsync()`

```php
assignLicenseTenantUserAsync($tenantId, $userId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1LicenseAssignedResponse
```

Assigns a license to a user in the context of a specific tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersLicensesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest | 

try {
    $result = $apiInstance->assignLicenseTenantUserAsync($tenantId, $userId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersLicensesApi->assignLicenseTenantUserAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1LicenseAssignedResponse**](../Model/IdentityApiUserV1LicenseAssignedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `assignLicenseTenantUserBulkAsync()`

```php
assignLicenseTenantUserBulkAsync($tenantId, $userId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1LicenseAssignedBulkResponse
```

Assigns one or more licenses to a user in the context of a specific tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersLicensesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest | 

try {
    $result = $apiInstance->assignLicenseTenantUserBulkAsync($tenantId, $userId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersLicensesApi->assignLicenseTenantUserBulkAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1LicenseAssignedBulkResponse**](../Model/IdentityApiUserV1LicenseAssignedBulkResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllTenantUserApplicationLicensesAsync()`

```php
getAllTenantUserApplicationLicensesAsync($tenantId, $userId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel
```

Retrieves a list of user licenses in the context of a specific tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersLicensesApi(
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
    $result = $apiInstance->getAllTenantUserApplicationLicensesAsync($tenantId, $userId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersLicensesApi->getAllTenantUserApplicationLicensesAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `revokeLicenseTenantUserAsync()`

```php
revokeLicenseTenantUserAsync($tenantId, $userId, $identityApiUserV1RevokeLicenseRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1LicenseRevokedResponse
```

Revokes a license from a user in the context of a specific tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersLicensesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$identityApiUserV1RevokeLicenseRequest = new \EdGraph\PlatformClient\Model\IdentityApiUserV1RevokeLicenseRequest(); // \EdGraph\PlatformClient\Model\IdentityApiUserV1RevokeLicenseRequest | 

try {
    $result = $apiInstance->revokeLicenseTenantUserAsync($tenantId, $userId, $identityApiUserV1RevokeLicenseRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersLicensesApi->revokeLicenseTenantUserAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **identityApiUserV1RevokeLicenseRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiUserV1RevokeLicenseRequest**](../Model/IdentityApiUserV1RevokeLicenseRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1LicenseRevokedResponse**](../Model/IdentityApiUserV1LicenseRevokedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `revokeLicenseTenantUserBulkAsync()`

```php
revokeLicenseTenantUserBulkAsync($tenantId, $userId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1LicenseRevokedBulkResponse
```

Revokes one or more licenses from a user in the context of a specific tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersLicensesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest | 

try {
    $result = $apiInstance->revokeLicenseTenantUserBulkAsync($tenantId, $userId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersLicensesApi->revokeLicenseTenantUserBulkAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1LicenseRevokedBulkResponse**](../Model/IdentityApiUserV1LicenseRevokedBulkResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
