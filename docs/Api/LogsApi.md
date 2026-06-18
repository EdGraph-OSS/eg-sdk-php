# EdGraph\PlatformClient\LogsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getLogs()**](LogsApi.md#getLogs) | **GET** /tenants/{tenantId}/validations/logs | Retrieves a list of Logs. |


## `getLogs()`

```php
getLogs($tenantId, $pageIndex, $pageSize, $orderBy, $environmentId, $collectionId, $containerId, $ruleId, $jobId, $jobExecutionId): \EdGraph\PlatformClient\Model\ValidationsApiValidationResultsV1FindResponse
```

Retrieves a list of Logs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\LogsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = 'orderBy_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$collectionId = 'collectionId_example'; // string | 
$containerId = 'containerId_example'; // string | 
$ruleId = 'ruleId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$jobExecutionId = 'jobExecutionId_example'; // string | 

try {
    $result = $apiInstance->getLogs($tenantId, $pageIndex, $pageSize, $orderBy, $environmentId, $collectionId, $containerId, $ruleId, $jobId, $jobExecutionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LogsApi->getLogs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] |
| **environmentId** | **string**|  | [optional] |
| **collectionId** | **string**|  | [optional] |
| **containerId** | **string**|  | [optional] |
| **ruleId** | **string**|  | [optional] |
| **jobId** | **string**|  | [optional] |
| **jobExecutionId** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiValidationResultsV1FindResponse**](../Model/ValidationsApiValidationResultsV1FindResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
