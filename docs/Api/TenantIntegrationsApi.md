# EdGraph\PlatformClient\TenantIntegrationsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addTenantIntegration()**](TenantIntegrationsApi.md#addTenantIntegration) | **POST** /tenants/{tenantId}/integrations | Creates an Integration for a tenant. |
| [**deleteTenantIntegration()**](TenantIntegrationsApi.md#deleteTenantIntegration) | **DELETE** /tenants/{tenantId}/integrations/{id} | Removes a tenant Integration. |
| [**getTenantIntegration()**](TenantIntegrationsApi.md#getTenantIntegration) | **GET** /tenants/{tenantId}/integrations/{id} | Gets a tenant Integration. |
| [**searchIntegrations()**](TenantIntegrationsApi.md#searchIntegrations) | **GET** /tenants/{tenantId}/integrations | Search a Tenant&#39;s Integrations |
| [**updateTenantIntegration()**](TenantIntegrationsApi.md#updateTenantIntegration) | **PUT** /tenants/{tenantId}/integrations/{id} | Updates a tenant Integration. |


## `addTenantIntegration()`

```php
addTenantIntegration($tenantId, $tenantApiIntegrationsV1CreateIntegrationRequest): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationResponse
```

Creates an Integration for a tenant.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantIntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$tenantApiIntegrationsV1CreateIntegrationRequest = new \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationRequest(); // \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationRequest | 

try {
    $result = $apiInstance->addTenantIntegration($tenantId, $tenantApiIntegrationsV1CreateIntegrationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantIntegrationsApi->addTenantIntegration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **tenantApiIntegrationsV1CreateIntegrationRequest** | [**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationRequest**](../Model/TenantApiIntegrationsV1CreateIntegrationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationResponse**](../Model/TenantApiIntegrationsV1CreateIntegrationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteTenantIntegration()`

```php
deleteTenantIntegration($tenantId, $id): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1DeleteIntegrationResponse
```

Removes a tenant Integration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantIntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$id = 'id_example'; // string | 

try {
    $result = $apiInstance->deleteTenantIntegration($tenantId, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantIntegrationsApi->deleteTenantIntegration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **id** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1DeleteIntegrationResponse**](../Model/TenantApiIntegrationsV1DeleteIntegrationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantIntegration()`

```php
getTenantIntegration($tenantId, $id): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1GetIntegrationResponse
```

Gets a tenant Integration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantIntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$id = 'id_example'; // string | 

try {
    $result = $apiInstance->getTenantIntegration($tenantId, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantIntegrationsApi->getTenantIntegration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **id** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1GetIntegrationResponse**](../Model/TenantApiIntegrationsV1GetIntegrationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchIntegrations()`

```php
searchIntegrations($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1IntegrationPaginatedItemsViewModel
```

Search a Tenant's Integrations

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantIntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->searchIntegrations($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantIntegrationsApi->searchIntegrations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1IntegrationPaginatedItemsViewModel**](../Model/TenantApiIntegrationsV1IntegrationPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTenantIntegration()`

```php
updateTenantIntegration($tenantId, $id, $tenantApiIntegrationsV1UpdateIntegrationRequest): object
```

Updates a tenant Integration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantIntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$id = 'id_example'; // string | 
$tenantApiIntegrationsV1UpdateIntegrationRequest = new \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1UpdateIntegrationRequest(); // \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1UpdateIntegrationRequest | 

try {
    $result = $apiInstance->updateTenantIntegration($tenantId, $id, $tenantApiIntegrationsV1UpdateIntegrationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantIntegrationsApi->updateTenantIntegration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **id** | **string**|  | |
| **tenantApiIntegrationsV1UpdateIntegrationRequest** | [**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1UpdateIntegrationRequest**](../Model/TenantApiIntegrationsV1UpdateIntegrationRequest.md)|  | [optional] |

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
