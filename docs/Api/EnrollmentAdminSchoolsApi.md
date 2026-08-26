# EdGraph\PlatformClient\EnrollmentAdminSchoolsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getEnrollmentSchool()**](EnrollmentAdminSchoolsApi.md#getEnrollmentSchool) | **GET** /tenants/{tenantId}/enrollmentadmin/schools/code/{code} | Gets an Enrollment School by its school code, with the programs it runs. |
| [**getEnrollmentSchoolById()**](EnrollmentAdminSchoolsApi.md#getEnrollmentSchoolById) | **GET** /tenants/{tenantId}/enrollmentadmin/schools/{id} | Gets an Enrollment School by its record id, with the programs it runs. |
| [**getEnrollmentSchools()**](EnrollmentAdminSchoolsApi.md#getEnrollmentSchools) | **GET** /tenants/{tenantId}/enrollmentadmin/schools | Searches Enrollment Schools. |
| [**setEnrollmentSchoolEnabled()**](EnrollmentAdminSchoolsApi.md#setEnrollmentSchoolEnabled) | **PUT** /tenants/{tenantId}/enrollmentadmin/schools/code/{code}/enabled | Enables or disables an Enrollment School. |


## `getEnrollmentSchool()`

```php
getEnrollmentSchool($tenantId, $code): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolResponseDto
```

Gets an Enrollment School by its school code, with the programs it runs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnrollmentAdminSchoolsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$code = 'code_example'; // string | 

try {
    $result = $apiInstance->getEnrollmentSchool($tenantId, $code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnrollmentAdminSchoolsApi->getEnrollmentSchool: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **code** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolResponseDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolResponseDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEnrollmentSchoolById()`

```php
getEnrollmentSchoolById($tenantId, $id): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolResponseDto
```

Gets an Enrollment School by its record id, with the programs it runs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnrollmentAdminSchoolsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$id = 'id_example'; // string | 

try {
    $result = $apiInstance->getEnrollmentSchoolById($tenantId, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnrollmentAdminSchoolsApi->getEnrollmentSchoolById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **id** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolResponseDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolResponseDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEnrollmentSchools()`

```php
getEnrollmentSchools($tenantId, $pageSize, $pageIndex, $orderBy, $filter, $search): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolListItemResponseDtoPaginatedItemsViewModel
```

Searches Enrollment Schools.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnrollmentAdminSchoolsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 50; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 
$search = ''; // string | Free-text match on school name or school code.

try {
    $result = $apiInstance->getEnrollmentSchools($tenantId, $pageSize, $pageIndex, $orderBy, $filter, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnrollmentAdminSchoolsApi->getEnrollmentSchools: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 50] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |
| **search** | **string**| Free-text match on school name or school code. | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolListItemResponseDtoPaginatedItemsViewModel**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolListItemResponseDtoPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setEnrollmentSchoolEnabled()`

```php
setEnrollmentSchoolEnabled($tenantId, $code, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminSetSchoolEnabledRequestDto): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto
```

Enables or disables an Enrollment School.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnrollmentAdminSchoolsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$code = 'code_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminSetSchoolEnabledRequestDto = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminSetSchoolEnabledRequestDto(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminSetSchoolEnabledRequestDto | 

try {
    $result = $apiInstance->setEnrollmentSchoolEnabled($tenantId, $code, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminSetSchoolEnabledRequestDto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnrollmentAdminSchoolsApi->setEnrollmentSchoolEnabled: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **code** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminSetSchoolEnabledRequestDto** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminSetSchoolEnabledRequestDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminSetSchoolEnabledRequestDto.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
