# EdGraph\PlatformClient\EdFiInstancesApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllEdFiAdminConnectionsFromAnalyticsAsync()**](EdFiInstancesApi.md#getAllEdFiAdminConnectionsFromAnalyticsAsync) | **GET** /tenants/{tenantId}/analytics/edfiadmin/connections | Retrieves a list of EdFi Admin connections |
| [**getAllEdFiAdminInstancesFromAnalyticsAsync()**](EdFiInstancesApi.md#getAllEdFiAdminInstancesFromAnalyticsAsync) | **GET** /tenants/{tenantId}/analytics/edfiadmin/instances | Retrieves a list of EdFi Admin instances |
| [**getEdFiAdminInstanceByIdFromAnalyticsAsync()**](EdFiInstancesApi.md#getEdFiAdminInstanceByIdFromAnalyticsAsync) | **GET** /tenants/{tenantId}/analytics/edfiadmin/instances/{instanceId} | Retrieves an Ed-Fi Admin instance by ID. |


## `getAllEdFiAdminConnectionsFromAnalyticsAsync()`

```php
getAllEdFiAdminConnectionsFromAnalyticsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportPaginatedItemsResponse
```

Retrieves a list of EdFi Admin connections

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EdFiInstancesApi(
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
    $result = $apiInstance->getAllEdFiAdminConnectionsFromAnalyticsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EdFiInstancesApi->getAllEdFiAdminConnectionsFromAnalyticsAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportPaginatedItemsResponse**](../Model/AnalyticsApiReportsV1ReportPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllEdFiAdminInstancesFromAnalyticsAsync()`

```php
getAllEdFiAdminInstancesFromAnalyticsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportPaginatedItemsResponse
```

Retrieves a list of EdFi Admin instances

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EdFiInstancesApi(
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
    $result = $apiInstance->getAllEdFiAdminInstancesFromAnalyticsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EdFiInstancesApi->getAllEdFiAdminInstancesFromAnalyticsAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportPaginatedItemsResponse**](../Model/AnalyticsApiReportsV1ReportPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEdFiAdminInstanceByIdFromAnalyticsAsync()`

```php
getEdFiAdminInstanceByIdFromAnalyticsAsync($tenantId, $instanceId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1Instance
```

Retrieves an Ed-Fi Admin instance by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EdFiInstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->getEdFiAdminInstanceByIdFromAnalyticsAsync($tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EdFiInstancesApi->getEdFiAdminInstanceByIdFromAnalyticsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1Instance**](../Model/EdfiAdminApiEdfiAdminV1Instance.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
