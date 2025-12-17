# EdGraph\PlatformClient\InstancesDescriptorMappingsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createDescriptorMapping()**](InstancesDescriptorMappingsApi.md#createDescriptorMapping) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings | Creates a Descriptor Mapping. |
| [**deleteDescriptorMapping()**](InstancesDescriptorMappingsApi.md#deleteDescriptorMapping) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Deletes a Descriptor Mapping. |
| [**getDescriptorMappingById()**](InstancesDescriptorMappingsApi.md#getDescriptorMappingById) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Retrieves a Descriptor Mapping by ID. |
| [**getDescriptorMappings()**](InstancesDescriptorMappingsApi.md#getDescriptorMappings) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings | Retrieves a list of Descriptors Mappings. |
| [**updateDescriptorMapping()**](InstancesDescriptorMappingsApi.md#updateDescriptorMapping) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Updates a Descriptor Mapping. |


## `createDescriptorMapping()`

```php
createDescriptorMapping($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse
```

Creates a Descriptor Mapping.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesDescriptorMappingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$edfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest | 

try {
    $result = $apiInstance->createDescriptorMapping($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesDescriptorMappingsApi->createDescriptorMapping: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **edfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest**](../Model/EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse**](../Model/EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteDescriptorMapping()`

```php
deleteDescriptorMapping($tenantId, $instanceId, $year, $descriptorMappingId)
```

Deletes a Descriptor Mapping.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesDescriptorMappingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$descriptorMappingId = 'descriptorMappingId_example'; // string | 

try {
    $apiInstance->deleteDescriptorMapping($tenantId, $instanceId, $year, $descriptorMappingId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesDescriptorMappingsApi->deleteDescriptorMapping: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **descriptorMappingId** | **string**|  | |

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

## `getDescriptorMappingById()`

```php
getDescriptorMappingById($tenantId, $instanceId, $year, $descriptorMappingId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorMapping
```

Retrieves a Descriptor Mapping by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesDescriptorMappingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$descriptorMappingId = 'descriptorMappingId_example'; // string | 

try {
    $result = $apiInstance->getDescriptorMappingById($tenantId, $instanceId, $year, $descriptorMappingId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesDescriptorMappingsApi->getDescriptorMappingById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **descriptorMappingId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorMapping**](../Model/EdfiAdminApiEdfiAdminV1DescriptorMapping.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDescriptorMappings()`

```php
getDescriptorMappings($tenantId, $instanceId, $year, $pageSize, $pageIndex, $namespace): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse
```

Retrieves a list of Descriptors Mappings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesDescriptorMappingsApi(
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
$namespace = 'namespace_example'; // string | 

try {
    $result = $apiInstance->getDescriptorMappings($tenantId, $instanceId, $year, $pageSize, $pageIndex, $namespace);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesDescriptorMappingsApi->getDescriptorMappings: ', $e->getMessage(), PHP_EOL;
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
| **namespace** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse**](../Model/EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateDescriptorMapping()`

```php
updateDescriptorMapping($tenantId, $instanceId, $year, $descriptorMappingId, $edfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse
```

Updates a Descriptor Mapping.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesDescriptorMappingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$descriptorMappingId = 'descriptorMappingId_example'; // string | 
$edfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest | 

try {
    $result = $apiInstance->updateDescriptorMapping($tenantId, $instanceId, $year, $descriptorMappingId, $edfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesDescriptorMappingsApi->updateDescriptorMapping: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **descriptorMappingId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest**](../Model/EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse**](../Model/EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
