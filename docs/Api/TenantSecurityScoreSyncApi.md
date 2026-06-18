# EdGraph\PlatformClient\TenantSecurityScoreSyncApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createSecurityScoreSyncJob()**](TenantSecurityScoreSyncApi.md#createSecurityScoreSyncJob) | **POST** /tenants/{tenantId}/jobs/securityscore | Creates an Security Score Sync Job for a given tenant |
| [**executeSecurityScoreSyncJob()**](TenantSecurityScoreSyncApi.md#executeSecurityScoreSyncJob) | **POST** /tenants/{tenantId}/jobs/securityscore/execute | Executes an Security Score Sync Job |
| [**getSecurityScoreSyncJob()**](TenantSecurityScoreSyncApi.md#getSecurityScoreSyncJob) | **GET** /tenants/{tenantId}/jobs/securityscore | Retrieves a Security Score Sync Job for a given tenant |
| [**getSecurityScoreSyncJobExecution()**](TenantSecurityScoreSyncApi.md#getSecurityScoreSyncJobExecution) | **GET** /tenants/{tenantId}/jobs/securityscore/{jobId}/executions/{jobExecutionId} | Retrieves a Security Score Sync Job Execution for a given tenant |
| [**updateSecurityScoreSyncJob()**](TenantSecurityScoreSyncApi.md#updateSecurityScoreSyncJob) | **PUT** /tenants/{tenantId}/jobs/securityscore | Updates a Security Score Sync for a given tenant |


## `createSecurityScoreSyncJob()`

```php
createSecurityScoreSyncJob($tenantId, $edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult
```

Creates an Security Score Sync Job for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantSecurityScoreSyncApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest | 

try {
    $result = $apiInstance->createSecurityScoreSyncJob($tenantId, $edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantSecurityScoreSyncApi->createSecurityScoreSyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult**](../Model/EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `executeSecurityScoreSyncJob()`

```php
executeSecurityScoreSyncJob($tenantId)
```

Executes an Security Score Sync Job

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantSecurityScoreSyncApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $apiInstance->executeSecurityScoreSyncJob($tenantId);
} catch (Exception $e) {
    echo 'Exception when calling TenantSecurityScoreSyncApi->executeSecurityScoreSyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

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

## `getSecurityScoreSyncJob()`

```php
getSecurityScoreSyncJob($tenantId): \EdGraph\PlatformClient\Model\DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile
```

Retrieves a Security Score Sync Job for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantSecurityScoreSyncApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->getSecurityScoreSyncJob($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantSecurityScoreSyncApi->getSecurityScoreSyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile**](../Model/DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSecurityScoreSyncJobExecution()`

```php
getSecurityScoreSyncJobExecution($tenantId, $jobId, $jobExecutionId): \EdGraph\PlatformClient\Model\DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile
```

Retrieves a Security Score Sync Job Execution for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantSecurityScoreSyncApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$jobExecutionId = 'jobExecutionId_example'; // string | 

try {
    $result = $apiInstance->getSecurityScoreSyncJobExecution($tenantId, $jobId, $jobExecutionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantSecurityScoreSyncApi->getSecurityScoreSyncJobExecution: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **jobExecutionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile**](../Model/DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSecurityScoreSyncJob()`

```php
updateSecurityScoreSyncJob($tenantId, $edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest)
```

Updates a Security Score Sync for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantSecurityScoreSyncApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest | 

try {
    $apiInstance->updateSecurityScoreSyncJob($tenantId, $edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest);
} catch (Exception $e) {
    echo 'Exception when calling TenantSecurityScoreSyncApi->updateSecurityScoreSyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest.md)|  | [optional] |

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
