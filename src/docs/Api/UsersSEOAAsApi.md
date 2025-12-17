# EdGraph\PlatformClient\UsersSEOAAsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addUserSEOAA()**](UsersSEOAAsApi.md#addUserSEOAA) | **POST** /v2/tenants/{tenantId}/users/{userId}/seoaas | Add User SEOAAs |
| [**deleteUserSEOAA()**](UsersSEOAAsApi.md#deleteUserSEOAA) | **DELETE** /v2/tenants/{tenantId}/users/{userId}/seoaas/{seoaaId} | Delete User SEOAAs |
| [**searchUserSEOAA()**](UsersSEOAAsApi.md#searchUserSEOAA) | **GET** /v2/tenants/{tenantId}/users/{userId}/seoaas | Search User SEOAAs |
| [**updateUserSEOAA()**](UsersSEOAAsApi.md#updateUserSEOAA) | **PUT** /v2/tenants/{tenantId}/users/{userId}/seoaas/{seoaaId} | Update User SEOAAs |


## `addUserSEOAA()`

```php
addUserSEOAA($tenantId, $userId, $edGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1SEOAAAddedResponse
```

Add User SEOAAs

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersSEOAAsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest | 

try {
    $result = $apiInstance->addUserSEOAA($tenantId, $userId, $edGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersSEOAAsApi->addUserSEOAA: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1SEOAAAddedResponse**](../Model/IdentityApiUserV1SEOAAAddedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteUserSEOAA()`

```php
deleteUserSEOAA($tenantId, $userId, $seoaaId): \EdGraph\PlatformClient\Model\IdentityApiUserV1SEOAAUpdatedResponse
```

Delete User SEOAAs

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersSEOAAsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$seoaaId = 'seoaaId_example'; // string | 

try {
    $result = $apiInstance->deleteUserSEOAA($tenantId, $userId, $seoaaId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersSEOAAsApi->deleteUserSEOAA: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **seoaaId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1SEOAAUpdatedResponse**](../Model/IdentityApiUserV1SEOAAUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchUserSEOAA()`

```php
searchUserSEOAA($tenantId, $userId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\IdentityApiUserV1GetSEOAAsResponse
```

Search User SEOAAs

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersSEOAAsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->searchUserSEOAA($tenantId, $userId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersSEOAAsApi->searchUserSEOAA: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1GetSEOAAsResponse**](../Model/IdentityApiUserV1GetSEOAAsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateUserSEOAA()`

```php
updateUserSEOAA($tenantId, $userId, $seoaaId, $edGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1SEOAAUpdatedResponse
```

Update User SEOAAs

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersSEOAAsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$seoaaId = 'seoaaId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest | 

try {
    $result = $apiInstance->updateUserSEOAA($tenantId, $userId, $seoaaId, $edGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersSEOAAsApi->updateUserSEOAA: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **seoaaId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1SEOAAUpdatedResponse**](../Model/IdentityApiUserV1SEOAAUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
