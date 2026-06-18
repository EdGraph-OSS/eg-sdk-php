# EdGraph\PlatformClient\JobExecutionsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllTenantDataSyncJobExecutions()**](JobExecutionsApi.md#getAllTenantDataSyncJobExecutions) | **GET** /tenants/{tenantId}/datasync/jobs/{jobId}/executions | Retrieves a list of DataSync Job Executions |
| [**getTenantJobExecutionsByJobId()**](JobExecutionsApi.md#getTenantJobExecutionsByJobId) | **GET** /tenants/{tenantId}/jobs/{jobId}/executions | Gets job executions by a given job Id |


## `getAllTenantDataSyncJobExecutions()`

```php
getAllTenantDataSyncJobExecutions($tenantId, $jobId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\DataSyncApiJobExecutionV1JobExecutionListResponsePaginatedItemsViewModel
```

Retrieves a list of DataSync Job Executions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobExecutionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getAllTenantDataSyncJobExecutions($tenantId, $jobId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobExecutionsApi->getAllTenantDataSyncJobExecutions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiJobExecutionV1JobExecutionListResponsePaginatedItemsViewModel**](../Model/DataSyncApiJobExecutionV1JobExecutionListResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantJobExecutionsByJobId()`

```php
getTenantJobExecutionsByJobId($tenantId, $jobId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\DataSyncApiJobExecutionV1JobExecutionListResponsePaginatedItemsViewModel
```

Gets job executions by a given job Id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobExecutionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getTenantJobExecutionsByJobId($tenantId, $jobId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobExecutionsApi->getTenantJobExecutionsByJobId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiJobExecutionV1JobExecutionListResponsePaginatedItemsViewModel**](../Model/DataSyncApiJobExecutionV1JobExecutionListResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
