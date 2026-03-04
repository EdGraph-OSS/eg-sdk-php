# EdGraph\PlatformClient\ObservationConfigurationApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getTenantObservationSettings()**](ObservationConfigurationApi.md#getTenantObservationSettings) | **GET** /tenants/{tenantId}/observations/configuration | Gets the Observation Settings for a given tenant |
| [**setObservationSettingApplicationSetting()**](ObservationConfigurationApi.md#setObservationSettingApplicationSetting) | **POST** /tenants/{tenantId}/observations/configuration/application | Sets the Application Settings of an Observation for a given Tenant |
| [**setObservationSettingUserSetting()**](ObservationConfigurationApi.md#setObservationSettingUserSetting) | **POST** /tenants/{tenantId}/observations/configuration/users | Sets the User Settings of an Observation for a given Tenant |


## `getTenantObservationSettings()`

```php
getTenantObservationSettings($tenantId): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1EvaluationSettingResponse
```

Gets the Observation Settings for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationConfigurationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->getTenantObservationSettings($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationConfigurationApi->getTenantObservationSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1EvaluationSettingResponse**](../Model/EvaluationApiEvaluationSettingsV1EvaluationSettingResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setObservationSettingApplicationSetting()`

```php
setObservationSettingApplicationSetting($tenantId, $evaluationApiEvaluationSettingsV1SetApplicationRequest): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1ApplicationSetResponse
```

Sets the Application Settings of an Observation for a given Tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationConfigurationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$evaluationApiEvaluationSettingsV1SetApplicationRequest = new \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1SetApplicationRequest(); // \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1SetApplicationRequest | 

try {
    $result = $apiInstance->setObservationSettingApplicationSetting($tenantId, $evaluationApiEvaluationSettingsV1SetApplicationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationConfigurationApi->setObservationSettingApplicationSetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **evaluationApiEvaluationSettingsV1SetApplicationRequest** | [**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1SetApplicationRequest**](../Model/EvaluationApiEvaluationSettingsV1SetApplicationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1ApplicationSetResponse**](../Model/EvaluationApiEvaluationSettingsV1ApplicationSetResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setObservationSettingUserSetting()`

```php
setObservationSettingUserSetting($tenantId, $evaluationApiEvaluationSettingsV1SetUsersRequest): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1UsersSetResponse
```

Sets the User Settings of an Observation for a given Tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationConfigurationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$evaluationApiEvaluationSettingsV1SetUsersRequest = new \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1SetUsersRequest(); // \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1SetUsersRequest | 

try {
    $result = $apiInstance->setObservationSettingUserSetting($tenantId, $evaluationApiEvaluationSettingsV1SetUsersRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationConfigurationApi->setObservationSettingUserSetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **evaluationApiEvaluationSettingsV1SetUsersRequest** | [**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1SetUsersRequest**](../Model/EvaluationApiEvaluationSettingsV1SetUsersRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1UsersSetResponse**](../Model/EvaluationApiEvaluationSettingsV1UsersSetResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
