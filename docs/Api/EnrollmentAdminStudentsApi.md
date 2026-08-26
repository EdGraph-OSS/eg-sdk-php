# EdGraph\PlatformClient\EnrollmentAdminStudentsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getEnrollmentStudent()**](EnrollmentAdminStudentsApi.md#getEnrollmentStudent) | **GET** /tenants/{tenantId}/enrollmentadmin/students/{studentId} | Gets an Enrollment Student. |
| [**getEnrollmentStudents()**](EnrollmentAdminStudentsApi.md#getEnrollmentStudents) | **GET** /tenants/{tenantId}/enrollmentadmin/students | Searches Enrollment Students. |


## `getEnrollmentStudent()`

```php
getEnrollmentStudent($tenantId, $studentId): \EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentStudentsV1StudentResponse
```

Gets an Enrollment Student.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnrollmentAdminStudentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$studentId = 'studentId_example'; // string | 

try {
    $result = $apiInstance->getEnrollmentStudent($tenantId, $studentId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnrollmentAdminStudentsApi->getEnrollmentStudent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **studentId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentStudentsV1StudentResponse**](../Model/EnrollmentApiEnrollmentStudentsV1StudentResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEnrollmentStudents()`

```php
getEnrollmentStudents($tenantId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentStudentsV1StudentsSearchResponse
```

Searches Enrollment Students.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnrollmentAdminStudentsApi(
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
    $result = $apiInstance->getEnrollmentStudents($tenantId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnrollmentAdminStudentsApi->getEnrollmentStudents: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentStudentsV1StudentsSearchResponse**](../Model/EnrollmentApiEnrollmentStudentsV1StudentsSearchResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
