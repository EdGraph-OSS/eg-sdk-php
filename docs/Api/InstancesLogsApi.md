# EdGraph\PlatformClient\InstancesLogsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getInstanceHttpLogs()**](InstancesLogsApi.md#getInstanceHttpLogs) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/logs/http | Retrieves HTTP logs for a given instance |


## `getInstanceHttpLogs()`

```php
getInstanceHttpLogs($tenantId, $instanceId, $year, $pageSize, $pageIndex, $from, $to, $field, $order): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLogPaginatedItemsViewModel
```

Retrieves HTTP logs for a given instance

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesLogsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$from = 0; // int | 
$to = 0; // int | 
$field = ''; // string | 
$order = false; // bool | 

try {
    $result = $apiInstance->getInstanceHttpLogs($tenantId, $instanceId, $year, $pageSize, $pageIndex, $from, $to, $field, $order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesLogsApi->getInstanceHttpLogs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **from** | **int**|  | [optional] [default to 0] |
| **to** | **int**|  | [optional] [default to 0] |
| **field** | **string**|  | [optional] [default to &#39;&#39;] |
| **order** | **bool**|  | [optional] [default to false] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLogPaginatedItemsViewModel**](../Model/EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLogPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
