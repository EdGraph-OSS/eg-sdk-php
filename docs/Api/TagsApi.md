# EdGraph\PlatformClient\TagsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTag()**](TagsApi.md#createTag) | **POST** /tenants/{tenantId}/validations/tags | Creates a Tag. |
| [**deleteTag()**](TagsApi.md#deleteTag) | **DELETE** /tenants/{tenantId}/validations/tags/{tagId} | Deletes a Tag. |
| [**getTagById()**](TagsApi.md#getTagById) | **GET** /tenants/{tenantId}/validations/tags/{tagId} | Retrieves a Tag by ID. |
| [**getTags()**](TagsApi.md#getTags) | **GET** /tenants/{tenantId}/validations/tags | Retrieves a list of Tags. |
| [**updateTag()**](TagsApi.md#updateTag) | **PUT** /tenants/{tenantId}/validations/tags/{tagId} | Updates a Tag. |


## `createTag()`

```php
createTag($tenantId, $validationsApiTagsV1CreateRequest): \EdGraph\PlatformClient\Model\ValidationsApiCoreV1CreatedResponse
```

Creates a Tag.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TagsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$validationsApiTagsV1CreateRequest = new \EdGraph\PlatformClient\Model\ValidationsApiTagsV1CreateRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiTagsV1CreateRequest | 

try {
    $result = $apiInstance->createTag($tenantId, $validationsApiTagsV1CreateRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TagsApi->createTag: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **validationsApiTagsV1CreateRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiTagsV1CreateRequest**](../Model/ValidationsApiTagsV1CreateRequest.md)|  | [optional] |

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

## `deleteTag()`

```php
deleteTag($tenantId, $tagId)
```

Deletes a Tag.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TagsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$tagId = 'tagId_example'; // string | 

try {
    $apiInstance->deleteTag($tenantId, $tagId);
} catch (Exception $e) {
    echo 'Exception when calling TagsApi->deleteTag: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **tagId** | **string**|  | |

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

## `getTagById()`

```php
getTagById($tenantId, $tagId): \EdGraph\PlatformClient\Model\ValidationsApiTagsV1TagDto
```

Retrieves a Tag by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TagsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$tagId = 'tagId_example'; // string | 

try {
    $result = $apiInstance->getTagById($tenantId, $tagId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TagsApi->getTagById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **tagId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiTagsV1TagDto**](../Model/ValidationsApiTagsV1TagDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTags()`

```php
getTags($tenantId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\ValidationsApiTagsV1PaginatedTags
```

Retrieves a list of Tags.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TagsApi(
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
    $result = $apiInstance->getTags($tenantId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TagsApi->getTags: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\ValidationsApiTagsV1PaginatedTags**](../Model/ValidationsApiTagsV1PaginatedTags.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTag()`

```php
updateTag($tenantId, $tagId, $validationsApiTagsV1UpdateRequest)
```

Updates a Tag.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TagsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$tagId = 'tagId_example'; // string | 
$validationsApiTagsV1UpdateRequest = new \EdGraph\PlatformClient\Model\ValidationsApiTagsV1UpdateRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiTagsV1UpdateRequest | 

try {
    $apiInstance->updateTag($tenantId, $tagId, $validationsApiTagsV1UpdateRequest);
} catch (Exception $e) {
    echo 'Exception when calling TagsApi->updateTag: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **tagId** | **string**|  | |
| **validationsApiTagsV1UpdateRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiTagsV1UpdateRequest**](../Model/ValidationsApiTagsV1UpdateRequest.md)|  | [optional] |

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
