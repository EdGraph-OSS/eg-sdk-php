# EdGraph\PlatformClient\OrganizationsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createOrganizationAsync()**](OrganizationsApi.md#createOrganizationAsync) | **POST** /tenants/{tenantId}/organizations | Creates an Organization. |
| [**deleteOrganizationAsync()**](OrganizationsApi.md#deleteOrganizationAsync) | **DELETE** /tenants/{tenantId}/organizations/{organizationIdentifier} | Deletes an Organization. |
| [**getOrganizationByIdAsync()**](OrganizationsApi.md#getOrganizationByIdAsync) | **GET** /tenants/{tenantId}/organizations/{organizationIdentifier} | Retrieves an Organization by ID. |
| [**getOrganizationsAsync()**](OrganizationsApi.md#getOrganizationsAsync) | **GET** /tenants/{tenantId}/organizations | Retrieves a list of Organizations. |
| [**updateOrganizationAsync()**](OrganizationsApi.md#updateOrganizationAsync) | **PUT** /tenants/{tenantId}/organizations/{organizationIdentifier} | Updates an Organization. |


## `createOrganizationAsync()`

```php
createOrganizationAsync($tenantId, $tenantApiTenantV1CreateOrganizationRequest): \EdGraph\PlatformClient\Model\TenantApiTenantV1OrganizationCreatedResponse
```

Creates an Organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\OrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$tenantApiTenantV1CreateOrganizationRequest = new \EdGraph\PlatformClient\Model\TenantApiTenantV1CreateOrganizationRequest(); // \EdGraph\PlatformClient\Model\TenantApiTenantV1CreateOrganizationRequest | 

try {
    $result = $apiInstance->createOrganizationAsync($tenantId, $tenantApiTenantV1CreateOrganizationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationsApi->createOrganizationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **tenantApiTenantV1CreateOrganizationRequest** | [**\EdGraph\PlatformClient\Model\TenantApiTenantV1CreateOrganizationRequest**](../Model/TenantApiTenantV1CreateOrganizationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1OrganizationCreatedResponse**](../Model/TenantApiTenantV1OrganizationCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteOrganizationAsync()`

```php
deleteOrganizationAsync($tenantId, $organizationIdentifier): \EdGraph\PlatformClient\Model\TenantApiTenantV1OrganizationDeletedResponse
```

Deletes an Organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\OrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$organizationIdentifier = 'organizationIdentifier_example'; // string | 

try {
    $result = $apiInstance->deleteOrganizationAsync($tenantId, $organizationIdentifier);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationsApi->deleteOrganizationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **organizationIdentifier** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1OrganizationDeletedResponse**](../Model/TenantApiTenantV1OrganizationDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrganizationByIdAsync()`

```php
getOrganizationByIdAsync($tenantId, $organizationIdentifier): \EdGraph\PlatformClient\Model\TenantApiTenantV1Organization
```

Retrieves an Organization by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\OrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$organizationIdentifier = 'organizationIdentifier_example'; // string | 

try {
    $result = $apiInstance->getOrganizationByIdAsync($tenantId, $organizationIdentifier);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationsApi->getOrganizationByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **organizationIdentifier** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1Organization**](../Model/TenantApiTenantV1Organization.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrganizationsAsync()`

```php
getOrganizationsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiTenantV1GetOrganizationsPaginatedResponse
```

Retrieves a list of Organizations.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\OrganizationsApi(
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
    $result = $apiInstance->getOrganizationsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationsApi->getOrganizationsAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1GetOrganizationsPaginatedResponse**](../Model/TenantApiTenantV1GetOrganizationsPaginatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateOrganizationAsync()`

```php
updateOrganizationAsync($tenantId, $organizationIdentifier, $tenantApiTenantV1UpdateOrganizationRequest): \EdGraph\PlatformClient\Model\TenantApiTenantV1OrganizationUpdatedResponse
```

Updates an Organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\OrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$organizationIdentifier = 'organizationIdentifier_example'; // string | 
$tenantApiTenantV1UpdateOrganizationRequest = new \EdGraph\PlatformClient\Model\TenantApiTenantV1UpdateOrganizationRequest(); // \EdGraph\PlatformClient\Model\TenantApiTenantV1UpdateOrganizationRequest | 

try {
    $result = $apiInstance->updateOrganizationAsync($tenantId, $organizationIdentifier, $tenantApiTenantV1UpdateOrganizationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationsApi->updateOrganizationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **organizationIdentifier** | **string**|  | |
| **tenantApiTenantV1UpdateOrganizationRequest** | [**\EdGraph\PlatformClient\Model\TenantApiTenantV1UpdateOrganizationRequest**](../Model/TenantApiTenantV1UpdateOrganizationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1OrganizationUpdatedResponse**](../Model/TenantApiTenantV1OrganizationUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
