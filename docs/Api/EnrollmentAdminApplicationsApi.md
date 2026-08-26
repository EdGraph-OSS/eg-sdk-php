# EdGraph\PlatformClient\EnrollmentAdminApplicationsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getEnrollmentApplication()**](EnrollmentAdminApplicationsApi.md#getEnrollmentApplication) | **GET** /tenants/{tenantId}/enrollmentadmin/applications/{applicationId} | Gets an Enrollment Application. |
| [**getEnrollmentApplications()**](EnrollmentAdminApplicationsApi.md#getEnrollmentApplications) | **GET** /tenants/{tenantId}/enrollmentadmin/applications | Searches Enrollment Applications. |


## `getEnrollmentApplication()`

```php
getEnrollmentApplication($tenantId, $applicationId): \EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse
```

Gets an Enrollment Application.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnrollmentAdminApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 

try {
    $result = $apiInstance->getEnrollmentApplication($tenantId, $applicationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnrollmentAdminApplicationsApi->getEnrollmentApplication: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **applicationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse**](../Model/EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEnrollmentApplications()`

```php
getEnrollmentApplications($tenantId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponsesSearchResponse
```

Searches Enrollment Applications.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnrollmentAdminApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 56; // int | 
$pageSize = 56; // int | 
$filter = 'filter_example'; // string | 
$orderBy = 'orderBy_example'; // string | 

try {
    $result = $apiInstance->getEnrollmentApplications($tenantId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnrollmentAdminApplicationsApi->getEnrollmentApplications: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] |
| **pageSize** | **int**|  | [optional] |
| **filter** | **string**|  | [optional] |
| **orderBy** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponsesSearchResponse**](../Model/EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponsesSearchResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
