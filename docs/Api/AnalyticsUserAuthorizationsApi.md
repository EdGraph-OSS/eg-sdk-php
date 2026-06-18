# EdGraph\PlatformClient\AnalyticsUserAuthorizationsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getPaginatedUserAuthorizations()**](AnalyticsUserAuthorizationsApi.md#getPaginatedUserAuthorizations) | **GET** /tenants/{tenantId}/analytics/userauthorizations | Retrieves paginated user authorizations |
| [**softDeleteUserAuthorization()**](AnalyticsUserAuthorizationsApi.md#softDeleteUserAuthorization) | **DELETE** /tenants/{tenantId}/analytics/userauthorizations/{userAuthorizationId} | Soft Deletes a user authorization by Id |


## `getPaginatedUserAuthorizations()`

```php
getPaginatedUserAuthorizations($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse
```

Retrieves paginated user authorizations

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\AnalyticsUserAuthorizationsApi(
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
    $result = $apiInstance->getPaginatedUserAuthorizations($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnalyticsUserAuthorizationsApi->getPaginatedUserAuthorizations: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse**](../Model/AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `softDeleteUserAuthorization()`

```php
softDeleteUserAuthorization($tenantId, $userAuthorizationId): \EdGraph\PlatformClient\Model\AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse
```

Soft Deletes a user authorization by Id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\AnalyticsUserAuthorizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userAuthorizationId = 'userAuthorizationId_example'; // string | 

try {
    $result = $apiInstance->softDeleteUserAuthorization($tenantId, $userAuthorizationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnalyticsUserAuthorizationsApi->softDeleteUserAuthorization: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userAuthorizationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse**](../Model/AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
