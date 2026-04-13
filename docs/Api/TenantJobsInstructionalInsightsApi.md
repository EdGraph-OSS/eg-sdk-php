# EdGraph\PlatformClient\TenantJobsInstructionalInsightsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createInstructionalInsightsSecuritySyncJob()**](TenantJobsInstructionalInsightsApi.md#createInstructionalInsightsSecuritySyncJob) | **POST** /tenants/{tenantId}/jobs/instructionalinsights | Creates an Instructional Insights Security Sync Job for a given tenant |
| [**executeInstructionalInsightsSecuritySyncJob()**](TenantJobsInstructionalInsightsApi.md#executeInstructionalInsightsSecuritySyncJob) | **POST** /tenants/{tenantId}/jobs/instructionalinsights/execute | Executes an Instructional Insights Security Sync Job |
| [**getInstructionalInsightsSecuritySyncJob()**](TenantJobsInstructionalInsightsApi.md#getInstructionalInsightsSecuritySyncJob) | **GET** /tenants/{tenantId}/jobs/instructionalinsights | Retrieves an Instructional Insights Security Sync Job for a given tenant |
| [**searchInstructionalInsightsSecuritySyncJobExecutionLogs()**](TenantJobsInstructionalInsightsApi.md#searchInstructionalInsightsSecuritySyncJobExecutionLogs) | **GET** /tenants/{tenantId}/jobs/instructionalinsights/executions/{executionId}/logs | Searches Instructional Insights Security Sync Job Execution Logs for a given tenant and execution |
| [**searchInstructionalInsightsSecuritySyncJobExecutions()**](TenantJobsInstructionalInsightsApi.md#searchInstructionalInsightsSecuritySyncJobExecutions) | **GET** /tenants/{tenantId}/jobs/instructionalinsights/executions | Searches Instructional Insights Security Sync Job Executions for a given tenant |
| [**updateInstructionalInsightsSecuritySyncJob()**](TenantJobsInstructionalInsightsApi.md#updateInstructionalInsightsSecuritySyncJob) | **PUT** /tenants/{tenantId}/jobs/instructionalinsights | Updates an Instructional Insights Security Sync Job for a given tenant |


## `createInstructionalInsightsSecuritySyncJob()`

```php
createInstructionalInsightsSecuritySyncJob($tenantId, $identityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest): \EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobCreatedResponse
```

Creates an Instructional Insights Security Sync Job for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantJobsInstructionalInsightsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$identityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest = new \EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest(); // \EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest | 

try {
    $result = $apiInstance->createInstructionalInsightsSecuritySyncJob($tenantId, $identityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantJobsInstructionalInsightsApi->createInstructionalInsightsSecuritySyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **identityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest**](../Model/IdentityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobCreatedResponse**](../Model/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `executeInstructionalInsightsSecuritySyncJob()`

```php
executeInstructionalInsightsSecuritySyncJob($tenantId): \EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutedResponse
```

Executes an Instructional Insights Security Sync Job

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantJobsInstructionalInsightsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->executeInstructionalInsightsSecuritySyncJob($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantJobsInstructionalInsightsApi->executeInstructionalInsightsSecuritySyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutedResponse**](../Model/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInstructionalInsightsSecuritySyncJob()`

```php
getInstructionalInsightsSecuritySyncJob($tenantId): \EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobResponse
```

Retrieves an Instructional Insights Security Sync Job for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantJobsInstructionalInsightsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->getInstructionalInsightsSecuritySyncJob($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantJobsInstructionalInsightsApi->getInstructionalInsightsSecuritySyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobResponse**](../Model/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchInstructionalInsightsSecuritySyncJobExecutionLogs()`

```php
searchInstructionalInsightsSecuritySyncJobExecutionLogs($tenantId, $executionId, $jobId, $pageIndex, $pageSize, $orderBy, $level, $message): \EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionLogsResponse
```

Searches Instructional Insights Security Sync Job Execution Logs for a given tenant and execution

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantJobsInstructionalInsightsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$executionId = 'executionId_example'; // string | 
$jobId = ''; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$level = ''; // string | 
$message = ''; // string | 

try {
    $result = $apiInstance->searchInstructionalInsightsSecuritySyncJobExecutionLogs($tenantId, $executionId, $jobId, $pageIndex, $pageSize, $orderBy, $level, $message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantJobsInstructionalInsightsApi->searchInstructionalInsightsSecuritySyncJobExecutionLogs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **executionId** | **string**|  | |
| **jobId** | **string**|  | [optional] [default to &#39;&#39;] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **level** | **string**|  | [optional] [default to &#39;&#39;] |
| **message** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionLogsResponse**](../Model/IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionLogsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchInstructionalInsightsSecuritySyncJobExecutions()`

```php
searchInstructionalInsightsSecuritySyncJobExecutions($tenantId, $jobId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionsResponse
```

Searches Instructional Insights Security Sync Job Executions for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantJobsInstructionalInsightsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = ''; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->searchInstructionalInsightsSecuritySyncJobExecutions($tenantId, $jobId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantJobsInstructionalInsightsApi->searchInstructionalInsightsSecuritySyncJobExecutions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | [optional] [default to &#39;&#39;] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionsResponse**](../Model/IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateInstructionalInsightsSecuritySyncJob()`

```php
updateInstructionalInsightsSecuritySyncJob($tenantId, $identityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest): \EdGraph\PlatformClient\Model\MicrosoftAspNetCoreMvcNoContentResult
```

Updates an Instructional Insights Security Sync Job for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantJobsInstructionalInsightsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$identityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest = new \EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest(); // \EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest | 

try {
    $result = $apiInstance->updateInstructionalInsightsSecuritySyncJob($tenantId, $identityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantJobsInstructionalInsightsApi->updateInstructionalInsightsSecuritySyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **identityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest**](../Model/IdentityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\MicrosoftAspNetCoreMvcNoContentResult**](../Model/MicrosoftAspNetCoreMvcNoContentResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
