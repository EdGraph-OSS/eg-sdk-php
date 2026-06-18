# EdGraph\PlatformClient\EvaluationSettingsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getEvaluationSetting()**](EvaluationSettingsApi.md#getEvaluationSetting) | **GET** /tenants/{tenantId}/evaluations/configuration | Gets the Evaluation Settings for a given tenant |
| [**setEvaluationSettingApplicationSetting()**](EvaluationSettingsApi.md#setEvaluationSettingApplicationSetting) | **POST** /tenants/{tenantId}/evaluations/configuration/application | Sets the Application Settings of an Evaluation for a given Tenant |
| [**setEvaluationSettingUserSetting()**](EvaluationSettingsApi.md#setEvaluationSettingUserSetting) | **POST** /tenants/{tenantId}/evaluations/configuration/users | Sets the User Settings of an Evaluation for a given Tenant |


## `getEvaluationSetting()`

```php
getEvaluationSetting($tenantId): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1EvaluationSettingResponse
```

Gets the Evaluation Settings for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EvaluationSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->getEvaluationSetting($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EvaluationSettingsApi->getEvaluationSetting: ', $e->getMessage(), PHP_EOL;
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

## `setEvaluationSettingApplicationSetting()`

```php
setEvaluationSettingApplicationSetting($tenantId, $evaluationApiEvaluationSettingsV1SetApplicationRequest): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1ApplicationSetResponse
```

Sets the Application Settings of an Evaluation for a given Tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EvaluationSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$evaluationApiEvaluationSettingsV1SetApplicationRequest = new \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1SetApplicationRequest(); // \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1SetApplicationRequest | 

try {
    $result = $apiInstance->setEvaluationSettingApplicationSetting($tenantId, $evaluationApiEvaluationSettingsV1SetApplicationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EvaluationSettingsApi->setEvaluationSettingApplicationSetting: ', $e->getMessage(), PHP_EOL;
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

## `setEvaluationSettingUserSetting()`

```php
setEvaluationSettingUserSetting($tenantId, $evaluationApiEvaluationSettingsV1SetUsersRequest): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1UsersSetResponse
```

Sets the User Settings of an Evaluation for a given Tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EvaluationSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$evaluationApiEvaluationSettingsV1SetUsersRequest = new \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1SetUsersRequest(); // \EdGraph\PlatformClient\Model\EvaluationApiEvaluationSettingsV1SetUsersRequest | 

try {
    $result = $apiInstance->setEvaluationSettingUserSetting($tenantId, $evaluationApiEvaluationSettingsV1SetUsersRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EvaluationSettingsApi->setEvaluationSettingUserSetting: ', $e->getMessage(), PHP_EOL;
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
