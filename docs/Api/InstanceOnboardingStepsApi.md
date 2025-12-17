# EdGraph\PlatformClient\InstanceOnboardingStepsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createInstanceOnboardingStepAsync()**](InstanceOnboardingStepsApi.md#createInstanceOnboardingStepAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/onboardingsteps | Creates an Onboarding Step. |
| [**updateInstanceOnboardingStepAsync()**](InstanceOnboardingStepsApi.md#updateInstanceOnboardingStepAsync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/onboardingsteps/{stepNumber} | Updates the status of an Onboarding Step. |


## `createInstanceOnboardingStepAsync()`

```php
createInstanceOnboardingStepAsync($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1CreateOnboardingStepRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse
```

Creates an Onboarding Step.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstanceOnboardingStepsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1CreateOnboardingStepRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest | 

try {
    $result = $apiInstance->createInstanceOnboardingStepAsync($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1CreateOnboardingStepRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstanceOnboardingStepsApi->createInstanceOnboardingStepAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1CreateOnboardingStepRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest**](../Model/EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse**](../Model/EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateInstanceOnboardingStepAsync()`

```php
updateInstanceOnboardingStepAsync($tenantId, $instanceId, $stepNumber, $edfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse
```

Updates the status of an Onboarding Step.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstanceOnboardingStepsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$stepNumber = 56; // int | 
$edfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest | 

try {
    $result = $apiInstance->updateInstanceOnboardingStepAsync($tenantId, $instanceId, $stepNumber, $edfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstanceOnboardingStepsApi->updateInstanceOnboardingStepAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **stepNumber** | **int**|  | |
| **edfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest**](../Model/EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse**](../Model/EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
