# EdGraph\PlatformClient\EdFiSyncApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createEdFiSync()**](EdFiSyncApi.md#createEdFiSync) | **POST** /tenants/{tenantId}/jobs/edfisync | Creates an Ed-Fi Sync Job for a given tenant |
| [**executeEdFiSyncJob()**](EdFiSyncApi.md#executeEdFiSyncJob) | **PUT** /tenants/{tenantId}/jobs/edfisync/execute | Executes an Ed-Fi Sync Job |
| [**getEdFiSyncData()**](EdFiSyncApi.md#getEdFiSyncData) | **GET** /tenants/{tenantId}/jobs/edfisync | Retrieves Ed-Fi Sync Connection Data for a given tenant |
| [**updateEdFiSync()**](EdFiSyncApi.md#updateEdFiSync) | **PUT** /tenants/{tenantId}/jobs/edfisync | Updates an Ed-Fi Sync for a given tenant |


## `createEdFiSync()`

```php
createEdFiSync($tenantId, $edGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult
```

Creates an Ed-Fi Sync Job for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EdFiSyncApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto | 

try {
    $result = $apiInstance->createEdFiSync($tenantId, $edGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EdFiSyncApi->createEdFiSync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto**](../Model/EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult**](../Model/EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `executeEdFiSyncJob()`

```php
executeEdFiSyncJob($tenantId): \EdGraph\PlatformClient\Model\DataSyncApiJobV1JobExecutionRequestedResponse
```

Executes an Ed-Fi Sync Job

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EdFiSyncApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->executeEdFiSyncJob($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EdFiSyncApi->executeEdFiSyncJob: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiJobV1JobExecutionRequestedResponse**](../Model/DataSyncApiJobV1JobExecutionRequestedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEdFiSyncData()`

```php
getEdFiSyncData($tenantId): \EdGraph\PlatformClient\Model\DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile
```

Retrieves Ed-Fi Sync Connection Data for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EdFiSyncApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->getEdFiSyncData($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EdFiSyncApi->getEdFiSyncData: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile**](../Model/DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateEdFiSync()`

```php
updateEdFiSync($tenantId, $body): \EdGraph\PlatformClient\Model\MicrosoftAspNetCoreMvcNoContentResult
```

Updates an Ed-Fi Sync for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EdFiSyncApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$body = NULL; // mixed | 

try {
    $result = $apiInstance->updateEdFiSync($tenantId, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EdFiSyncApi->updateEdFiSync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **body** | **mixed**|  | [optional] |

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
