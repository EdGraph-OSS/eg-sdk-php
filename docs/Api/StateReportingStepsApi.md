# EdGraph\PlatformClient\StateReportingStepsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getSteps()**](StateReportingStepsApi.md#getSteps) | **GET** /tenants/{tenantId}/statereporting/schoolYear/{schoolYear}/steps | Get Steps Status for the tenant. |
| [**updateStep()**](StateReportingStepsApi.md#updateStep) | **POST** /tenants/{tenantId}/statereporting/schoolYear/{schoolYear}/steps | Update Steps Status for the tenant. |


## `getSteps()`

```php
getSteps($tenantId, $schoolYear): \EdGraph\PlatformClient\Model\ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse
```

Get Steps Status for the tenant.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\StateReportingStepsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$schoolYear = 56; // int | 

try {
    $result = $apiInstance->getSteps($tenantId, $schoolYear);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StateReportingStepsApi->getSteps: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **schoolYear** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse**](../Model/ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateStep()`

```php
updateStep($tenantId, $schoolYear, $validationsApiStateReportingStepsV1UpdateStateReportingStepRequest): \EdGraph\PlatformClient\Model\ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse
```

Update Steps Status for the tenant.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\StateReportingStepsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$schoolYear = 56; // int | 
$validationsApiStateReportingStepsV1UpdateStateReportingStepRequest = new \EdGraph\PlatformClient\Model\ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest | 

try {
    $result = $apiInstance->updateStep($tenantId, $schoolYear, $validationsApiStateReportingStepsV1UpdateStateReportingStepRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StateReportingStepsApi->updateStep: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **schoolYear** | **int**|  | |
| **validationsApiStateReportingStepsV1UpdateStateReportingStepRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest**](../Model/ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse**](../Model/ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
