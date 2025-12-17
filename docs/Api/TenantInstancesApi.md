# EdGraph\PlatformClient\TenantInstancesApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**loadOnboardingStepEdFiApiMetadata()**](TenantInstancesApi.md#loadOnboardingStepEdFiApiMetadata) | **POST** /tenants/{tenantId}/onboardingsteps/edfi-api-metadata | Loads connection metadata. |
| [**testOnboardingStepConnection()**](TenantInstancesApi.md#testOnboardingStepConnection) | **POST** /tenants/{tenantId}/onboardingsteps/testconnection | Tests availability of provided connection metadata. |


## `loadOnboardingStepEdFiApiMetadata()`

```php
loadOnboardingStepEdFiApiMetadata($tenantId, $edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult
```

Loads connection metadata.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantInstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest | 

try {
    $result = $apiInstance->loadOnboardingStepEdFiApiMetadata($tenantId, $edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantInstancesApi->loadOnboardingStepEdFiApiMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult**](../Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `testOnboardingStepConnection()`

```php
testOnboardingStepConnection($tenantId, $body): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse
```

Tests availability of provided connection metadata.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantInstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$body = NULL; // mixed | 

try {
    $result = $apiInstance->testOnboardingStepConnection($tenantId, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantInstancesApi->testOnboardingStepConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **body** | **mixed**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
