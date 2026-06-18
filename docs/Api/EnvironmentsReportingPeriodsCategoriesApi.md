# EdGraph\PlatformClient\EnvironmentsReportingPeriodsCategoriesApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**searchStateReportingPeriodCategories()**](EnvironmentsReportingPeriodsCategoriesApi.md#searchStateReportingPeriodCategories) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/categories | Retrieves the Categories of a Reporting Period. |
| [**searchStateReportingPeriodSubCategories()**](EnvironmentsReportingPeriodsCategoriesApi.md#searchStateReportingPeriodSubCategories) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/categories/{categoryId}/subcategories | Retrieves the Sub-Categories of a Reporting Period. |


## `searchStateReportingPeriodCategories()`

```php
searchStateReportingPeriodCategories($tenantId, $environmentId, $reportingPeriodId, $pageIndex, $pageSize, $orderBy): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedCategories
```

Retrieves the Categories of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsCategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$pageIndex = 56; // int | 
$pageSize = 56; // int | 
$orderBy = 'orderBy_example'; // string | 

try {
    $result = $apiInstance->searchStateReportingPeriodCategories($tenantId, $environmentId, $reportingPeriodId, $pageIndex, $pageSize, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsCategoriesApi->searchStateReportingPeriodCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] |
| **pageSize** | **int**|  | [optional] |
| **orderBy** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedCategories**](../Model/EdGraphServicesStateReportingV1PaginatedCategories.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchStateReportingPeriodSubCategories()`

```php
searchStateReportingPeriodSubCategories($tenantId, $environmentId, $reportingPeriodId, $categoryId, $pageIndex, $pageSize, $orderBy): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedSubCategories
```

Retrieves the Sub-Categories of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsCategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$categoryId = 'categoryId_example'; // string | 
$pageIndex = 56; // int | 
$pageSize = 56; // int | 
$orderBy = 'orderBy_example'; // string | 

try {
    $result = $apiInstance->searchStateReportingPeriodSubCategories($tenantId, $environmentId, $reportingPeriodId, $categoryId, $pageIndex, $pageSize, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsCategoriesApi->searchStateReportingPeriodSubCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **categoryId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] |
| **pageSize** | **int**|  | [optional] |
| **orderBy** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedSubCategories**](../Model/EdGraphServicesStateReportingV1PaginatedSubCategories.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
