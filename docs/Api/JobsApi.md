# EdGraph\PlatformClient\JobsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**activateTenantDataSyncJob()**](JobsApi.md#activateTenantDataSyncJob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/activate | Activate a DataSync job matching the primary key |
| [**cancelJob()**](JobsApi.md#cancelJob) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/cancel | Requests a Job cancellation. |
| [**cancelTenantDataSyncJob()**](JobsApi.md#cancelTenantDataSyncJob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/cancel | Cancel a DataSync job matching the primary key |
| [**createJob()**](JobsApi.md#createJob) | **POST** /tenants/{tenantId}/validations/jobs | Creates a Job. |
| [**createTenantDataSyncJob()**](JobsApi.md#createTenantDataSyncJob) | **POST** /tenants/{tenantId}/datasync/jobs | Creates a new DataSync job |
| [**deactivateTenantDataSyncJob()**](JobsApi.md#deactivateTenantDataSyncJob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/deactivate | Deactivate a DataSync job matching the primary key |
| [**deleteJob()**](JobsApi.md#deleteJob) | **DELETE** /tenants/{tenantId}/validations/jobs/{jobId} | Deletes a Job. |
| [**deleteTenantDataSyncJob()**](JobsApi.md#deleteTenantDataSyncJob) | **DELETE** /tenants/{tenantId}/datasync/jobs/{jobId} | Delete a DataSync job matching the primary key |
| [**executeJob()**](JobsApi.md#executeJob) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/execute | Requests a Job execution. |
| [**executeTenantDataSyncJob()**](JobsApi.md#executeTenantDataSyncJob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/execute | Execute a DataSync job matching the primary key |
| [**getAllTenantDataSyncJobs()**](JobsApi.md#getAllTenantDataSyncJobs) | **GET** /tenants/{tenantId}/datasync/jobs | Retrieves a list of DataSync Jobs |
| [**getJobById()**](JobsApi.md#getJobById) | **GET** /tenants/{tenantId}/validations/jobs/{jobId} | Retrieves a Job by ID. |
| [**getJobs()**](JobsApi.md#getJobs) | **GET** /tenants/{tenantId}/validations/jobs | Retrieves a list of Jobs. |
| [**getTenantDataSyncJobProfileById()**](JobsApi.md#getTenantDataSyncJobProfileById) | **GET** /tenants/{tenantId}/datasync/jobs/{jobId} | Retrieves a specific DataSync job using its primary key |
| [**restartJobSchedule()**](JobsApi.md#restartJobSchedule) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/restart | Requests a Job schedule restart. |
| [**updateJob()**](JobsApi.md#updateJob) | **PUT** /tenants/{tenantId}/validations/jobs/{jobId} | Updates a Job. |
| [**updateTenantDataSyncJob()**](JobsApi.md#updateTenantDataSyncJob) | **PUT** /tenants/{tenantId}/datasync/jobs/{jobId} | Updates a DataSync job matching the primary key |


## `activateTenantDataSyncJob()`

```php
activateTenantDataSyncJob($tenantId, $jobId, $dataSyncApiJobV1ActivateJobRequest)
```

Activate a DataSync job matching the primary key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$dataSyncApiJobV1ActivateJobRequest = new \EdGraph\PlatformClient\Model\DataSyncApiJobV1ActivateJobRequest(); // \EdGraph\PlatformClient\Model\DataSyncApiJobV1ActivateJobRequest | 

try {
    $apiInstance->activateTenantDataSyncJob($tenantId, $jobId, $dataSyncApiJobV1ActivateJobRequest);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->activateTenantDataSyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **dataSyncApiJobV1ActivateJobRequest** | [**\EdGraph\PlatformClient\Model\DataSyncApiJobV1ActivateJobRequest**](../Model/DataSyncApiJobV1ActivateJobRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `cancelJob()`

```php
cancelJob($tenantId, $jobId): object
```

Requests a Job cancellation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 

try {
    $result = $apiInstance->cancelJob($tenantId, $jobId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->cancelJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `cancelTenantDataSyncJob()`

```php
cancelTenantDataSyncJob($tenantId, $jobId, $dataSyncApiJobV1CancelJobRequest)
```

Cancel a DataSync job matching the primary key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$dataSyncApiJobV1CancelJobRequest = new \EdGraph\PlatformClient\Model\DataSyncApiJobV1CancelJobRequest(); // \EdGraph\PlatformClient\Model\DataSyncApiJobV1CancelJobRequest | 

try {
    $apiInstance->cancelTenantDataSyncJob($tenantId, $jobId, $dataSyncApiJobV1CancelJobRequest);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->cancelTenantDataSyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **dataSyncApiJobV1CancelJobRequest** | [**\EdGraph\PlatformClient\Model\DataSyncApiJobV1CancelJobRequest**](../Model/DataSyncApiJobV1CancelJobRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createJob()`

```php
createJob($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest): \EdGraph\PlatformClient\Model\ValidationsApiCoreV1CreatedResponse
```

Creates a Job.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest | 

try {
    $result = $apiInstance->createJob($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->createJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiCoreV1CreatedResponse**](../Model/ValidationsApiCoreV1CreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createTenantDataSyncJob()`

```php
createTenantDataSyncJob($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest)
```

Creates a new DataSync job

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest | 

try {
    $apiInstance->createTenantDataSyncJob($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->createTenantDataSyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deactivateTenantDataSyncJob()`

```php
deactivateTenantDataSyncJob($tenantId, $jobId, $dataSyncApiJobV1DeactivateJobRequest)
```

Deactivate a DataSync job matching the primary key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$dataSyncApiJobV1DeactivateJobRequest = new \EdGraph\PlatformClient\Model\DataSyncApiJobV1DeactivateJobRequest(); // \EdGraph\PlatformClient\Model\DataSyncApiJobV1DeactivateJobRequest | 

try {
    $apiInstance->deactivateTenantDataSyncJob($tenantId, $jobId, $dataSyncApiJobV1DeactivateJobRequest);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->deactivateTenantDataSyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **dataSyncApiJobV1DeactivateJobRequest** | [**\EdGraph\PlatformClient\Model\DataSyncApiJobV1DeactivateJobRequest**](../Model/DataSyncApiJobV1DeactivateJobRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteJob()`

```php
deleteJob($tenantId, $jobId)
```

Deletes a Job.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 

try {
    $apiInstance->deleteJob($tenantId, $jobId);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->deleteJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteTenantDataSyncJob()`

```php
deleteTenantDataSyncJob($tenantId, $jobId)
```

Delete a DataSync job matching the primary key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 

try {
    $apiInstance->deleteTenantDataSyncJob($tenantId, $jobId);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->deleteTenantDataSyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `executeJob()`

```php
executeJob($tenantId, $jobId): object
```

Requests a Job execution.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 

try {
    $result = $apiInstance->executeJob($tenantId, $jobId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->executeJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `executeTenantDataSyncJob()`

```php
executeTenantDataSyncJob($tenantId, $jobId, $dataSyncApiJobV1ExecuteJobRequest)
```

Execute a DataSync job matching the primary key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$dataSyncApiJobV1ExecuteJobRequest = new \EdGraph\PlatformClient\Model\DataSyncApiJobV1ExecuteJobRequest(); // \EdGraph\PlatformClient\Model\DataSyncApiJobV1ExecuteJobRequest | 

try {
    $apiInstance->executeTenantDataSyncJob($tenantId, $jobId, $dataSyncApiJobV1ExecuteJobRequest);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->executeTenantDataSyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **dataSyncApiJobV1ExecuteJobRequest** | [**\EdGraph\PlatformClient\Model\DataSyncApiJobV1ExecuteJobRequest**](../Model/DataSyncApiJobV1ExecuteJobRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllTenantDataSyncJobs()`

```php
getAllTenantDataSyncJobs($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\DataSyncApiJobV1JobListResponsePaginatedItemsViewModel
```

Retrieves a list of DataSync Jobs

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
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
    $result = $apiInstance->getAllTenantDataSyncJobs($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->getAllTenantDataSyncJobs: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\DataSyncApiJobV1JobListResponsePaginatedItemsViewModel**](../Model/DataSyncApiJobV1JobListResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getJobById()`

```php
getJobById($tenantId, $jobId): \EdGraph\PlatformClient\Model\ValidationsApiJobsV1JobProfileResponse
```

Retrieves a Job by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 

try {
    $result = $apiInstance->getJobById($tenantId, $jobId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->getJobById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiJobsV1JobProfileResponse**](../Model/ValidationsApiJobsV1JobProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getJobs()`

```php
getJobs($tenantId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\ValidationsApiJobsV1PaginatedItemsResponse
```

Retrieves a list of Jobs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$filter = 'filter_example'; // string | 
$orderBy = 'orderBy_example'; // string | 

try {
    $result = $apiInstance->getJobs($tenantId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->getJobs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] |
| **orderBy** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiJobsV1PaginatedItemsResponse**](../Model/ValidationsApiJobsV1PaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantDataSyncJobProfileById()`

```php
getTenantDataSyncJobProfileById($tenantId, $jobId): \EdGraph\PlatformClient\Model\DataSyncApiJobV1JobProfileResponse
```

Retrieves a specific DataSync job using its primary key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 

try {
    $result = $apiInstance->getTenantDataSyncJobProfileById($tenantId, $jobId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->getTenantDataSyncJobProfileById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiJobV1JobProfileResponse**](../Model/DataSyncApiJobV1JobProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `restartJobSchedule()`

```php
restartJobSchedule($tenantId, $jobId)
```

Requests a Job schedule restart.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 

try {
    $apiInstance->restartJobSchedule($tenantId, $jobId);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->restartJobSchedule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateJob()`

```php
updateJob($tenantId, $jobId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest)
```

Updates a Job.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest | 

try {
    $apiInstance->updateJob($tenantId, $jobId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->updateJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTenantDataSyncJob()`

```php
updateTenantDataSyncJob($tenantId, $jobId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest)
```

Updates a DataSync job matching the primary key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest | 

try {
    $apiInstance->updateTenantDataSyncJob($tenantId, $jobId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->updateTenantDataSyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
