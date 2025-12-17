# EdGraph\PlatformClient\JobTypesApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllTenantDataSyncJobTypes()**](JobTypesApi.md#getAllTenantDataSyncJobTypes) | **GET** /tenants/{tenantId}/datasync/jobtypes | Retrieves a list of DataSync job types |
| [**getTenantDataSyncJobTypeProfileById()**](JobTypesApi.md#getTenantDataSyncJobTypeProfileById) | **GET** /tenants/{tenantId}/datasync/jobtypes/{jobTypeId} | Retrieves a specific DataSync job type using its primary key |


## `getAllTenantDataSyncJobTypes()`

```php
getAllTenantDataSyncJobTypes($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\DataSyncApiJobTypeV1JobTypeListResponsePaginatedItemsViewModel
```

Retrieves a list of DataSync job types

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobTypesApi(
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
    $result = $apiInstance->getAllTenantDataSyncJobTypes($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobTypesApi->getAllTenantDataSyncJobTypes: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\DataSyncApiJobTypeV1JobTypeListResponsePaginatedItemsViewModel**](../Model/DataSyncApiJobTypeV1JobTypeListResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantDataSyncJobTypeProfileById()`

```php
getTenantDataSyncJobTypeProfileById($tenantId, $jobTypeId): \EdGraph\PlatformClient\Model\DataSyncApiJobTypeV1JobTypeProfileResponse
```

Retrieves a specific DataSync job type using its primary key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobTypesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobTypeId = 'jobTypeId_example'; // string | 

try {
    $result = $apiInstance->getTenantDataSyncJobTypeProfileById($tenantId, $jobTypeId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobTypesApi->getTenantDataSyncJobTypeProfileById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobTypeId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiJobTypeV1JobTypeProfileResponse**](../Model/DataSyncApiJobTypeV1JobTypeProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
