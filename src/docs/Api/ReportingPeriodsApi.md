# EdGraph\PlatformClient\ReportingPeriodsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addReportingPeriodSubmissionMetrics()**](ReportingPeriodsApi.md#addReportingPeriodSubmissionMetrics) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Adds Metrics to a Submission. |
| [**addReportingPeriodSubmissionMetricsBulk()**](ReportingPeriodsApi.md#addReportingPeriodSubmissionMetricsBulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics/bulk | Adds Metrics to a Submission in bulk. |
| [**cancelReportingPeriodSubmission()**](ReportingPeriodsApi.md#cancelReportingPeriodSubmission) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/cancel | Cancels a Submission. |
| [**closeReportingPeriodAsync()**](ReportingPeriodsApi.md#closeReportingPeriodAsync) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/close | Closes the state of a Reporting Period. |
| [**deleteReportingPeriodRules()**](ReportingPeriodsApi.md#deleteReportingPeriodRules) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/rules | Delete the Reporting Period and Associated Rules |
| [**getReportingPeriodCertificationStatus()**](ReportingPeriodsApi.md#getReportingPeriodCertificationStatus) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/certificationstatus | Retrieves the Certification Status of a Reporting Period. |
| [**getReportingPeriodRecords()**](ReportingPeriodsApi.md#getReportingPeriodRecords) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/records | Retrieves the Invalid Records of all the Rules within a Reporting Period. |
| [**getReportingPeriodRuleRecords()**](ReportingPeriodsApi.md#getReportingPeriodRuleRecords) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records | Retrieves the Invalid Records of a Rule. |
| [**getReportingPeriodSubmission()**](ReportingPeriodsApi.md#getReportingPeriodSubmission) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId} | Retrieves the Submission of a Reporting Period. |
| [**getReportingPeriodSubmissionLatest()**](ReportingPeriodsApi.md#getReportingPeriodSubmissionLatest) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/latest | Retrieves the latest Submission of a Reporting Period. |
| [**getReportingPeriodSubmissionLogs()**](ReportingPeriodsApi.md#getReportingPeriodSubmissionLogs) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/logs | Retrieves a list of Submission Logs of a Reporting Period. |
| [**getReportingPeriodSubmissionMetrics()**](ReportingPeriodsApi.md#getReportingPeriodSubmissionMetrics) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Retrieves the Metrics of a Submission. |
| [**getReportingPeriodSubmissions()**](ReportingPeriodsApi.md#getReportingPeriodSubmissions) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions | Retrieves a list of Submissions of a Reporting Period. |
| [**getReportingPeriodValidationSummary()**](ReportingPeriodsApi.md#getReportingPeriodValidationSummary) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/validationsummary | Retrieves the Validation Summary of a Reporting Period. |
| [**getReportingPeriodValidationSummaryByCategoryId()**](ReportingPeriodsApi.md#getReportingPeriodValidationSummaryByCategoryId) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/validationsummary/categories/{categoryId} | Retrieves the Validation Summary of a Reporting Period for a Category. |
| [**getReportingPeriods()**](ReportingPeriodsApi.md#getReportingPeriods) | **GET** /tenants/{tenantId}/statereporting/reportingperiods | Retrieves a list of Reporting Periods. |
| [**postReportingPeriod()**](ReportingPeriodsApi.md#postReportingPeriod) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/post | Post a Reporting Period. |
| [**runReportingPeriodValidations()**](ReportingPeriodsApi.md#runReportingPeriodValidations) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/run | Run Reporting Period Validations. |
| [**setReportingPeriodRuleRecordExcludeFromPostFlagBulk()**](ReportingPeriodsApi.md#setReportingPeriodRuleRecordExcludeFromPostFlagBulk) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records/excludefrompost | Toggles the \&quot;ExcludeFromPost\&quot; flag of a Rule&#39;s Invalid Records. |
| [**setReportingPeriodSubmissionStatus()**](ReportingPeriodsApi.md#setReportingPeriodSubmissionStatus) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/status | Sets the Status of a Submission. |
| [**toggleReportingPeriodSelection()**](ReportingPeriodsApi.md#toggleReportingPeriodSelection) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/toggle | Toggles the Selected state of a Reporting Period. |
| [**updateReportingPeriodBulk()**](ReportingPeriodsApi.md#updateReportingPeriodBulk) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods | Updates Reporting Periods in bulk. |


## `addReportingPeriodSubmissionMetrics()`

```php
addReportingPeriodSubmissionMetrics($tenantId, $reportingPeriodId, $submissionId, $validationsApiReportingPeriodsV1AddSubmissionMetricsRequest): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionMetricsAddedResponse
```

Adds Metrics to a Submission.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 
$validationsApiReportingPeriodsV1AddSubmissionMetricsRequest = new \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1AddSubmissionMetricsRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1AddSubmissionMetricsRequest | 

try {
    $result = $apiInstance->addReportingPeriodSubmissionMetrics($tenantId, $reportingPeriodId, $submissionId, $validationsApiReportingPeriodsV1AddSubmissionMetricsRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->addReportingPeriodSubmissionMetrics: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |
| **validationsApiReportingPeriodsV1AddSubmissionMetricsRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1AddSubmissionMetricsRequest**](../Model/ValidationsApiReportingPeriodsV1AddSubmissionMetricsRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionMetricsAddedResponse**](../Model/ValidationsApiReportingPeriodsV1SubmissionMetricsAddedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `addReportingPeriodSubmissionMetricsBulk()`

```php
addReportingPeriodSubmissionMetricsBulk($tenantId, $reportingPeriodId, $submissionId, $validationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionMetricsAddedBulkResponse
```

Adds Metrics to a Submission in bulk.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 
$validationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest = new \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest | 

try {
    $result = $apiInstance->addReportingPeriodSubmissionMetricsBulk($tenantId, $reportingPeriodId, $submissionId, $validationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->addReportingPeriodSubmissionMetricsBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |
| **validationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest**](../Model/ValidationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionMetricsAddedBulkResponse**](../Model/ValidationsApiReportingPeriodsV1SubmissionMetricsAddedBulkResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `cancelReportingPeriodSubmission()`

```php
cancelReportingPeriodSubmission($tenantId, $reportingPeriodId, $submissionId): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionCancelledResponse
```

Cancels a Submission.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 

try {
    $result = $apiInstance->cancelReportingPeriodSubmission($tenantId, $reportingPeriodId, $submissionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->cancelReportingPeriodSubmission: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionCancelledResponse**](../Model/ValidationsApiReportingPeriodsV1SubmissionCancelledResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `closeReportingPeriodAsync()`

```php
closeReportingPeriodAsync($tenantId, $reportingPeriodId): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1CloseReportingPeriodResponse
```

Closes the state of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->closeReportingPeriodAsync($tenantId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->closeReportingPeriodAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1CloseReportingPeriodResponse**](../Model/ValidationsApiReportingPeriodsV1CloseReportingPeriodResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteReportingPeriodRules()`

```php
deleteReportingPeriodRules($tenantId, $reportingPeriodId): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1DeleteReportingPeriodRulesResponse
```

Delete the Reporting Period and Associated Rules

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->deleteReportingPeriodRules($tenantId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->deleteReportingPeriodRules: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1DeleteReportingPeriodRulesResponse**](../Model/ValidationsApiReportingPeriodsV1DeleteReportingPeriodRulesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodCertificationStatus()`

```php
getReportingPeriodCertificationStatus($tenantId, $reportingPeriodId): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1CertificationStatus
```

Retrieves the Certification Status of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->getReportingPeriodCertificationStatus($tenantId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->getReportingPeriodCertificationStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1CertificationStatus**](../Model/ValidationsApiReportingPeriodsV1CertificationStatus.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodRecords()`

```php
getReportingPeriodRecords($tenantId, $reportingPeriodId, $pageIndex, $pageSize, $excludedFromPost): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PaginatedRecords
```

Retrieves the Invalid Records of all the Rules within a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$excludedFromPost = True; // bool | 

try {
    $result = $apiInstance->getReportingPeriodRecords($tenantId, $reportingPeriodId, $pageIndex, $pageSize, $excludedFromPost);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->getReportingPeriodRecords: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **excludedFromPost** | **bool**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PaginatedRecords**](../Model/ValidationsApiReportingPeriodsV1PaginatedRecords.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodRuleRecords()`

```php
getReportingPeriodRuleRecords($tenantId, $reportingPeriodId, $ruleId, $pageIndex, $pageSize): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PaginatedRuleRecordsV2
```

Retrieves the Invalid Records of a Rule.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$ruleId = 'ruleId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 

try {
    $result = $apiInstance->getReportingPeriodRuleRecords($tenantId, $reportingPeriodId, $ruleId, $pageIndex, $pageSize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->getReportingPeriodRuleRecords: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **ruleId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PaginatedRuleRecordsV2**](../Model/ValidationsApiReportingPeriodsV1PaginatedRuleRecordsV2.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodSubmission()`

```php
getReportingPeriodSubmission($tenantId, $reportingPeriodId, $submissionId): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionProfile
```

Retrieves the Submission of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 

try {
    $result = $apiInstance->getReportingPeriodSubmission($tenantId, $reportingPeriodId, $submissionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->getReportingPeriodSubmission: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionProfile**](../Model/ValidationsApiReportingPeriodsV1SubmissionProfile.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodSubmissionLatest()`

```php
getReportingPeriodSubmissionLatest($tenantId, $reportingPeriodId): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionProfile
```

Retrieves the latest Submission of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->getReportingPeriodSubmissionLatest($tenantId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->getReportingPeriodSubmissionLatest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionProfile**](../Model/ValidationsApiReportingPeriodsV1SubmissionProfile.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodSubmissionLogs()`

```php
getReportingPeriodSubmissionLogs($tenantId, $reportingPeriodId, $submissionId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PaginatedSubmissions
```

Retrieves a list of Submission Logs of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$filter = ''; // string | 
$orderBy = ''; // string | 

try {
    $result = $apiInstance->getReportingPeriodSubmissionLogs($tenantId, $reportingPeriodId, $submissionId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->getReportingPeriodSubmissionLogs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PaginatedSubmissions**](../Model/ValidationsApiReportingPeriodsV1PaginatedSubmissions.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodSubmissionMetrics()`

```php
getReportingPeriodSubmissionMetrics($tenantId, $reportingPeriodId, $submissionId): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionMetricsResponse
```

Retrieves the Metrics of a Submission.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 

try {
    $result = $apiInstance->getReportingPeriodSubmissionMetrics($tenantId, $reportingPeriodId, $submissionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->getReportingPeriodSubmissionMetrics: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionMetricsResponse**](../Model/ValidationsApiReportingPeriodsV1SubmissionMetricsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodSubmissions()`

```php
getReportingPeriodSubmissions($tenantId, $reportingPeriodId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PaginatedSubmissions
```

Retrieves a list of Submissions of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$filter = ''; // string | 
$orderBy = ''; // string | 

try {
    $result = $apiInstance->getReportingPeriodSubmissions($tenantId, $reportingPeriodId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->getReportingPeriodSubmissions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PaginatedSubmissions**](../Model/ValidationsApiReportingPeriodsV1PaginatedSubmissions.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodValidationSummary()`

```php
getReportingPeriodValidationSummary($tenantId, $reportingPeriodId): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1ValidationSummary
```

Retrieves the Validation Summary of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->getReportingPeriodValidationSummary($tenantId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->getReportingPeriodValidationSummary: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1ValidationSummary**](../Model/ValidationsApiReportingPeriodsV1ValidationSummary.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriodValidationSummaryByCategoryId()`

```php
getReportingPeriodValidationSummaryByCategoryId($tenantId, $reportingPeriodId, $categoryId): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1ValidationSummaryByCategoryId
```

Retrieves the Validation Summary of a Reporting Period for a Category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$categoryId = 'categoryId_example'; // string | 

try {
    $result = $apiInstance->getReportingPeriodValidationSummaryByCategoryId($tenantId, $reportingPeriodId, $categoryId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->getReportingPeriodValidationSummaryByCategoryId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **categoryId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1ValidationSummaryByCategoryId**](../Model/ValidationsApiReportingPeriodsV1ValidationSummaryByCategoryId.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportingPeriods()`

```php
getReportingPeriods($tenantId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PaginatedReportingPeriods
```

Retrieves a list of Reporting Periods.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$filter = ''; // string | 
$orderBy = ''; // string | 

try {
    $result = $apiInstance->getReportingPeriods($tenantId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->getReportingPeriods: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PaginatedReportingPeriods**](../Model/ValidationsApiReportingPeriodsV1PaginatedReportingPeriods.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postReportingPeriod()`

```php
postReportingPeriod($tenantId, $reportingPeriodId, $validationsApiReportingPeriodsV1PostRequest): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PostedResponse
```

Post a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$validationsApiReportingPeriodsV1PostRequest = new \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PostRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PostRequest | 

try {
    $result = $apiInstance->postReportingPeriod($tenantId, $reportingPeriodId, $validationsApiReportingPeriodsV1PostRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->postReportingPeriod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **validationsApiReportingPeriodsV1PostRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PostRequest**](../Model/ValidationsApiReportingPeriodsV1PostRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1PostedResponse**](../Model/ValidationsApiReportingPeriodsV1PostedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `runReportingPeriodValidations()`

```php
runReportingPeriodValidations($tenantId, $reportingPeriodId, $categoryId): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1RunResponse
```

Run Reporting Period Validations.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$categoryId = 'categoryId_example'; // string | 

try {
    $result = $apiInstance->runReportingPeriodValidations($tenantId, $reportingPeriodId, $categoryId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->runReportingPeriodValidations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **categoryId** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1RunResponse**](../Model/ValidationsApiReportingPeriodsV1RunResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setReportingPeriodRuleRecordExcludeFromPostFlagBulk()`

```php
setReportingPeriodRuleRecordExcludeFromPostFlagBulk($tenantId, $reportingPeriodId, $ruleId, $validationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1RuleRecordPostFlagSetBulkResponse
```

Toggles the \"ExcludeFromPost\" flag of a Rule's Invalid Records.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$ruleId = 'ruleId_example'; // string | 
$validationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest = new \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest | 

try {
    $result = $apiInstance->setReportingPeriodRuleRecordExcludeFromPostFlagBulk($tenantId, $reportingPeriodId, $ruleId, $validationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->setReportingPeriodRuleRecordExcludeFromPostFlagBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **ruleId** | **string**|  | |
| **validationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest**](../Model/ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1RuleRecordPostFlagSetBulkResponse**](../Model/ValidationsApiReportingPeriodsV1RuleRecordPostFlagSetBulkResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setReportingPeriodSubmissionStatus()`

```php
setReportingPeriodSubmissionStatus($tenantId, $reportingPeriodId, $submissionId, $validationsApiReportingPeriodsV1SetSubmissionStatusRequest): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionStatusSetResponse
```

Sets the Status of a Submission.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 
$validationsApiReportingPeriodsV1SetSubmissionStatusRequest = new \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SetSubmissionStatusRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SetSubmissionStatusRequest | 

try {
    $result = $apiInstance->setReportingPeriodSubmissionStatus($tenantId, $reportingPeriodId, $submissionId, $validationsApiReportingPeriodsV1SetSubmissionStatusRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->setReportingPeriodSubmissionStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **submissionId** | **string**|  | |
| **validationsApiReportingPeriodsV1SetSubmissionStatusRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SetSubmissionStatusRequest**](../Model/ValidationsApiReportingPeriodsV1SetSubmissionStatusRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1SubmissionStatusSetResponse**](../Model/ValidationsApiReportingPeriodsV1SubmissionStatusSetResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `toggleReportingPeriodSelection()`

```php
toggleReportingPeriodSelection($tenantId, $reportingPeriodId, $validationsApiReportingPeriodsV1ToggleSelectedRequest): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1ToggledResponse
```

Toggles the Selected state of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$validationsApiReportingPeriodsV1ToggleSelectedRequest = new \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1ToggleSelectedRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1ToggleSelectedRequest | 

try {
    $result = $apiInstance->toggleReportingPeriodSelection($tenantId, $reportingPeriodId, $validationsApiReportingPeriodsV1ToggleSelectedRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->toggleReportingPeriodSelection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **validationsApiReportingPeriodsV1ToggleSelectedRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1ToggleSelectedRequest**](../Model/ValidationsApiReportingPeriodsV1ToggleSelectedRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1ToggledResponse**](../Model/ValidationsApiReportingPeriodsV1ToggledResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateReportingPeriodBulk()`

```php
updateReportingPeriodBulk($tenantId, $validationsApiReportingPeriodsV1UpdateBulkRequest): \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1UpdatedBulkResponse
```

Updates Reporting Periods in bulk.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$validationsApiReportingPeriodsV1UpdateBulkRequest = new \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1UpdateBulkRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1UpdateBulkRequest | 

try {
    $result = $apiInstance->updateReportingPeriodBulk($tenantId, $validationsApiReportingPeriodsV1UpdateBulkRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportingPeriodsApi->updateReportingPeriodBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **validationsApiReportingPeriodsV1UpdateBulkRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1UpdateBulkRequest**](../Model/ValidationsApiReportingPeriodsV1UpdateBulkRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiReportingPeriodsV1UpdatedBulkResponse**](../Model/ValidationsApiReportingPeriodsV1UpdatedBulkResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
