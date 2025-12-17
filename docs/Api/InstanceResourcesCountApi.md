# EdGraph\PlatformClient\InstanceResourcesCountApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllInstanceResourcesCountAsync()**](InstanceResourcesCountApi.md#getAllInstanceResourcesCountAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/applications/{applicationId}/apiclients/{apiClientId}/resourcescount | Retrieves a paginated list of Instance Resources Count |
| [**getAllInstanceResourcesCountJson()**](InstanceResourcesCountApi.md#getAllInstanceResourcesCountJson) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/applications/{applicationId}/apiclients/{apiClientId}/resourcescount/export | Retrieves the JSON representation of Instance Resources Count. Useful for exporting into other systems. |


## `getAllInstanceResourcesCountAsync()`

```php
getAllInstanceResourcesCountAsync($tenantId, $instanceId, $year, $applicationId, $apiClientId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponsePaginatedItemsViewModel
```

Retrieves a paginated list of Instance Resources Count

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstanceResourcesCountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$applicationId = 56; // int | 
$apiClientId = 56; // int | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getAllInstanceResourcesCountAsync($tenantId, $instanceId, $year, $applicationId, $apiClientId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstanceResourcesCountApi->getAllInstanceResourcesCountAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **applicationId** | **int**|  | |
| **apiClientId** | **int**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponsePaginatedItemsViewModel**](../Model/EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllInstanceResourcesCountJson()`

```php
getAllInstanceResourcesCountJson($tenantId, $instanceId, $year, $applicationId, $apiClientId, $filter): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceResourcesCountJsonResponse
```

Retrieves the JSON representation of Instance Resources Count. Useful for exporting into other systems.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstanceResourcesCountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$applicationId = 56; // int | 
$apiClientId = 56; // int | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getAllInstanceResourcesCountJson($tenantId, $instanceId, $year, $applicationId, $apiClientId, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstanceResourcesCountApi->getAllInstanceResourcesCountJson: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **applicationId** | **int**|  | |
| **apiClientId** | **int**|  | |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceResourcesCountJsonResponse**](../Model/EdfiAdminApiEdfiAdminV1InstanceResourcesCountJsonResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
