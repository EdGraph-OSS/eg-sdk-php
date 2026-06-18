# EdGraph\PlatformClient\OnboardingStepsConnectionsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createOnboardingStepConnection()**](OnboardingStepsConnectionsApi.md#createOnboardingStepConnection) | **POST** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections | Creates an Onboarding Step connection. |
| [**getOnboardingStepConnectionById()**](OnboardingStepsConnectionsApi.md#getOnboardingStepConnectionById) | **GET** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections/{connectionId} | Get an Onboarding Step connection by Id |
| [**updateOnboardingStepConnection()**](OnboardingStepsConnectionsApi.md#updateOnboardingStepConnection) | **PUT** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections/{connectionId} | Update an Onboarding Step connection by Id |


## `createOnboardingStepConnection()`

```php
createOnboardingStepConnection($tenantId, $stepNumber, $body): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse
```

Creates an Onboarding Step connection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\OnboardingStepsConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$stepNumber = 56; // int | 
$body = NULL; // mixed | 

try {
    $result = $apiInstance->createOnboardingStepConnection($tenantId, $stepNumber, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OnboardingStepsConnectionsApi->createOnboardingStepConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **stepNumber** | **int**|  | |
| **body** | **mixed**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOnboardingStepConnectionById()`

```php
getOnboardingStepConnectionById($tenantId, $stepNumber, $connectionId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse
```

Get an Onboarding Step connection by Id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\OnboardingStepsConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$stepNumber = 56; // int | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->getOnboardingStepConnectionById($tenantId, $stepNumber, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OnboardingStepsConnectionsApi->getOnboardingStepConnectionById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **stepNumber** | **int**|  | |
| **connectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateOnboardingStepConnection()`

```php
updateOnboardingStepConnection($tenantId, $stepNumber, $connectionId, $body): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse
```

Update an Onboarding Step connection by Id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\OnboardingStepsConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$stepNumber = 56; // int | 
$connectionId = 'connectionId_example'; // string | 
$body = NULL; // mixed | 

try {
    $result = $apiInstance->updateOnboardingStepConnection($tenantId, $stepNumber, $connectionId, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OnboardingStepsConnectionsApi->updateOnboardingStepConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **stepNumber** | **int**|  | |
| **connectionId** | **string**|  | |
| **body** | **mixed**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
