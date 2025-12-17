# EdGraph\PlatformClient\CollectionsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createCollection()**](CollectionsApi.md#createCollection) | **POST** /tenants/{tenantId}/validations/collections | Creates a Collection. |
| [**createContainer()**](CollectionsApi.md#createContainer) | **POST** /tenants/{tenantId}/validations/collections/{collectionId}/containers | Creates a Container. |
| [**deleteCollection()**](CollectionsApi.md#deleteCollection) | **DELETE** /tenants/{tenantId}/validations/collections/{collectionId} | Deletes a Collection. |
| [**deleteContainer()**](CollectionsApi.md#deleteContainer) | **DELETE** /tenants/{tenantId}/validations/collections/{collectionId}/containers/{containerId} | Deletes a Container. |
| [**getCollectionById()**](CollectionsApi.md#getCollectionById) | **GET** /tenants/{tenantId}/validations/collections/{collectionId} | Retrieves a Collection by ID. |
| [**getCollectionJson()**](CollectionsApi.md#getCollectionJson) | **GET** /tenants/{tenantId}/validations/collections/{collectionId}/export | Retrieves the JSON representation of a Collection. Useful for exporting into other systems. |
| [**getCollections()**](CollectionsApi.md#getCollections) | **GET** /tenants/{tenantId}/validations/collections | Retrieves a list of Collections. |
| [**getCollectionsTree()**](CollectionsApi.md#getCollectionsTree) | **GET** /tenants/{tenantId}/validations/categories/tree | Retrieves a list of Collections. |
| [**getContainerById()**](CollectionsApi.md#getContainerById) | **GET** /tenants/{tenantId}/validations/collections/{collectionId}/containers/{containerId} | Retrieves a Container by ID. |
| [**getContainers()**](CollectionsApi.md#getContainers) | **GET** /tenants/{tenantId}/validations/collections/{collectionId}/containers | Retrieves a list of Containers. |
| [**updateCollection()**](CollectionsApi.md#updateCollection) | **PUT** /tenants/{tenantId}/validations/collections/{collectionId} | Updates a Collection. |
| [**updateContainer()**](CollectionsApi.md#updateContainer) | **PUT** /tenants/{tenantId}/validations/collections/{collectionId}/containers/{containerId} | Updates a Container. |
| [**uploadCollectionJson()**](CollectionsApi.md#uploadCollectionJson) | **POST** /tenants/{tenantId}/validations/collections/import | Uploads a Collection JSON. Useful for importing from another system. |


## `createCollection()`

```php
createCollection($tenantId, $validationsApiContainersV1CreateCollectionRequest): \EdGraph\PlatformClient\Model\ValidationsApiCoreV1CreatedResponse
```

Creates a Collection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$validationsApiContainersV1CreateCollectionRequest = new \EdGraph\PlatformClient\Model\ValidationsApiContainersV1CreateCollectionRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiContainersV1CreateCollectionRequest | 

try {
    $result = $apiInstance->createCollection($tenantId, $validationsApiContainersV1CreateCollectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->createCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **validationsApiContainersV1CreateCollectionRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1CreateCollectionRequest**](../Model/ValidationsApiContainersV1CreateCollectionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiCoreV1CreatedResponse**](../Model/ValidationsApiCoreV1CreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createContainer()`

```php
createContainer($tenantId, $collectionId, $validationsApiContainersV1CreateContainerRequest): \EdGraph\PlatformClient\Model\ValidationsApiCoreV1CreatedResponse
```

Creates a Container.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$collectionId = 'collectionId_example'; // string | 
$validationsApiContainersV1CreateContainerRequest = new \EdGraph\PlatformClient\Model\ValidationsApiContainersV1CreateContainerRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiContainersV1CreateContainerRequest | 

try {
    $result = $apiInstance->createContainer($tenantId, $collectionId, $validationsApiContainersV1CreateContainerRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->createContainer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **collectionId** | **string**|  | |
| **validationsApiContainersV1CreateContainerRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1CreateContainerRequest**](../Model/ValidationsApiContainersV1CreateContainerRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiCoreV1CreatedResponse**](../Model/ValidationsApiCoreV1CreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteCollection()`

```php
deleteCollection($tenantId, $collectionId)
```

Deletes a Collection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$collectionId = 'collectionId_example'; // string | 

try {
    $apiInstance->deleteCollection($tenantId, $collectionId);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->deleteCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **collectionId** | **string**|  | |

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

## `deleteContainer()`

```php
deleteContainer($tenantId, $collectionId, $containerId)
```

Deletes a Container.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$collectionId = 'collectionId_example'; // string | 
$containerId = 'containerId_example'; // string | 

try {
    $apiInstance->deleteContainer($tenantId, $collectionId, $containerId);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->deleteContainer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **collectionId** | **string**|  | |
| **containerId** | **string**|  | |

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

## `getCollectionById()`

```php
getCollectionById($tenantId, $collectionId): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1ContainerDto
```

Retrieves a Collection by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$collectionId = 'collectionId_example'; // string | 

try {
    $result = $apiInstance->getCollectionById($tenantId, $collectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->getCollectionById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **collectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1ContainerDto**](../Model/ValidationsApiContainersV1ContainerDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCollectionJson()`

```php
getCollectionJson($tenantId, $collectionId): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1GetJsonResponse
```

Retrieves the JSON representation of a Collection. Useful for exporting into other systems.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$collectionId = 'collectionId_example'; // string | 

try {
    $result = $apiInstance->getCollectionJson($tenantId, $collectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->getCollectionJson: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **collectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1GetJsonResponse**](../Model/ValidationsApiContainersV1GetJsonResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCollections()`

```php
getCollections($tenantId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1PaginatedContainers
```

Retrieves a list of Collections.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$filter = 'filter_example'; // string | 
$orderBy = 'orderBy_example'; // string | 

try {
    $result = $apiInstance->getCollections($tenantId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->getCollections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] |
| **orderBy** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1PaginatedContainers**](../Model/ValidationsApiContainersV1PaginatedContainers.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCollectionsTree()`

```php
getCollectionsTree($tenantId, $pageIndex, $pageSize, $orderBy, $categoryId, $categoryName, $subCategoryId, $subCategoryName): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1PaginatedCategoryTreeResponse
```

Retrieves a list of Collections.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = 'orderBy_example'; // string | 
$categoryId = 'categoryId_example'; // string | 
$categoryName = 'categoryName_example'; // string | 
$subCategoryId = 'subCategoryId_example'; // string | 
$subCategoryName = 'subCategoryName_example'; // string | 

try {
    $result = $apiInstance->getCollectionsTree($tenantId, $pageIndex, $pageSize, $orderBy, $categoryId, $categoryName, $subCategoryId, $subCategoryName);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->getCollectionsTree: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] |
| **categoryId** | **string**|  | [optional] |
| **categoryName** | **string**|  | [optional] |
| **subCategoryId** | **string**|  | [optional] |
| **subCategoryName** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1PaginatedCategoryTreeResponse**](../Model/ValidationsApiContainersV1PaginatedCategoryTreeResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getContainerById()`

```php
getContainerById($tenantId, $collectionId, $containerId): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1ContainerDto
```

Retrieves a Container by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$collectionId = 'collectionId_example'; // string | 
$containerId = 'containerId_example'; // string | 

try {
    $result = $apiInstance->getContainerById($tenantId, $collectionId, $containerId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->getContainerById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **collectionId** | **string**|  | |
| **containerId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1ContainerDto**](../Model/ValidationsApiContainersV1ContainerDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getContainers()`

```php
getContainers($tenantId, $collectionId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1PaginatedContainers
```

Retrieves a list of Containers.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$collectionId = 'collectionId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$filter = 'filter_example'; // string | 
$orderBy = 'orderBy_example'; // string | 

try {
    $result = $apiInstance->getContainers($tenantId, $collectionId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->getContainers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **collectionId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] |
| **orderBy** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1PaginatedContainers**](../Model/ValidationsApiContainersV1PaginatedContainers.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateCollection()`

```php
updateCollection($tenantId, $collectionId, $validationsApiContainersV1UpdateCollectionRequest)
```

Updates a Collection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$collectionId = 'collectionId_example'; // string | 
$validationsApiContainersV1UpdateCollectionRequest = new \EdGraph\PlatformClient\Model\ValidationsApiContainersV1UpdateCollectionRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiContainersV1UpdateCollectionRequest | 

try {
    $apiInstance->updateCollection($tenantId, $collectionId, $validationsApiContainersV1UpdateCollectionRequest);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->updateCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **collectionId** | **string**|  | |
| **validationsApiContainersV1UpdateCollectionRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1UpdateCollectionRequest**](../Model/ValidationsApiContainersV1UpdateCollectionRequest.md)|  | [optional] |

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

## `updateContainer()`

```php
updateContainer($tenantId, $collectionId, $containerId, $validationsApiContainersV1UpdateContainerRequest)
```

Updates a Container.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$collectionId = 'collectionId_example'; // string | 
$containerId = 'containerId_example'; // string | 
$validationsApiContainersV1UpdateContainerRequest = new \EdGraph\PlatformClient\Model\ValidationsApiContainersV1UpdateContainerRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiContainersV1UpdateContainerRequest | 

try {
    $apiInstance->updateContainer($tenantId, $collectionId, $containerId, $validationsApiContainersV1UpdateContainerRequest);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->updateContainer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **collectionId** | **string**|  | |
| **containerId** | **string**|  | |
| **validationsApiContainersV1UpdateContainerRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1UpdateContainerRequest**](../Model/ValidationsApiContainersV1UpdateContainerRequest.md)|  | [optional] |

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

## `uploadCollectionJson()`

```php
uploadCollectionJson($tenantId, $validationsApiContainersV1UploadCollectionRequest): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1CollectionUploadedResponse
```

Uploads a Collection JSON. Useful for importing from another system.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$validationsApiContainersV1UploadCollectionRequest = new \EdGraph\PlatformClient\Model\ValidationsApiContainersV1UploadCollectionRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiContainersV1UploadCollectionRequest | 

try {
    $result = $apiInstance->uploadCollectionJson($tenantId, $validationsApiContainersV1UploadCollectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->uploadCollectionJson: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **validationsApiContainersV1UploadCollectionRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1UploadCollectionRequest**](../Model/ValidationsApiContainersV1UploadCollectionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1CollectionUploadedResponse**](../Model/ValidationsApiContainersV1CollectionUploadedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
