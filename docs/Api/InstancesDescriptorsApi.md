# EdGraph\PlatformClient\InstancesDescriptorsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createDescriptorAsync()**](InstancesDescriptorsApi.md#createDescriptorAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors | Creates a Descriptor. |
| [**deleteDescriptorAsync()**](InstancesDescriptorsApi.md#deleteDescriptorAsync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Deletes a Descriptor. |
| [**getDescriptorByIdAsync()**](InstancesDescriptorsApi.md#getDescriptorByIdAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Retrieves a Descriptor by ID. |
| [**getDescriptorNamespacesAsync()**](InstancesDescriptorsApi.md#getDescriptorNamespacesAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/namespaces | Retrieves a list of Descriptor Namespaces. |
| [**getDescriptorsAsync()**](InstancesDescriptorsApi.md#getDescriptorsAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors | Retrieves a list of Descriptors. |
| [**updateDescriptorAsync()**](InstancesDescriptorsApi.md#updateDescriptorAsync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Updates a Descriptor. |


## `createDescriptorAsync()`

```php
createDescriptorAsync($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1DescriptorType): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse
```

Creates a Descriptor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$edfiAdminApiEdfiAdminV1DescriptorType = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorType(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorType | 

try {
    $result = $apiInstance->createDescriptorAsync($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1DescriptorType);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesDescriptorsApi->createDescriptorAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **edfiAdminApiEdfiAdminV1DescriptorType** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorType**](../Model/EdfiAdminApiEdfiAdminV1DescriptorType.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse**](../Model/EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteDescriptorAsync()`

```php
deleteDescriptorAsync($tenantId, $instanceId, $year, $descriptorId)
```

Deletes a Descriptor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$descriptorId = 56; // int | 

try {
    $apiInstance->deleteDescriptorAsync($tenantId, $instanceId, $year, $descriptorId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesDescriptorsApi->deleteDescriptorAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **descriptorId** | **int**|  | |

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

## `getDescriptorByIdAsync()`

```php
getDescriptorByIdAsync($tenantId, $instanceId, $year, $descriptorId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorType
```

Retrieves a Descriptor by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$descriptorId = 56; // int | 

try {
    $result = $apiInstance->getDescriptorByIdAsync($tenantId, $instanceId, $year, $descriptorId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesDescriptorsApi->getDescriptorByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **descriptorId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorType**](../Model/EdfiAdminApiEdfiAdminV1DescriptorType.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDescriptorNamespacesAsync()`

```php
getDescriptorNamespacesAsync($tenantId, $instanceId, $year, $pageSize, $pageIndex): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse
```

Retrieves a list of Descriptor Namespaces.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 

try {
    $result = $apiInstance->getDescriptorNamespacesAsync($tenantId, $instanceId, $year, $pageSize, $pageIndex);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesDescriptorsApi->getDescriptorNamespacesAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse**](../Model/EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDescriptorsAsync()`

```php
getDescriptorsAsync($tenantId, $instanceId, $year, $pageSize, $pageIndex, $filter, $orderBy): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse
```

Retrieves a list of Descriptors.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$filter = 'filter_example'; // string | 
$orderBy = 'orderBy_example'; // string | 

try {
    $result = $apiInstance->getDescriptorsAsync($tenantId, $instanceId, $year, $pageSize, $pageIndex, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesDescriptorsApi->getDescriptorsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **filter** | **string**|  | [optional] |
| **orderBy** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse**](../Model/EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateDescriptorAsync()`

```php
updateDescriptorAsync($tenantId, $instanceId, $year, $descriptorId, $edfiAdminApiEdfiAdminV1DescriptorType): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse
```

Updates a Descriptor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$descriptorId = 56; // int | 
$edfiAdminApiEdfiAdminV1DescriptorType = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorType(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorType | 

try {
    $result = $apiInstance->updateDescriptorAsync($tenantId, $instanceId, $year, $descriptorId, $edfiAdminApiEdfiAdminV1DescriptorType);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesDescriptorsApi->updateDescriptorAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **descriptorId** | **int**|  | |
| **edfiAdminApiEdfiAdminV1DescriptorType** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorType**](../Model/EdfiAdminApiEdfiAdminV1DescriptorType.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse**](../Model/EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
