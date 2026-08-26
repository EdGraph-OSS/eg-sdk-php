# EdGraph\PlatformClient\ClientSettingsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createClientSetting()**](ClientSettingsApi.md#createClientSetting) | **POST** /v2/tenants/{tenantId}/clients/{clientId}/settings | Create a Client-scope setting |
| [**deleteClientSetting()**](ClientSettingsApi.md#deleteClientSetting) | **DELETE** /v2/tenants/{tenantId}/clients/{clientId}/settings/{settingIdOrCode} | Delete the Client-scope setting for a key, addressed by SettingType id or Code |
| [**getClientSetting()**](ClientSettingsApi.md#getClientSetting) | **GET** /v2/tenants/{tenantId}/clients/{clientId}/settings/{settingIdOrCode} | Get a Client-scope setting |
| [**searchClientSettings()**](ClientSettingsApi.md#searchClientSettings) | **GET** /v2/tenants/{tenantId}/clients/{clientId}/settings | List Client-scope settings |
| [**setClientSetting()**](ClientSettingsApi.md#setClientSetting) | **PUT** /v2/tenants/{tenantId}/clients/{clientId}/settings | Create or update (upsert) a Client-scope setting, addressed by the SettingTypeId in the body |
| [**updateClientSetting()**](ClientSettingsApi.md#updateClientSetting) | **PUT** /v2/tenants/{tenantId}/clients/{clientId}/settings/{settingIdOrCode} | Update the Client-scope setting for a key, addressed by SettingType id or Code |


## `createClientSetting()`

```php
createClientSetting($tenantId, $clientId, $edGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody): \EdGraph\PlatformClient\Model\SettingsApiClientSettingsV1CreateClientSettingResponse
```

Create a Client-scope setting

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ClientSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$clientId = 'clientId_example'; // string
$edGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody

try {
    $result = $apiInstance->createClientSetting($tenantId, $clientId, $edGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientSettingsApi->createClientSetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody**](../Model/EdGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\SettingsApiClientSettingsV1CreateClientSettingResponse**](../Model/SettingsApiClientSettingsV1CreateClientSettingResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteClientSetting()`

```php
deleteClientSetting($tenantId, $clientId, $settingIdOrCode, $edGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody)
```

Delete the Client-scope setting for a key, addressed by SettingType id or Code

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ClientSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$clientId = 'clientId_example'; // string
$settingIdOrCode = 'settingIdOrCode_example'; // string
$edGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody

try {
    $apiInstance->deleteClientSetting($tenantId, $clientId, $settingIdOrCode, $edGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody);
} catch (Exception $e) {
    echo 'Exception when calling ClientSettingsApi->deleteClientSetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |
| **settingIdOrCode** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody**](../Model/EdGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody.md)|  | [optional] |

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

## `getClientSetting()`

```php
getClientSetting($tenantId, $clientId, $settingIdOrCode, $settingTypeId, $provider, $applicationId, $resolveEffectiveValue): \EdGraph\PlatformClient\Model\SettingsApiClientSettingsV1ClientSettingMessage
```

Get a Client-scope setting

Answers with the stored record alone. Effective-value resolution is opt-in: pass  `resolveEffectiveValue=true` to instead receive the value in force at this scope — every  layer above it merged under the setting's own value.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ClientSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$clientId = 'clientId_example'; // string
$settingIdOrCode = 'settingIdOrCode_example'; // string
$settingTypeId = 'settingTypeId_example'; // string
$provider = 'provider_example'; // string
$applicationId = 'applicationId_example'; // string
$resolveEffectiveValue = false; // bool

try {
    $result = $apiInstance->getClientSetting($tenantId, $clientId, $settingIdOrCode, $settingTypeId, $provider, $applicationId, $resolveEffectiveValue);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientSettingsApi->getClientSetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |
| **settingIdOrCode** | **string**|  | |
| **settingTypeId** | **string**|  | [optional] |
| **provider** | **string**|  | [optional] |
| **applicationId** | **string**|  | [optional] |
| **resolveEffectiveValue** | **bool**|  | [optional] [default to false] |

### Return type

[**\EdGraph\PlatformClient\Model\SettingsApiClientSettingsV1ClientSettingMessage**](../Model/SettingsApiClientSettingsV1ClientSettingMessage.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchClientSettings()`

```php
searchClientSettings($tenantId, $clientId, $applicationId, $settingTypeId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\SettingsApiClientSettingsV1SearchClientSettingsResponse
```

List Client-scope settings

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ClientSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$clientId = 'clientId_example'; // string
$applicationId = 'applicationId_example'; // string
$settingTypeId = 'settingTypeId_example'; // string
$pageIndex = 0; // int
$pageSize = 10; // int
$orderBy = ''; // string
$filter = ''; // string

try {
    $result = $apiInstance->searchClientSettings($tenantId, $clientId, $applicationId, $settingTypeId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientSettingsApi->searchClientSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |
| **applicationId** | **string**|  | [optional] |
| **settingTypeId** | **string**|  | [optional] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\SettingsApiClientSettingsV1SearchClientSettingsResponse**](../Model/SettingsApiClientSettingsV1SearchClientSettingsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setClientSetting()`

```php
setClientSetting($tenantId, $clientId, $edGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody): \EdGraph\PlatformClient\Model\SettingsApiClientSettingsV1SetClientSettingResponse
```

Create or update (upsert) a Client-scope setting, addressed by the SettingTypeId in the body

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ClientSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$clientId = 'clientId_example'; // string
$edGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody

try {
    $result = $apiInstance->setClientSetting($tenantId, $clientId, $edGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientSettingsApi->setClientSetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody**](../Model/EdGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\SettingsApiClientSettingsV1SetClientSettingResponse**](../Model/SettingsApiClientSettingsV1SetClientSettingResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateClientSetting()`

```php
updateClientSetting($tenantId, $clientId, $settingIdOrCode, $edGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody)
```

Update the Client-scope setting for a key, addressed by SettingType id or Code

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ClientSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$clientId = 'clientId_example'; // string
$settingIdOrCode = 'settingIdOrCode_example'; // string
$edGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody

try {
    $apiInstance->updateClientSetting($tenantId, $clientId, $settingIdOrCode, $edGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody);
} catch (Exception $e) {
    echo 'Exception when calling ClientSettingsApi->updateClientSetting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |
| **settingIdOrCode** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody**](../Model/EdGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody.md)|  | [optional] |

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
