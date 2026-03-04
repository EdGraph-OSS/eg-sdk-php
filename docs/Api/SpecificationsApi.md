# EdGraph\PlatformClient\SpecificationsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createSpecification()**](SpecificationsApi.md#createSpecification) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications | Create a Specification resource |
| [**deleteSpecification()**](SpecificationsApi.md#deleteSpecification) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/{id} | Delete of Specification resource |
| [**exportSpecifications()**](SpecificationsApi.md#exportSpecifications) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/export | Export all Specifications resources given a Tenant |
| [**getSpecification()**](SpecificationsApi.md#getSpecification) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/{id} | Get Specification resource |
| [**purgeSpecification()**](SpecificationsApi.md#purgeSpecification) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/{specificationId}/purge | Purge a deleted Specification resource |
| [**recoverSpecification()**](SpecificationsApi.md#recoverSpecification) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/{specificationId}/recover | Recover deleted Specification resource |
| [**searchSpecifications()**](SpecificationsApi.md#searchSpecifications) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/search | Seaarch specifications |
| [**updateSpecification()**](SpecificationsApi.md#updateSpecification) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/{id} | Update specification |


## `createSpecification()`

```php
createSpecification($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1CreateSpecificationRequest)
```

Create a Specification resource

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SpecificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1CreateSpecificationRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateSpecificationRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateSpecificationRequest | 

try {
    $apiInstance->createSpecification($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1CreateSpecificationRequest);
} catch (Exception $e) {
    echo 'Exception when calling SpecificationsApi->createSpecification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1CreateSpecificationRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateSpecificationRequest**](../Model/EdfiAdminApiEdfiAdminV1CreateSpecificationRequest.md)|  | [optional] |

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

## `deleteSpecification()`

```php
deleteSpecification($tenantId, $instanceId, $id): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationDeletedResponse
```

Delete of Specification resource

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SpecificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$id = 'id_example'; // string | 

try {
    $result = $apiInstance->deleteSpecification($tenantId, $instanceId, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SpecificationsApi->deleteSpecification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **id** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationDeletedResponse**](../Model/EdfiAdminApiEdfiAdminV1SpecificationDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `exportSpecifications()`

```php
exportSpecifications($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1ExportSpecificationsRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationsExportedResponse
```

Export all Specifications resources given a Tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SpecificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1ExportSpecificationsRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ExportSpecificationsRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ExportSpecificationsRequest | 

try {
    $result = $apiInstance->exportSpecifications($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1ExportSpecificationsRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SpecificationsApi->exportSpecifications: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1ExportSpecificationsRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ExportSpecificationsRequest**](../Model/EdfiAdminApiEdfiAdminV1ExportSpecificationsRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationsExportedResponse**](../Model/EdfiAdminApiEdfiAdminV1SpecificationsExportedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSpecification()`

```php
getSpecification($id, $tenantId, $instanceId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationResponse
```

Get Specification resource

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SpecificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | 
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->getSpecification($id, $tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SpecificationsApi->getSpecification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationResponse**](../Model/EdfiAdminApiEdfiAdminV1SpecificationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `purgeSpecification()`

```php
purgeSpecification($tenantId, $instanceId, $specificationId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationPurgedResponse
```

Purge a deleted Specification resource

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SpecificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$specificationId = 'specificationId_example'; // string | 

try {
    $result = $apiInstance->purgeSpecification($tenantId, $instanceId, $specificationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SpecificationsApi->purgeSpecification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **specificationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationPurgedResponse**](../Model/EdfiAdminApiEdfiAdminV1SpecificationPurgedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `recoverSpecification()`

```php
recoverSpecification($tenantId, $instanceId, $specificationId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationRecoveredResponse
```

Recover deleted Specification resource

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SpecificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$specificationId = 'specificationId_example'; // string | 

try {
    $result = $apiInstance->recoverSpecification($tenantId, $instanceId, $specificationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SpecificationsApi->recoverSpecification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **specificationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationRecoveredResponse**](../Model/EdfiAdminApiEdfiAdminV1SpecificationRecoveredResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchSpecifications()`

```php
searchSpecifications($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1SearchSpecificationsRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationsSearchResponse
```

Seaarch specifications

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SpecificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1SearchSpecificationsRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SearchSpecificationsRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SearchSpecificationsRequest | 

try {
    $result = $apiInstance->searchSpecifications($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1SearchSpecificationsRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SpecificationsApi->searchSpecifications: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1SearchSpecificationsRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SearchSpecificationsRequest**](../Model/EdfiAdminApiEdfiAdminV1SearchSpecificationsRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationsSearchResponse**](../Model/EdfiAdminApiEdfiAdminV1SpecificationsSearchResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSpecification()`

```php
updateSpecification($tenantId, $instanceId, $id, $edfiAdminApiEdfiAdminV1UpdateSpecificationRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationUpdatedResponse
```

Update specification

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SpecificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$id = 'id_example'; // string | 
$edfiAdminApiEdfiAdminV1UpdateSpecificationRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateSpecificationRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateSpecificationRequest | 

try {
    $result = $apiInstance->updateSpecification($tenantId, $instanceId, $id, $edfiAdminApiEdfiAdminV1UpdateSpecificationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SpecificationsApi->updateSpecification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **id** | **string**|  | |
| **edfiAdminApiEdfiAdminV1UpdateSpecificationRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateSpecificationRequest**](../Model/EdfiAdminApiEdfiAdminV1UpdateSpecificationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SpecificationUpdatedResponse**](../Model/EdfiAdminApiEdfiAdminV1SpecificationUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
