# EdGraph\PlatformClient\TenantSettingsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTenantSetting()**](TenantSettingsApi.md#createTenantSetting) | **POST** /v2/tenants/{tenantId}/settings | Create a Tenant-scope setting |
| [**deleteTenantSetting()**](TenantSettingsApi.md#deleteTenantSetting) | **DELETE** /v2/tenants/{tenantId}/settings/{settingIdOrCode} | Delete the Tenant-scope setting for a key, addressed by SettingType id or Code |
| [**getTenantSetting()**](TenantSettingsApi.md#getTenantSetting) | **GET** /v2/tenants/{tenantId}/settings/{settingIdOrCode} | Get a Tenant-scope setting |
| [**searchTenantSettings()**](TenantSettingsApi.md#searchTenantSettings) | **GET** /v2/tenants/{tenantId}/settings | List Tenant-scope settings |
| [**setTenantSetting()**](TenantSettingsApi.md#setTenantSetting) | **PUT** /v2/tenants/{tenantId}/settings | Create or update (upsert) a Tenant-scope setting, addressed by the SettingTypeId in the body |
| [**updateTenantSetting()**](TenantSettingsApi.md#updateTenantSetting) | **PUT** /v2/tenants/{tenantId}/settings/{settingIdOrCode} | Update the Tenant-scope setting for a key, addressed by SettingType id or Code |


## `createTenantSetting()`

```php
createTenantSetting($tenantId, $edGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody): \EdGraph\PlatformClient\Model\SettingsApiTenantSettingsV1CreateTenantSettingResponse
```

Create a Tenant-scope setting

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$edGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody

try {
    $result = $apiInstance->createTenantSetting($tenantId, $edGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantSettingsApi->createTenantSetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody**](../Model/EdGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\SettingsApiTenantSettingsV1CreateTenantSettingResponse**](../Model/SettingsApiTenantSettingsV1CreateTenantSettingResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteTenantSetting()`

```php
deleteTenantSetting($tenantId, $settingIdOrCode, $edGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody)
```

Delete the Tenant-scope setting for a key, addressed by SettingType id or Code

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$settingIdOrCode = 'settingIdOrCode_example'; // string
$edGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody

try {
    $apiInstance->deleteTenantSetting($tenantId, $settingIdOrCode, $edGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody);
} catch (Exception $e) {
    echo 'Exception when calling TenantSettingsApi->deleteTenantSetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **settingIdOrCode** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody**](../Model/EdGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody.md)|  | [optional] |

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

## `getTenantSetting()`

```php
getTenantSetting($tenantId, $settingIdOrCode, $settingTypeId, $provider, $applicationId, $resolveEffectiveValue): \EdGraph\PlatformClient\Model\SettingsApiTenantSettingsV1TenantSettingMessage
```

Get a Tenant-scope setting

Answers with the stored record alone. Effective-value resolution is opt-in: pass  `resolveEffectiveValue=true` to instead receive the value in force at this scope — every  layer above it merged under the setting's own value.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$settingIdOrCode = 'settingIdOrCode_example'; // string
$settingTypeId = 'settingTypeId_example'; // string
$provider = 'provider_example'; // string
$applicationId = 'applicationId_example'; // string
$resolveEffectiveValue = false; // bool

try {
    $result = $apiInstance->getTenantSetting($tenantId, $settingIdOrCode, $settingTypeId, $provider, $applicationId, $resolveEffectiveValue);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantSettingsApi->getTenantSetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **settingIdOrCode** | **string**|  | |
| **settingTypeId** | **string**|  | [optional] |
| **provider** | **string**|  | [optional] |
| **applicationId** | **string**|  | [optional] |
| **resolveEffectiveValue** | **bool**|  | [optional] [default to false] |

### Return type

[**\EdGraph\PlatformClient\Model\SettingsApiTenantSettingsV1TenantSettingMessage**](../Model/SettingsApiTenantSettingsV1TenantSettingMessage.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchTenantSettings()`

```php
searchTenantSettings($tenantId, $applicationId, $settingTypeId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\SettingsApiTenantSettingsV1SearchTenantSettingsResponse
```

List Tenant-scope settings

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$applicationId = 'applicationId_example'; // string
$settingTypeId = 'settingTypeId_example'; // string
$pageIndex = 0; // int
$pageSize = 10; // int
$orderBy = ''; // string
$filter = ''; // string

try {
    $result = $apiInstance->searchTenantSettings($tenantId, $applicationId, $settingTypeId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantSettingsApi->searchTenantSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **applicationId** | **string**|  | [optional] |
| **settingTypeId** | **string**|  | [optional] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\SettingsApiTenantSettingsV1SearchTenantSettingsResponse**](../Model/SettingsApiTenantSettingsV1SearchTenantSettingsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setTenantSetting()`

```php
setTenantSetting($tenantId, $edGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody): \EdGraph\PlatformClient\Model\SettingsApiTenantSettingsV1SetTenantSettingResponse
```

Create or update (upsert) a Tenant-scope setting, addressed by the SettingTypeId in the body

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$edGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody

try {
    $result = $apiInstance->setTenantSetting($tenantId, $edGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantSettingsApi->setTenantSetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody**](../Model/EdGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\SettingsApiTenantSettingsV1SetTenantSettingResponse**](../Model/SettingsApiTenantSettingsV1SetTenantSettingResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTenantSetting()`

```php
updateTenantSetting($tenantId, $settingIdOrCode, $edGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody)
```

Update the Tenant-scope setting for a key, addressed by SettingType id or Code

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$settingIdOrCode = 'settingIdOrCode_example'; // string
$edGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody

try {
    $apiInstance->updateTenantSetting($tenantId, $settingIdOrCode, $edGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody);
} catch (Exception $e) {
    echo 'Exception when calling TenantSettingsApi->updateTenantSetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **settingIdOrCode** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody**](../Model/EdGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody.md)|  | [optional] |

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
