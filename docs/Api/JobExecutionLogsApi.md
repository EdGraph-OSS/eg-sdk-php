# EdGraph\PlatformClient\JobExecutionLogsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllTenantDataSyncJobExecutionLogs()**](JobExecutionLogsApi.md#getAllTenantDataSyncJobExecutionLogs) | **GET** /tenants/{tenantId}/datasync/jobs/{jobId}/executions/{jobExecutionId}/logs | Retrieves a list of DataSync Job Execution Logs |


## `getAllTenantDataSyncJobExecutionLogs()`

```php
getAllTenantDataSyncJobExecutionLogs($tenantId, $jobId, $jobExecutionId, $pageSize, $pageIndex, $orderBy, $filter, $search): \EdGraph\PlatformClient\Model\DataSyncApiJobExecutionLogV1JobExecutionLogEntryPaginatedItemsViewModel
```

Retrieves a list of DataSync Job Execution Logs

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobExecutionLogsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$jobExecutionId = 'jobExecutionId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 
$search = ''; // string | 

try {
    $result = $apiInstance->getAllTenantDataSyncJobExecutionLogs($tenantId, $jobId, $jobExecutionId, $pageSize, $pageIndex, $orderBy, $filter, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobExecutionLogsApi->getAllTenantDataSyncJobExecutionLogs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **jobExecutionId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |
| **search** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiJobExecutionLogV1JobExecutionLogEntryPaginatedItemsViewModel**](../Model/DataSyncApiJobExecutionLogV1JobExecutionLogEntryPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
