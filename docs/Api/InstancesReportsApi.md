# EdGraph\PlatformClient\InstancesReportsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**generateReportsAsync()**](InstancesReportsApi.md#generateReportsAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/generate | Queues a job to generate the report views in the ODS Database. |
| [**getReportsStatusAsync()**](InstancesReportsApi.md#getReportsStatusAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/status | Retrieves the status of the report views in Instance. |
| [**getSchoolsByTypeReportAsync()**](InstancesReportsApi.md#getSchoolsByTypeReportAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/schoolsbytype/{localEducationAgencyId} | Retrieves a \&quot;Schools By Type\&quot; report. |
| [**getStudentEconomicSituationReportAsync()**](InstancesReportsApi.md#getStudentEconomicSituationReportAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentseconomicsituation/{localEducationAgencyId} | Retrieves a \&quot;Students Economic Situation\&quot; report. |
| [**getStudentEnrollmentByEthnicityReport()**](InstancesReportsApi.md#getStudentEnrollmentByEthnicityReport) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentenrollment/ethnicity/{localEducationAgencyId} | Retrieves a \&quot;Student Enrollment By Ethnicity\&quot; report. |
| [**getStudentEnrollmentByGenderReportAsync()**](InstancesReportsApi.md#getStudentEnrollmentByGenderReportAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentenrollment/gender/{localEducationAgencyId} | Retrieves a \&quot;Student Enrollment By Gender\&quot; report. |
| [**getStudentEnrollmentByRaceReportAsync()**](InstancesReportsApi.md#getStudentEnrollmentByRaceReportAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentenrollment/race/{localEducationAgencyId} | Retrieves a \&quot;Student Enrollment By Race\&quot; report. |
| [**getStudentsByProgramReportAsync()**](InstancesReportsApi.md#getStudentsByProgramReportAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentsbyprogram/{localEducationAgencyId} | Retrieves a \&quot;Students By Program\&quot; report. |
| [**getTotalEnrollmentsReportAsync()**](InstancesReportsApi.md#getTotalEnrollmentsReportAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/totalenrollments/{localEducationAgencyId} | Retrieves a \&quot;Total Enrollments\&quot; report. |


## `generateReportsAsync()`

```php
generateReportsAsync($tenantId, $instanceId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1GenerateReportsResponse
```

Queues a job to generate the report views in the ODS Database.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->generateReportsAsync($tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesReportsApi->generateReportsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1GenerateReportsResponse**](../Model/EdfiAdminApiEdfiAdminV1GenerateReportsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportsStatusAsync()`

```php
getReportsStatusAsync($tenantId, $instanceId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ReportsStatusResponse
```

Retrieves the status of the report views in Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->getReportsStatusAsync($tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesReportsApi->getReportsStatusAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ReportsStatusResponse**](../Model/EdfiAdminApiEdfiAdminV1ReportsStatusResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSchoolsByTypeReportAsync()`

```php
getSchoolsByTypeReportAsync($tenantId, $instanceId, $localEducationAgencyId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SchoolsByTypeReportResponse
```

Retrieves a \"Schools By Type\" report.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$localEducationAgencyId = 56; // int | 

try {
    $result = $apiInstance->getSchoolsByTypeReportAsync($tenantId, $instanceId, $localEducationAgencyId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesReportsApi->getSchoolsByTypeReportAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **localEducationAgencyId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SchoolsByTypeReportResponse**](../Model/EdfiAdminApiEdfiAdminV1SchoolsByTypeReportResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStudentEconomicSituationReportAsync()`

```php
getStudentEconomicSituationReportAsync($tenantId, $instanceId, $localEducationAgencyId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StudentEconomicSituationReportResponse
```

Retrieves a \"Students Economic Situation\" report.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$localEducationAgencyId = 56; // int | 

try {
    $result = $apiInstance->getStudentEconomicSituationReportAsync($tenantId, $instanceId, $localEducationAgencyId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesReportsApi->getStudentEconomicSituationReportAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **localEducationAgencyId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StudentEconomicSituationReportResponse**](../Model/EdfiAdminApiEdfiAdminV1StudentEconomicSituationReportResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStudentEnrollmentByEthnicityReport()`

```php
getStudentEnrollmentByEthnicityReport($tenantId, $instanceId, $localEducationAgencyId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StudentEnrollmentByEthnicityReportResponse
```

Retrieves a \"Student Enrollment By Ethnicity\" report.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$localEducationAgencyId = 56; // int | 

try {
    $result = $apiInstance->getStudentEnrollmentByEthnicityReport($tenantId, $instanceId, $localEducationAgencyId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesReportsApi->getStudentEnrollmentByEthnicityReport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **localEducationAgencyId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StudentEnrollmentByEthnicityReportResponse**](../Model/EdfiAdminApiEdfiAdminV1StudentEnrollmentByEthnicityReportResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStudentEnrollmentByGenderReportAsync()`

```php
getStudentEnrollmentByGenderReportAsync($tenantId, $instanceId, $localEducationAgencyId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StudentEnrollmentByGenderReportResponse
```

Retrieves a \"Student Enrollment By Gender\" report.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$localEducationAgencyId = 56; // int | 

try {
    $result = $apiInstance->getStudentEnrollmentByGenderReportAsync($tenantId, $instanceId, $localEducationAgencyId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesReportsApi->getStudentEnrollmentByGenderReportAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **localEducationAgencyId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StudentEnrollmentByGenderReportResponse**](../Model/EdfiAdminApiEdfiAdminV1StudentEnrollmentByGenderReportResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStudentEnrollmentByRaceReportAsync()`

```php
getStudentEnrollmentByRaceReportAsync($tenantId, $instanceId, $localEducationAgencyId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StudentEnrollmentByRaceReportResponse
```

Retrieves a \"Student Enrollment By Race\" report.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$localEducationAgencyId = 56; // int | 

try {
    $result = $apiInstance->getStudentEnrollmentByRaceReportAsync($tenantId, $instanceId, $localEducationAgencyId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesReportsApi->getStudentEnrollmentByRaceReportAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **localEducationAgencyId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StudentEnrollmentByRaceReportResponse**](../Model/EdfiAdminApiEdfiAdminV1StudentEnrollmentByRaceReportResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStudentsByProgramReportAsync()`

```php
getStudentsByProgramReportAsync($tenantId, $instanceId, $localEducationAgencyId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StudentsByProgramReportResponse
```

Retrieves a \"Students By Program\" report.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$localEducationAgencyId = 56; // int | 

try {
    $result = $apiInstance->getStudentsByProgramReportAsync($tenantId, $instanceId, $localEducationAgencyId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesReportsApi->getStudentsByProgramReportAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **localEducationAgencyId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StudentsByProgramReportResponse**](../Model/EdfiAdminApiEdfiAdminV1StudentsByProgramReportResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTotalEnrollmentsReportAsync()`

```php
getTotalEnrollmentsReportAsync($tenantId, $instanceId, $localEducationAgencyId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1TotalEnrollmentsReportResponse
```

Retrieves a \"Total Enrollments\" report.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$localEducationAgencyId = 56; // int | 

try {
    $result = $apiInstance->getTotalEnrollmentsReportAsync($tenantId, $instanceId, $localEducationAgencyId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesReportsApi->getTotalEnrollmentsReportAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **localEducationAgencyId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1TotalEnrollmentsReportResponse**](../Model/EdfiAdminApiEdfiAdminV1TotalEnrollmentsReportResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
