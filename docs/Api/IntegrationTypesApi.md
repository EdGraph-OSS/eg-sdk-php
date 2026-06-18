# EdGraph\PlatformClient\IntegrationTypesApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createIntegrationType()**](IntegrationTypesApi.md#createIntegrationType) | **POST** /integrations/types | Creates an Integration Type. |
| [**deleteIntegrationType()**](IntegrationTypesApi.md#deleteIntegrationType) | **DELETE** /integrations/types/{typeId} | Removes an Integration Type. |
| [**getIntegrationType()**](IntegrationTypesApi.md#getIntegrationType) | **GET** /integrations/types/{typeId} | Gets an Integration Type. |
| [**searchIntegrationTypes()**](IntegrationTypesApi.md#searchIntegrationTypes) | **GET** /integrations/types | Search Integration Types. |
| [**updateIntegrationType()**](IntegrationTypesApi.md#updateIntegrationType) | **PUT** /integrations/types/{typeId} | Updates an Integration Type. |


## `createIntegrationType()`

```php
createIntegrationType($tenantApiIntegrationsV1CreateIntegrationTypeRequest): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationTypeResponse
```

Creates an Integration Type.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationTypesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantApiIntegrationsV1CreateIntegrationTypeRequest = new \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationTypeRequest(); // \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationTypeRequest | 

try {
    $result = $apiInstance->createIntegrationType($tenantApiIntegrationsV1CreateIntegrationTypeRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationTypesApi->createIntegrationType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantApiIntegrationsV1CreateIntegrationTypeRequest** | [**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationTypeRequest**](../Model/TenantApiIntegrationsV1CreateIntegrationTypeRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationTypeResponse**](../Model/TenantApiIntegrationsV1CreateIntegrationTypeResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteIntegrationType()`

```php
deleteIntegrationType($typeId): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1DeleteIntegrationTypeResponse
```

Removes an Integration Type.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationTypesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$typeId = 'typeId_example'; // string | 

try {
    $result = $apiInstance->deleteIntegrationType($typeId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationTypesApi->deleteIntegrationType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **typeId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1DeleteIntegrationTypeResponse**](../Model/TenantApiIntegrationsV1DeleteIntegrationTypeResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getIntegrationType()`

```php
getIntegrationType($typeId): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1GetIntegrationTypeResponse
```

Gets an Integration Type.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationTypesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$typeId = 'typeId_example'; // string | 

try {
    $result = $apiInstance->getIntegrationType($typeId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationTypesApi->getIntegrationType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **typeId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1GetIntegrationTypeResponse**](../Model/TenantApiIntegrationsV1GetIntegrationTypeResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchIntegrationTypes()`

```php
searchIntegrationTypes($pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1IntegrationTypePaginatedItemsViewModel
```

Search Integration Types.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationTypesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->searchIntegrationTypes($pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationTypesApi->searchIntegrationTypes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1IntegrationTypePaginatedItemsViewModel**](../Model/TenantApiIntegrationsV1IntegrationTypePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateIntegrationType()`

```php
updateIntegrationType($typeId, $tenantApiIntegrationsV1UpdateIntegrationTypeRequest): object
```

Updates an Integration Type.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationTypesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$typeId = 'typeId_example'; // string | 
$tenantApiIntegrationsV1UpdateIntegrationTypeRequest = new \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1UpdateIntegrationTypeRequest(); // \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1UpdateIntegrationTypeRequest | 

try {
    $result = $apiInstance->updateIntegrationType($typeId, $tenantApiIntegrationsV1UpdateIntegrationTypeRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationTypesApi->updateIntegrationType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **typeId** | **string**|  | |
| **tenantApiIntegrationsV1UpdateIntegrationTypeRequest** | [**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1UpdateIntegrationTypeRequest**](../Model/TenantApiIntegrationsV1UpdateIntegrationTypeRequest.md)|  | [optional] |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
