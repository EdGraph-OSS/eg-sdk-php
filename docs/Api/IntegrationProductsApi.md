# EdGraph\PlatformClient\IntegrationProductsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createIntegrationProduct()**](IntegrationProductsApi.md#createIntegrationProduct) | **POST** /integrations/products | Creates an Integration Product. |
| [**deleteIntegrationProduct()**](IntegrationProductsApi.md#deleteIntegrationProduct) | **DELETE** /integrations/products/{productId} | Removes an Integration Product. |
| [**getIntegrationProduct()**](IntegrationProductsApi.md#getIntegrationProduct) | **GET** /integrations/products/{productId} | Gets an Integration Product. |
| [**searchIntegrationProducts()**](IntegrationProductsApi.md#searchIntegrationProducts) | **GET** /integrations/products | Search Integration Products. |
| [**updateIntegrationProduct()**](IntegrationProductsApi.md#updateIntegrationProduct) | **PUT** /integrations/products/{productId} | Updates an Integration Product. |


## `createIntegrationProduct()`

```php
createIntegrationProduct($tenantApiIntegrationsV1CreateIntegrationProductRequest): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationProductResponse
```

Creates an Integration Product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantApiIntegrationsV1CreateIntegrationProductRequest = new \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationProductRequest(); // \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationProductRequest | 

try {
    $result = $apiInstance->createIntegrationProduct($tenantApiIntegrationsV1CreateIntegrationProductRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationProductsApi->createIntegrationProduct: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantApiIntegrationsV1CreateIntegrationProductRequest** | [**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationProductRequest**](../Model/TenantApiIntegrationsV1CreateIntegrationProductRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1CreateIntegrationProductResponse**](../Model/TenantApiIntegrationsV1CreateIntegrationProductResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteIntegrationProduct()`

```php
deleteIntegrationProduct($productId): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1DeleteIntegrationProductResponse
```

Removes an Integration Product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$productId = 'productId_example'; // string | 

try {
    $result = $apiInstance->deleteIntegrationProduct($productId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationProductsApi->deleteIntegrationProduct: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **productId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1DeleteIntegrationProductResponse**](../Model/TenantApiIntegrationsV1DeleteIntegrationProductResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getIntegrationProduct()`

```php
getIntegrationProduct($productId): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1GetIntegrationProductResponse
```

Gets an Integration Product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$productId = 'productId_example'; // string | 

try {
    $result = $apiInstance->getIntegrationProduct($productId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationProductsApi->getIntegrationProduct: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **productId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1GetIntegrationProductResponse**](../Model/TenantApiIntegrationsV1GetIntegrationProductResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchIntegrationProducts()`

```php
searchIntegrationProducts($pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1IntegrationProductPaginatedItemsViewModel
```

Search Integration Products.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationProductsApi(
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
    $result = $apiInstance->searchIntegrationProducts($pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationProductsApi->searchIntegrationProducts: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1IntegrationProductPaginatedItemsViewModel**](../Model/TenantApiIntegrationsV1IntegrationProductPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateIntegrationProduct()`

```php
updateIntegrationProduct($productId, $tenantApiIntegrationsV1UpdateIntegrationProductRequest): object
```

Updates an Integration Product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\IntegrationProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$productId = 'productId_example'; // string | 
$tenantApiIntegrationsV1UpdateIntegrationProductRequest = new \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1UpdateIntegrationProductRequest(); // \EdGraph\PlatformClient\Model\TenantApiIntegrationsV1UpdateIntegrationProductRequest | 

try {
    $result = $apiInstance->updateIntegrationProduct($productId, $tenantApiIntegrationsV1UpdateIntegrationProductRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationProductsApi->updateIntegrationProduct: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **productId** | **string**|  | |
| **tenantApiIntegrationsV1UpdateIntegrationProductRequest** | [**\EdGraph\PlatformClient\Model\TenantApiIntegrationsV1UpdateIntegrationProductRequest**](../Model/TenantApiIntegrationsV1UpdateIntegrationProductRequest.md)|  | [optional] |

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
