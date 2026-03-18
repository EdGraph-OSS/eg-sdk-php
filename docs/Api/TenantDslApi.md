# EdGraph\PlatformClient\TenantDslApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createDslSync()**](TenantDslApi.md#createDslSync) | **POST** /tenants/{tenantId}/jobs/dsl | Creates a DSL Sync Job for a given tenant |
| [**executeDslSyncJob()**](TenantDslApi.md#executeDslSyncJob) | **PUT** /tenants/{tenantId}/jobs/dsl/{jobId}/execute | Executes a DSL Sync Job for a given tenant |
| [**getDslSyncData()**](TenantDslApi.md#getDslSyncData) | **GET** /tenants/{tenantId}/jobs/dsl/{jobId} | Retrieves a DSL jobs profile for a given tenant |
| [**updateDslSync()**](TenantDslApi.md#updateDslSync) | **PUT** /tenants/{tenantId}/jobs/dsl/{jobId} | Updates a DSL Sync Job for a given tenant |


## `createDslSync()`

```php
createDslSync($tenantId, $dataSyncApiDslV1CreateJobRequest): \EdGraph\PlatformClient\Model\DataSyncApiDslV1JobCreatedResponse
```

Creates a DSL Sync Job for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantDslApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$dataSyncApiDslV1CreateJobRequest = new \EdGraph\PlatformClient\Model\DataSyncApiDslV1CreateJobRequest(); // \EdGraph\PlatformClient\Model\DataSyncApiDslV1CreateJobRequest | 

try {
    $result = $apiInstance->createDslSync($tenantId, $dataSyncApiDslV1CreateJobRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantDslApi->createDslSync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **dataSyncApiDslV1CreateJobRequest** | [**\EdGraph\PlatformClient\Model\DataSyncApiDslV1CreateJobRequest**](../Model/DataSyncApiDslV1CreateJobRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiDslV1JobCreatedResponse**](../Model/DataSyncApiDslV1JobCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `executeDslSyncJob()`

```php
executeDslSyncJob($tenantId, $jobId): \EdGraph\PlatformClient\Model\DataSyncApiDslV1DslJobExecutedResponse
```

Executes a DSL Sync Job for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantDslApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 

try {
    $result = $apiInstance->executeDslSyncJob($tenantId, $jobId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantDslApi->executeDslSyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiDslV1DslJobExecutedResponse**](../Model/DataSyncApiDslV1DslJobExecutedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDslSyncData()`

```php
getDslSyncData($tenantId, $jobId): \EdGraph\PlatformClient\Model\DataSyncApiDslV1DslProfile
```

Retrieves a DSL jobs profile for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantDslApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 

try {
    $result = $apiInstance->getDslSyncData($tenantId, $jobId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantDslApi->getDslSyncData: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiDslV1DslProfile**](../Model/DataSyncApiDslV1DslProfile.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateDslSync()`

```php
updateDslSync($tenantId, $jobId, $dataSyncApiDslV1UpdateJobRequest): object
```

Updates a DSL Sync Job for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantDslApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$dataSyncApiDslV1UpdateJobRequest = new \EdGraph\PlatformClient\Model\DataSyncApiDslV1UpdateJobRequest(); // \EdGraph\PlatformClient\Model\DataSyncApiDslV1UpdateJobRequest | 

try {
    $result = $apiInstance->updateDslSync($tenantId, $jobId, $dataSyncApiDslV1UpdateJobRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantDslApi->updateDslSync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **dataSyncApiDslV1UpdateJobRequest** | [**\EdGraph\PlatformClient\Model\DataSyncApiDslV1UpdateJobRequest**](../Model/DataSyncApiDslV1UpdateJobRequest.md)|  | [optional] |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
