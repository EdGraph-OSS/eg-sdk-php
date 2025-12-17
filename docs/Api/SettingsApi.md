# EdGraph\PlatformClient\SettingsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getTenantSettings()**](SettingsApi.md#getTenantSettings) | **GET** /tenants/{tenantId}/settings | Retrieves a list of the Tenant&#39;s settings. |
| [**getTenantSettingsByCode()**](SettingsApi.md#getTenantSettingsByCode) | **GET** /tenants/{tenantId}/settings/{code} | Retrieves a Tenant&#39;s settings by code. |
| [**setTenantSettings()**](SettingsApi.md#setTenantSettings) | **POST** /tenants/{tenantId}/settings/{code} | Creates/updates a Tenant&#39;s settings. |


## `getTenantSettings()`

```php
getTenantSettings($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiTenantV1GetAppSettingsResponse
```

Retrieves a list of the Tenant's settings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getTenantSettings($tenantId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->getTenantSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1GetAppSettingsResponse**](../Model/TenantApiTenantV1GetAppSettingsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantSettingsByCode()`

```php
getTenantSettingsByCode($tenantId, $code): \EdGraph\PlatformClient\Model\TenantApiTenantV1TenantAppSettings
```

Retrieves a Tenant's settings by code.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$code = 'code_example'; // string | 

try {
    $result = $apiInstance->getTenantSettingsByCode($tenantId, $code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->getTenantSettingsByCode: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **code** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1TenantAppSettings**](../Model/TenantApiTenantV1TenantAppSettings.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setTenantSettings()`

```php
setTenantSettings($tenantId, $code, $tenantApiTenantV1SetAppSettingsRequest): \EdGraph\PlatformClient\Model\TenantApiTenantV1SetAppSettingsResponse
```

Creates/updates a Tenant's settings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$code = 'code_example'; // string | 
$tenantApiTenantV1SetAppSettingsRequest = new \EdGraph\PlatformClient\Model\TenantApiTenantV1SetAppSettingsRequest(); // \EdGraph\PlatformClient\Model\TenantApiTenantV1SetAppSettingsRequest | 

try {
    $result = $apiInstance->setTenantSettings($tenantId, $code, $tenantApiTenantV1SetAppSettingsRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->setTenantSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **code** | **string**|  | |
| **tenantApiTenantV1SetAppSettingsRequest** | [**\EdGraph\PlatformClient\Model\TenantApiTenantV1SetAppSettingsRequest**](../Model/TenantApiTenantV1SetAppSettingsRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1SetAppSettingsResponse**](../Model/TenantApiTenantV1SetAppSettingsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
