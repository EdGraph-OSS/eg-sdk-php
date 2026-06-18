# EdGraph\PlatformClient\EnvironmentsReportingPeriodsSubmissionsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addReportingPeriodSubmissionMetricsBulkV2()**](EnvironmentsReportingPeriodsSubmissionsApi.md#addReportingPeriodSubmissionMetricsBulkV2) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics/bulk | Adds Metrics to a Submission in bulk. |
| [**addReportingPeriodSubmissionMetricsV2()**](EnvironmentsReportingPeriodsSubmissionsApi.md#addReportingPeriodSubmissionMetricsV2) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Adds Metrics to a Submission. |
| [**cancelReportingPeriodSubmissionV2()**](EnvironmentsReportingPeriodsSubmissionsApi.md#cancelReportingPeriodSubmissionV2) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/cancel | Cancels a Submission. |
| [**getReportingPeriodSubmissionLatestV2()**](EnvironmentsReportingPeriodsSubmissionsApi.md#getReportingPeriodSubmissionLatestV2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/latest | Retrieves the latest Submission of a Reporting Period. |
| [**getReportingPeriodSubmissionLogsV2()**](EnvironmentsReportingPeriodsSubmissionsApi.md#getReportingPeriodSubmissionLogsV2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/logs | Retrieves a list of Submission Logs of a Reporting Period. |
| [**getReportingPeriodSubmissionMetricsV2()**](EnvironmentsReportingPeriodsSubmissionsApi.md#getReportingPeriodSubmissionMetricsV2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Retrieves the Metrics of a Submission. |
| [**getReportingPeriodSubmissionV2()**](EnvironmentsReportingPeriodsSubmissionsApi.md#getReportingPeriodSubmissionV2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId} | Retrieves the Submission of a Reporting Period. |
| [**getStateReportingPeriodSubmissionsV2()**](EnvironmentsReportingPeriodsSubmissionsApi.md#getStateReportingPeriodSubmissionsV2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions | Retrieves a list of Submissions of a Reporting Period. |
| [**setReportingPeriodSubmissionStatusV2()**](EnvironmentsReportingPeriodsSubmissionsApi.md#setReportingPeriodSubmissionStatusV2) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/status | Sets the Status of a Submission. |


## `addReportingPeriodSubmissionMetricsBulkV2()`

```php
addReportingPeriodSubmissionMetricsBulkV2($tenantId, $environmentId, $reportingPeriodId, $submissionId, $edGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionMetricsAddedBulkResponse
```

Adds Metrics to a Submission in bulk.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsSubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 
$edGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest | 

try {
    $result = $apiInstance->addReportingPeriodSubmissionMetricsBulkV2($tenantId, $environmentId, $reportingPeriodId, $submissionId, $edGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsSubmissionsApi->addReportingPeriodSubmissionMetricsBulkV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |
| **edGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest**](../Model/EdGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionMetricsAddedBulkResponse**](../Model/EdGraphServicesStateReportingV1SubmissionMetricsAddedBulkResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `addReportingPeriodSubmissionMetricsV2()`

```php
addReportingPeriodSubmissionMetricsV2($tenantId, $environmentId, $reportingPeriodId, $submissionId, $edGraphServicesStateReportingV1AddSubmissionMetricsRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionMetricsAddedResponse
```

Adds Metrics to a Submission.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsSubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 
$edGraphServicesStateReportingV1AddSubmissionMetricsRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1AddSubmissionMetricsRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1AddSubmissionMetricsRequest | 

try {
    $result = $apiInstance->addReportingPeriodSubmissionMetricsV2($tenantId, $environmentId, $reportingPeriodId, $submissionId, $edGraphServicesStateReportingV1AddSubmissionMetricsRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsSubmissionsApi->addReportingPeriodSubmissionMetricsV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |
| **edGraphServicesStateReportingV1AddSubmissionMetricsRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1AddSubmissionMetricsRequest**](../Model/EdGraphServicesStateReportingV1AddSubmissionMetricsRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionMetricsAddedResponse**](../Model/EdGraphServicesStateReportingV1SubmissionMetricsAddedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `cancelReportingPeriodSubmissionV2()`

```php
cancelReportingPeriodSubmissionV2($tenantId, $environmentId, $reportingPeriodId, $submissionId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionCancelledResponse
```

Cancels a Submission.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsSubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 

try {
    $result = $apiInstance->cancelReportingPeriodSubmissionV2($tenantId, $environmentId, $reportingPeriodId, $submissionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsSubmissionsApi->cancelReportingPeriodSubmissionV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionCancelledResponse**](../Model/EdGraphServicesStateReportingV1SubmissionCancelledResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodSubmissionLatestV2()`

```php
getReportingPeriodSubmissionLatestV2($tenantId, $environmentId, $reportingPeriodId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionProfile
```

Retrieves the latest Submission of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsSubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->getReportingPeriodSubmissionLatestV2($tenantId, $environmentId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsSubmissionsApi->getReportingPeriodSubmissionLatestV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionProfile**](../Model/EdGraphServicesStateReportingV1SubmissionProfile.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodSubmissionLogsV2()`

```php
getReportingPeriodSubmissionLogsV2($tenantId, $environmentId, $reportingPeriodId, $submissionId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedSubmissionLogs
```

Retrieves a list of Submission Logs of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsSubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 
$pageIndex = 56; // int | 
$pageSize = 56; // int | 
$filter = 'filter_example'; // string | 
$orderBy = 'orderBy_example'; // string | 

try {
    $result = $apiInstance->getReportingPeriodSubmissionLogsV2($tenantId, $environmentId, $reportingPeriodId, $submissionId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsSubmissionsApi->getReportingPeriodSubmissionLogsV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] |
| **pageSize** | **int**|  | [optional] |
| **filter** | **string**|  | [optional] |
| **orderBy** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedSubmissionLogs**](../Model/EdGraphServicesStateReportingV1PaginatedSubmissionLogs.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodSubmissionMetricsV2()`

```php
getReportingPeriodSubmissionMetricsV2($tenantId, $environmentId, $reportingPeriodId, $submissionId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionMetricsResponse
```

Retrieves the Metrics of a Submission.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsSubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 

try {
    $result = $apiInstance->getReportingPeriodSubmissionMetricsV2($tenantId, $environmentId, $reportingPeriodId, $submissionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsSubmissionsApi->getReportingPeriodSubmissionMetricsV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionMetricsResponse**](../Model/EdGraphServicesStateReportingV1SubmissionMetricsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodSubmissionV2()`

```php
getReportingPeriodSubmissionV2($tenantId, $environmentId, $reportingPeriodId, $submissionId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionProfile
```

Retrieves the Submission of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsSubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 

try {
    $result = $apiInstance->getReportingPeriodSubmissionV2($tenantId, $environmentId, $reportingPeriodId, $submissionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsSubmissionsApi->getReportingPeriodSubmissionV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionProfile**](../Model/EdGraphServicesStateReportingV1SubmissionProfile.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStateReportingPeriodSubmissionsV2()`

```php
getStateReportingPeriodSubmissionsV2($tenantId, $environmentId, $reportingPeriodId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedSubmissions
```

Retrieves a list of Submissions of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsSubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$filter = ''; // string | 
$orderBy = ''; // string | 

try {
    $result = $apiInstance->getStateReportingPeriodSubmissionsV2($tenantId, $environmentId, $reportingPeriodId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsSubmissionsApi->getStateReportingPeriodSubmissionsV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedSubmissions**](../Model/EdGraphServicesStateReportingV1PaginatedSubmissions.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setReportingPeriodSubmissionStatusV2()`

```php
setReportingPeriodSubmissionStatusV2($tenantId, $environmentId, $reportingPeriodId, $submissionId, $edGraphServicesStateReportingV1SetSubmissionStatusRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionStatusSetResponse
```

Sets the Status of a Submission.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsSubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 
$edGraphServicesStateReportingV1SetSubmissionStatusRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetSubmissionStatusRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetSubmissionStatusRequest | 

try {
    $result = $apiInstance->setReportingPeriodSubmissionStatusV2($tenantId, $environmentId, $reportingPeriodId, $submissionId, $edGraphServicesStateReportingV1SetSubmissionStatusRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsSubmissionsApi->setReportingPeriodSubmissionStatusV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |
| **edGraphServicesStateReportingV1SetSubmissionStatusRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetSubmissionStatusRequest**](../Model/EdGraphServicesStateReportingV1SetSubmissionStatusRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SubmissionStatusSetResponse**](../Model/EdGraphServicesStateReportingV1SubmissionStatusSetResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
