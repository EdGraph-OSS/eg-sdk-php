# EdGraph\PlatformClient\MySettingsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createMySetting()**](MySettingsApi.md#createMySetting) | **POST** /me/settings | Create a User-scope setting |
| [**deleteMySetting()**](MySettingsApi.md#deleteMySetting) | **DELETE** /me/settings/{settingIdOrCode} | Delete the User-scope setting for a key, addressed by SettingType id or Code |
| [**getMySetting()**](MySettingsApi.md#getMySetting) | **GET** /me/settings/{settingIdOrCode} | Get a User-scope setting |
| [**searchMySettings()**](MySettingsApi.md#searchMySettings) | **GET** /me/settings | List User-scope settings |
| [**setMySetting()**](MySettingsApi.md#setMySetting) | **PUT** /me/settings | Create or update (upsert) a User-scope setting, addressed by the SettingTypeId in the body |
| [**updateMySetting()**](MySettingsApi.md#updateMySetting) | **PUT** /me/settings/{settingIdOrCode} | Update the User-scope setting for a key, addressed by SettingType id or Code |


## `createMySetting()`

```php
createMySetting($edGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody): \EdGraph\PlatformClient\Model\SettingsApiUserSettingsV1CreateUserSettingResponse
```

Create a User-scope setting

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MySettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$edGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody = new \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody(); // \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody

try {
    $result = $apiInstance->createMySetting($edGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MySettingsApi->createMySetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **edGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody** | [**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\SettingsApiUserSettingsV1CreateUserSettingResponse**](../Model/SettingsApiUserSettingsV1CreateUserSettingResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteMySetting()`

```php
deleteMySetting($settingIdOrCode, $edGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody)
```

Delete the User-scope setting for a key, addressed by SettingType id or Code

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MySettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$settingIdOrCode = 'settingIdOrCode_example'; // string
$edGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody = new \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody(); // \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody

try {
    $apiInstance->deleteMySetting($settingIdOrCode, $edGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody);
} catch (Exception $e) {
    echo 'Exception when calling MySettingsApi->deleteMySetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **settingIdOrCode** | **string**|  | |
| **edGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody** | [**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody.md)|  | [optional] |

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

## `getMySetting()`

```php
getMySetting($settingIdOrCode, $settingTypeId, $provider, $applicationId, $resolveEffectiveValue): \EdGraph\PlatformClient\Model\SettingsApiUserSettingsV1UserSettingMessage
```

Get a User-scope setting

Answers with the stored record alone. Effective-value resolution is opt-in: pass  `resolveEffectiveValue=true` to instead receive the value in force at this scope — every  layer above it merged under the setting's own value.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MySettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$settingIdOrCode = 'settingIdOrCode_example'; // string
$settingTypeId = 'settingTypeId_example'; // string
$provider = 'provider_example'; // string
$applicationId = 'applicationId_example'; // string
$resolveEffectiveValue = false; // bool

try {
    $result = $apiInstance->getMySetting($settingIdOrCode, $settingTypeId, $provider, $applicationId, $resolveEffectiveValue);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MySettingsApi->getMySetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **settingIdOrCode** | **string**|  | |
| **settingTypeId** | **string**|  | [optional] |
| **provider** | **string**|  | [optional] |
| **applicationId** | **string**|  | [optional] |
| **resolveEffectiveValue** | **bool**|  | [optional] [default to false] |

### Return type

[**\EdGraph\PlatformClient\Model\SettingsApiUserSettingsV1UserSettingMessage**](../Model/SettingsApiUserSettingsV1UserSettingMessage.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchMySettings()`

```php
searchMySettings($applicationId, $settingTypeId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\SettingsApiUserSettingsV1SearchUserSettingsResponse
```

List User-scope settings

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MySettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$applicationId = 'applicationId_example'; // string
$settingTypeId = 'settingTypeId_example'; // string
$pageIndex = 0; // int
$pageSize = 10; // int
$orderBy = ''; // string
$filter = ''; // string

try {
    $result = $apiInstance->searchMySettings($applicationId, $settingTypeId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MySettingsApi->searchMySettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **applicationId** | **string**|  | [optional] |
| **settingTypeId** | **string**|  | [optional] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\SettingsApiUserSettingsV1SearchUserSettingsResponse**](../Model/SettingsApiUserSettingsV1SearchUserSettingsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setMySetting()`

```php
setMySetting($edGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody): \EdGraph\PlatformClient\Model\SettingsApiUserSettingsV1SetUserSettingResponse
```

Create or update (upsert) a User-scope setting, addressed by the SettingTypeId in the body

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MySettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$edGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody = new \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody(); // \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody

try {
    $result = $apiInstance->setMySetting($edGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MySettingsApi->setMySetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **edGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody** | [**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\SettingsApiUserSettingsV1SetUserSettingResponse**](../Model/SettingsApiUserSettingsV1SetUserSettingResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateMySetting()`

```php
updateMySetting($settingIdOrCode, $edGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody)
```

Update the User-scope setting for a key, addressed by SettingType id or Code

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MySettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$settingIdOrCode = 'settingIdOrCode_example'; // string
$edGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody = new \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody(); // \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody

try {
    $apiInstance->updateMySetting($settingIdOrCode, $edGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody);
} catch (Exception $e) {
    echo 'Exception when calling MySettingsApi->updateMySetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **settingIdOrCode** | **string**|  | |
| **edGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody** | [**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody.md)|  | [optional] |

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
