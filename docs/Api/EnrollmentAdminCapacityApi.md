# EdGraph\PlatformClient\EnrollmentAdminCapacityApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getCapacity()**](EnrollmentAdminCapacityApi.md#getCapacity) | **GET** /tenants/{tenantId}/enrollmentadmin/schools/{schoolCode}/capacity | Searches Capacity for one school - one row per program x grade x school year. |


## `getCapacity()`

```php
getCapacity($tenantId, $schoolCode, $pageSize, $pageIndex, $orderBy, $filter, $grade, $search): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminCapacityListItemDtoPaginatedItemsViewModel
```

Searches Capacity for one school - one row per program x grade x school year.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnrollmentAdminCapacityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$schoolCode = 'schoolCode_example'; // string | Required - a seat count is meaningless without a school.
$pageSize = 50; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 
$grade = ''; // string | Optional exact match.
$search = ''; // string | Free-text match on program name/code.

try {
    $result = $apiInstance->getCapacity($tenantId, $schoolCode, $pageSize, $pageIndex, $orderBy, $filter, $grade, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnrollmentAdminCapacityApi->getCapacity: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **schoolCode** | **string**| Required - a seat count is meaningless without a school. | |
| **pageSize** | **int**|  | [optional] [default to 50] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |
| **grade** | **string**| Optional exact match. | [optional] [default to &#39;&#39;] |
| **search** | **string**| Free-text match on program name/code. | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminCapacityListItemDtoPaginatedItemsViewModel**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminCapacityListItemDtoPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
