# EdGraph\PlatformClient\ApplicationsSettingsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getClientSettingsAsync()**](ApplicationsSettingsApi.md#getClientSettingsAsync) | **GET** /tenants/{tenantId}/clients/{clientId}/settings | Retrieves a list of a Tenant&#39;s ClientSettings. |
| [**getClientSettingsByCodeAsync()**](ApplicationsSettingsApi.md#getClientSettingsByCodeAsync) | **GET** /tenants/{tenantId}/clients/{clientId}/settings/{code} | Retrieves a Tenant&#39;s ClientSetting by code. |
| [**getClientSettingsTypesAsync()**](ApplicationsSettingsApi.md#getClientSettingsTypesAsync) | **GET** /tenants/{tenantId}/clients/{clientId}/settingstypes | Retrieves a list of ClientSettingsTypes. |
| [**setClientSettingsAsync()**](ApplicationsSettingsApi.md#setClientSettingsAsync) | **POST** /tenants/{tenantId}/clients/{clientId}/settings | Creates/updates a Tenant&#39;s ClientSettings. |
| [**setClientSettingsByCodeAsync()**](ApplicationsSettingsApi.md#setClientSettingsByCodeAsync) | **POST** /tenants/{tenantId}/clients/{clientId}/settings/{code} | Creates/updates a Tenant&#39;s ClientSetting by code. |


## `getClientSettingsAsync()`

```php
getClientSettingsAsync($tenantId, $clientId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiTenantV1GetAppSettingsResponse
```

Retrieves a list of a Tenant's ClientSettings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ApplicationsSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$clientId = 'clientId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 100; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getClientSettingsAsync($tenantId, $clientId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsSettingsApi->getClientSettingsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 100] |
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

## `getClientSettingsByCodeAsync()`

```php
getClientSettingsByCodeAsync($tenantId, $clientId, $code): \EdGraph\PlatformClient\Model\TenantApiTenantV1TenantAppSettings
```

Retrieves a Tenant's ClientSetting by code.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ApplicationsSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$clientId = 'clientId_example'; // string | 
$code = 'code_example'; // string | 

try {
    $result = $apiInstance->getClientSettingsByCodeAsync($tenantId, $clientId, $code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsSettingsApi->getClientSettingsByCodeAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |
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

## `getClientSettingsTypesAsync()`

```php
getClientSettingsTypesAsync($tenantId, $clientId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\IdentityApiClientSettingsTypeV1GetClientSettingsTypesResponse
```

Retrieves a list of ClientSettingsTypes.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ApplicationsSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$clientId = 'clientId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getClientSettingsTypesAsync($tenantId, $clientId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsSettingsApi->getClientSettingsTypesAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiClientSettingsTypeV1GetClientSettingsTypesResponse**](../Model/IdentityApiClientSettingsTypeV1GetClientSettingsTypesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setClientSettingsAsync()`

```php
setClientSettingsAsync($tenantId, $clientId, $tenantApiTenantV1SetAppSettingsRequest): \EdGraph\PlatformClient\Model\TenantApiTenantV1SetAppSettingsResponse
```

Creates/updates a Tenant's ClientSettings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ApplicationsSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$clientId = 'clientId_example'; // string | 
$tenantApiTenantV1SetAppSettingsRequest = new \EdGraph\PlatformClient\Model\TenantApiTenantV1SetAppSettingsRequest(); // \EdGraph\PlatformClient\Model\TenantApiTenantV1SetAppSettingsRequest | 

try {
    $result = $apiInstance->setClientSettingsAsync($tenantId, $clientId, $tenantApiTenantV1SetAppSettingsRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsSettingsApi->setClientSettingsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |
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

## `setClientSettingsByCodeAsync()`

```php
setClientSettingsByCodeAsync($tenantId, $clientId, $code, $tenantApiTenantV1SetAppSettingsRequest): \EdGraph\PlatformClient\Model\TenantApiTenantV1SetAppSettingsResponse
```

Creates/updates a Tenant's ClientSetting by code.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ApplicationsSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$clientId = 'clientId_example'; // string | 
$code = 'code_example'; // string | 
$tenantApiTenantV1SetAppSettingsRequest = new \EdGraph\PlatformClient\Model\TenantApiTenantV1SetAppSettingsRequest(); // \EdGraph\PlatformClient\Model\TenantApiTenantV1SetAppSettingsRequest | 

try {
    $result = $apiInstance->setClientSettingsByCodeAsync($tenantId, $clientId, $code, $tenantApiTenantV1SetAppSettingsRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsSettingsApi->setClientSettingsByCodeAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |
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
