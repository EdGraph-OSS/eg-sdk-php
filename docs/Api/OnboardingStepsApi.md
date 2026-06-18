# EdGraph\PlatformClient\OnboardingStepsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createOnboardingStep()**](OnboardingStepsApi.md#createOnboardingStep) | **POST** /tenants/{tenantId}/onboardingsteps | Creates an Onboarding Step. |
| [**getOnboardingSteps()**](OnboardingStepsApi.md#getOnboardingSteps) | **GET** /tenants/{tenantId}/onboardingsteps | Gets a list of Onboarding Steps. |
| [**updateOnboardingStep()**](OnboardingStepsApi.md#updateOnboardingStep) | **PUT** /tenants/{tenantId}/onboardingsteps/{stepNumber} | Updates the status of an Onboarding Step. |


## `createOnboardingStep()`

```php
createOnboardingStep($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto): \EdGraph\PlatformClient\Model\TenantApiTenantV1TenantUpdatedResponse
```

Creates an Onboarding Step.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\OnboardingStepsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto | 

try {
    $result = $apiInstance->createOnboardingStep($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OnboardingStepsApi->createOnboardingStep: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1TenantUpdatedResponse**](../Model/TenantApiTenantV1TenantUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOnboardingSteps()`

```php
getOnboardingSteps($tenantId): \EdGraph\PlatformClient\Model\TenantApiTenantV1OnboardingStepsReponse
```

Gets a list of Onboarding Steps.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\OnboardingStepsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->getOnboardingSteps($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OnboardingStepsApi->getOnboardingSteps: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1OnboardingStepsReponse**](../Model/TenantApiTenantV1OnboardingStepsReponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateOnboardingStep()`

```php
updateOnboardingStep($tenantId, $stepNumber, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto): \EdGraph\PlatformClient\Model\TenantApiTenantV1TenantUpdatedResponse
```

Updates the status of an Onboarding Step.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\OnboardingStepsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$stepNumber = 56; // int | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto | 

try {
    $result = $apiInstance->updateOnboardingStep($tenantId, $stepNumber, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OnboardingStepsApi->updateOnboardingStep: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **stepNumber** | **int**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1TenantUpdatedResponse**](../Model/TenantApiTenantV1TenantUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
