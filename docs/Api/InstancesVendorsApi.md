# EdGraph\PlatformClient\InstancesVendorsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createVendorAsync()**](InstancesVendorsApi.md#createVendorAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors | Creates a new Vendor. |
| [**deleteVendorAsync()**](InstancesVendorsApi.md#deleteVendorAsync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId} | Deletes a Vendor. |
| [**getVendorByIdAsync()**](InstancesVendorsApi.md#getVendorByIdAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId} | Retrieves a Vendor by ID. |
| [**getVendorsAsync()**](InstancesVendorsApi.md#getVendorsAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors | Retrieves a list of Vendors. |
| [**syncVendorAsync()**](InstancesVendorsApi.md#syncVendorAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId}/sync | Copies a Vendor from one instance to another/other instance(s). |
| [**updateVendorAsync()**](InstancesVendorsApi.md#updateVendorAsync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId} | Updates a Vendor. |


## `createVendorAsync()`

```php
createVendorAsync($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1CreateVendorRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1VendorCreatedResponse
```

Creates a new Vendor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesVendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1CreateVendorRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateVendorRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateVendorRequest | 

try {
    $result = $apiInstance->createVendorAsync($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1CreateVendorRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesVendorsApi->createVendorAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1CreateVendorRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateVendorRequest**](../Model/EdfiAdminApiEdfiAdminV1CreateVendorRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1VendorCreatedResponse**](../Model/EdfiAdminApiEdfiAdminV1VendorCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteVendorAsync()`

```php
deleteVendorAsync($tenantId, $instanceId, $vendorId)
```

Deletes a Vendor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesVendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$vendorId = 56; // int | 

try {
    $apiInstance->deleteVendorAsync($tenantId, $instanceId, $vendorId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesVendorsApi->deleteVendorAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **vendorId** | **int**|  | |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVendorByIdAsync()`

```php
getVendorByIdAsync($tenantId, $instanceId, $vendorId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1VendorProfileResponse
```

Retrieves a Vendor by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesVendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$vendorId = 'vendorId_example'; // string | 

try {
    $result = $apiInstance->getVendorByIdAsync($tenantId, $instanceId, $vendorId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesVendorsApi->getVendorByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **vendorId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1VendorProfileResponse**](../Model/EdfiAdminApiEdfiAdminV1VendorProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVendorsAsync()`

```php
getVendorsAsync($tenantId, $instanceId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1VendorListResponsePaginatedItemsViewModel
```

Retrieves a list of Vendors.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesVendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getVendorsAsync($tenantId, $instanceId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesVendorsApi->getVendorsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1VendorListResponsePaginatedItemsViewModel**](../Model/EdfiAdminApiEdfiAdminV1VendorListResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `syncVendorAsync()`

```php
syncVendorAsync($tenantId, $instanceId, $vendorId, $edfiAdminApiEdfiAdminV1SyncVendorRequest)
```

Copies a Vendor from one instance to another/other instance(s).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesVendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$vendorId = 56; // int | 
$edfiAdminApiEdfiAdminV1SyncVendorRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncVendorRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncVendorRequest | 

try {
    $apiInstance->syncVendorAsync($tenantId, $instanceId, $vendorId, $edfiAdminApiEdfiAdminV1SyncVendorRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesVendorsApi->syncVendorAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **vendorId** | **int**|  | |
| **edfiAdminApiEdfiAdminV1SyncVendorRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncVendorRequest**](../Model/EdfiAdminApiEdfiAdminV1SyncVendorRequest.md)|  | [optional] |

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

## `updateVendorAsync()`

```php
updateVendorAsync($tenantId, $instanceId, $vendorId, $edfiAdminApiEdfiAdminV1UpdateVendorRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1VendorUpdatedResponse
```

Updates a Vendor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesVendorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$vendorId = 'vendorId_example'; // string | 
$edfiAdminApiEdfiAdminV1UpdateVendorRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateVendorRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateVendorRequest | 

try {
    $result = $apiInstance->updateVendorAsync($tenantId, $instanceId, $vendorId, $edfiAdminApiEdfiAdminV1UpdateVendorRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesVendorsApi->updateVendorAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **vendorId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1UpdateVendorRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateVendorRequest**](../Model/EdfiAdminApiEdfiAdminV1UpdateVendorRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1VendorUpdatedResponse**](../Model/EdfiAdminApiEdfiAdminV1VendorUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
