# EdGraph\PlatformClient\InstancesClaimSetsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createClaimSetAsync()**](InstancesClaimSetsApi.md#createClaimSetAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets | Creates a ClaimSet. |
| [**deleteClaimSetAsync()**](InstancesClaimSetsApi.md#deleteClaimSetAsync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Deletes a ClaimSet. |
| [**getClaimSetByIdAsync()**](InstancesClaimSetsApi.md#getClaimSetByIdAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Retrieves a ClaimSet by ID. |
| [**getClaimSetsAsync()**](InstancesClaimSetsApi.md#getClaimSetsAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets | Retrieves a list of ClaimSets. |
| [**getResourceClaimsGridAsync()**](InstancesClaimSetsApi.md#getResourceClaimsGridAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId}/resourceclaims | Retrieves a grid of Resource Claims. |
| [**syncClaimSetAsync()**](InstancesClaimSetsApi.md#syncClaimSetAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId}/sync | Copies a Claim Set from one instance to another/other instance(s) |
| [**updateClaimSetAsync()**](InstancesClaimSetsApi.md#updateClaimSetAsync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Updates a ClaimSet. |


## `createClaimSetAsync()`

```php
createClaimSetAsync($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1SaveClaimSetRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SaveClaimSetResponse
```

Creates a ClaimSet.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesClaimSetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1SaveClaimSetRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SaveClaimSetRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SaveClaimSetRequest | 

try {
    $result = $apiInstance->createClaimSetAsync($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1SaveClaimSetRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesClaimSetsApi->createClaimSetAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1SaveClaimSetRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SaveClaimSetRequest**](../Model/EdfiAdminApiEdfiAdminV1SaveClaimSetRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SaveClaimSetResponse**](../Model/EdfiAdminApiEdfiAdminV1SaveClaimSetResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteClaimSetAsync()`

```php
deleteClaimSetAsync($tenantId, $instanceId, $claimSetId)
```

Deletes a ClaimSet.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesClaimSetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$claimSetId = 56; // int | 

try {
    $apiInstance->deleteClaimSetAsync($tenantId, $instanceId, $claimSetId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesClaimSetsApi->deleteClaimSetAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **claimSetId** | **int**|  | |

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

## `getClaimSetByIdAsync()`

```php
getClaimSetByIdAsync($tenantId, $instanceId, $claimSetId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ClaimSet
```

Retrieves a ClaimSet by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesClaimSetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$claimSetId = 56; // int | 

try {
    $result = $apiInstance->getClaimSetByIdAsync($tenantId, $instanceId, $claimSetId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesClaimSetsApi->getClaimSetByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **claimSetId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ClaimSet**](../Model/EdfiAdminApiEdfiAdminV1ClaimSet.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getClaimSetsAsync()`

```php
getClaimSetsAsync($tenantId, $instanceId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel
```

Retrieves a list of ClaimSets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesClaimSetsApi(
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
    $result = $apiInstance->getClaimSetsAsync($tenantId, $instanceId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesClaimSetsApi->getClaimSetsAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel**](../Model/EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getResourceClaimsGridAsync()`

```php
getResourceClaimsGridAsync($tenantId, $instanceId, $claimSetId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse
```

Retrieves a grid of Resource Claims.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesClaimSetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$claimSetId = 56; // int | 

try {
    $result = $apiInstance->getResourceClaimsGridAsync($tenantId, $instanceId, $claimSetId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesClaimSetsApi->getResourceClaimsGridAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **claimSetId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse**](../Model/EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `syncClaimSetAsync()`

```php
syncClaimSetAsync($tenantId, $instanceId, $claimSetId, $edfiAdminApiEdfiAdminV1SyncClaimSetRequest)
```

Copies a Claim Set from one instance to another/other instance(s)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesClaimSetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$claimSetId = 56; // int | 
$edfiAdminApiEdfiAdminV1SyncClaimSetRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncClaimSetRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncClaimSetRequest | 

try {
    $apiInstance->syncClaimSetAsync($tenantId, $instanceId, $claimSetId, $edfiAdminApiEdfiAdminV1SyncClaimSetRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesClaimSetsApi->syncClaimSetAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **claimSetId** | **int**|  | |
| **edfiAdminApiEdfiAdminV1SyncClaimSetRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncClaimSetRequest**](../Model/EdfiAdminApiEdfiAdminV1SyncClaimSetRequest.md)|  | [optional] |

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

## `updateClaimSetAsync()`

```php
updateClaimSetAsync($tenantId, $instanceId, $claimSetId, $edfiAdminApiEdfiAdminV1SaveClaimSetRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SaveClaimSetResponse
```

Updates a ClaimSet.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesClaimSetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$claimSetId = 56; // int | 
$edfiAdminApiEdfiAdminV1SaveClaimSetRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SaveClaimSetRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SaveClaimSetRequest | 

try {
    $result = $apiInstance->updateClaimSetAsync($tenantId, $instanceId, $claimSetId, $edfiAdminApiEdfiAdminV1SaveClaimSetRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesClaimSetsApi->updateClaimSetAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **claimSetId** | **int**|  | |
| **edfiAdminApiEdfiAdminV1SaveClaimSetRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SaveClaimSetRequest**](../Model/EdfiAdminApiEdfiAdminV1SaveClaimSetRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SaveClaimSetResponse**](../Model/EdfiAdminApiEdfiAdminV1SaveClaimSetResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
