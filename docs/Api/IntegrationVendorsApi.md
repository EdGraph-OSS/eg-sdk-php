# EdGraph\PlatformClient\IntegrationVendorsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createIntegrationVendor()**](IntegrationVendorsApi.md#createIntegrationVendor) | **POST** /integrations/vendors | Creates an Integration Vendor. |
| [**deleteIntegrationVendor()**](IntegrationVendorsApi.md#deleteIntegrationVendor) | **DELETE** /integrations/vendors/{vendorId} | Removes an Integration Vendor. |
| [**getIntegrationVendor()**](IntegrationVendorsApi.md#getIntegrationVendor) | **GET** /integrations/vendors/{vendorId} | Gets an Integration Vendor. |
| [**searchIntegrationVendors()**](IntegrationVendorsApi.md#searchIntegrationVendors) | **GET** /integrations/vendors | Search Integration Vendors. |
| [**updateIntegrationVendor()**](IntegrationVendorsApi.md#updateIntegrationVendor) | **PUT** /integrations/vendors/{vendorId} | Updates an Integration Vendor. |


## `createIntegrationVendor()`

```php
createIntegrationVendor($tenantApiIntegrationsV1CreateIntegrationVendorRequest): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationVendorResponse
```

Creates an Integration Vendor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationVendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantApiIntegrationsV1CreateIntegrationVendorRequest = new \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationVendorRequest(); // \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationVendorRequest | 

try {
    $result = $apiInstance->createIntegrationVendor($tenantApiIntegrationsV1CreateIntegrationVendorRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationVendorsApi->createIntegrationVendor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantApiIntegrationsV1CreateIntegrationVendorRequest** | [**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationVendorRequest**](../Model/TenantApiIntegrationsV1CreateIntegrationVendorRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationVendorResponse**](../Model/TenantApiIntegrationsV1CreateIntegrationVendorResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteIntegrationVendor()`

```php
deleteIntegrationVendor($vendorId): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1DeleteIntegrationVendorResponse
```

Removes an Integration Vendor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationVendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$vendorId = 'vendorId_example'; // string | 

try {
    $result = $apiInstance->deleteIntegrationVendor($vendorId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationVendorsApi->deleteIntegrationVendor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **vendorId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1DeleteIntegrationVendorResponse**](../Model/TenantApiIntegrationsV1DeleteIntegrationVendorResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getIntegrationVendor()`

```php
getIntegrationVendor($vendorId): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1GetIntegrationVendorResponse
```

Gets an Integration Vendor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationVendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$vendorId = 'vendorId_example'; // string | 

try {
    $result = $apiInstance->getIntegrationVendor($vendorId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationVendorsApi->getIntegrationVendor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **vendorId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1GetIntegrationVendorResponse**](../Model/TenantApiIntegrationsV1GetIntegrationVendorResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchIntegrationVendors()`

```php
searchIntegrationVendors($pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1IntegrationVendorPaginatedItemsViewModel
```

Search Integration Vendors.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationVendorsApi(
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
    $result = $apiInstance->searchIntegrationVendors($pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationVendorsApi->searchIntegrationVendors: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1IntegrationVendorPaginatedItemsViewModel**](../Model/TenantApiIntegrationsV1IntegrationVendorPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateIntegrationVendor()`

```php
updateIntegrationVendor($vendorId, $tenantApiIntegrationsV1UpdateIntegrationVendorRequest): object
```

Updates an Integration Vendor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationVendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$vendorId = 'vendorId_example'; // string | 
$tenantApiIntegrationsV1UpdateIntegrationVendorRequest = new \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1UpdateIntegrationVendorRequest(); // \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1UpdateIntegrationVendorRequest | 

try {
    $result = $apiInstance->updateIntegrationVendor($vendorId, $tenantApiIntegrationsV1UpdateIntegrationVendorRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationVendorsApi->updateIntegrationVendor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **vendorId** | **string**|  | |
| **tenantApiIntegrationsV1UpdateIntegrationVendorRequest** | [**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1UpdateIntegrationVendorRequest**](../Model/TenantApiIntegrationsV1UpdateIntegrationVendorRequest.md)|  | [optional] |

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
