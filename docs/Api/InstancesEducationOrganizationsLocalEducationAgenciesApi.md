# EdGraph\PlatformClient\InstancesEducationOrganizationsLocalEducationAgenciesApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createLocalEducationAgencyAsync()**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#createLocalEducationAgencyAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies | Creates a LocalEducationAgency. |
| [**deleteLocalEducationAgencyAsync()**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#deleteLocalEducationAgencyAsync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Deletes a LocalEducationAgency. |
| [**getLocalEducationAgencyByIdAsync()**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#getLocalEducationAgencyByIdAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Retrieves a LocalEducationAgency by ID. |
| [**getlLocalEducationAgenciesAsync()**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#getlLocalEducationAgenciesAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies | Retrieves a list of LocalEducationAgencies. |
| [**syncLocalEducationAgencyAsync()**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#syncLocalEducationAgencyAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId}/sync | Copies a LocalEducationAgency from one instance to another/other instance(s). |
| [**updateLocalEducationAgencyAsync()**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#updateLocalEducationAgencyAsync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Updates a LocalEducationAgency. |


## `createLocalEducationAgencyAsync()`

```php
createLocalEducationAgencyAsync($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse
```

Creates a LocalEducationAgency.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsLocalEducationAgenciesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$edfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest | 

try {
    $result = $apiInstance->createLocalEducationAgencyAsync($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi->createLocalEducationAgencyAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **edfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest**](../Model/EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse**](../Model/EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteLocalEducationAgencyAsync()`

```php
deleteLocalEducationAgencyAsync($tenantId, $instanceId, $year, $localEducationAgencyId)
```

Deletes a LocalEducationAgency.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsLocalEducationAgenciesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$localEducationAgencyId = 'localEducationAgencyId_example'; // string | 

try {
    $apiInstance->deleteLocalEducationAgencyAsync($tenantId, $instanceId, $year, $localEducationAgencyId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi->deleteLocalEducationAgencyAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **localEducationAgencyId** | **string**|  | |

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

## `getLocalEducationAgencyByIdAsync()`

```php
getLocalEducationAgencyByIdAsync($tenantId, $instanceId, $year, $localEducationAgencyId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse
```

Retrieves a LocalEducationAgency by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsLocalEducationAgenciesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$localEducationAgencyId = 'localEducationAgencyId_example'; // string | 

try {
    $result = $apiInstance->getLocalEducationAgencyByIdAsync($tenantId, $instanceId, $year, $localEducationAgencyId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi->getLocalEducationAgencyByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **localEducationAgencyId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse**](../Model/EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getlLocalEducationAgenciesAsync()`

```php
getlLocalEducationAgenciesAsync($tenantId, $instanceId, $year, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel
```

Retrieves a list of LocalEducationAgencies.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsLocalEducationAgenciesApi(
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
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getlLocalEducationAgenciesAsync($tenantId, $instanceId, $year, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi->getlLocalEducationAgenciesAsync: ', $e->getMessage(), PHP_EOL;
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
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel**](../Model/EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `syncLocalEducationAgencyAsync()`

```php
syncLocalEducationAgencyAsync($tenantId, $instanceId, $year, $localEducationAgencyId, $edfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncResponse
```

Copies a LocalEducationAgency from one instance to another/other instance(s).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsLocalEducationAgenciesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$localEducationAgencyId = 56; // int | 
$edfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest | 

try {
    $result = $apiInstance->syncLocalEducationAgencyAsync($tenantId, $instanceId, $year, $localEducationAgencyId, $edfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi->syncLocalEducationAgencyAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **localEducationAgencyId** | **int**|  | |
| **edfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest**](../Model/EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncResponse**](../Model/EdfiAdminApiEdfiAdminV1SyncResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateLocalEducationAgencyAsync()`

```php
updateLocalEducationAgencyAsync($tenantId, $instanceId, $year, $localEducationAgencyId, $edfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest)
```

Updates a LocalEducationAgency.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsLocalEducationAgenciesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$localEducationAgencyId = 'localEducationAgencyId_example'; // string | 
$edfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest | 

try {
    $apiInstance->updateLocalEducationAgencyAsync($tenantId, $instanceId, $year, $localEducationAgencyId, $edfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi->updateLocalEducationAgencyAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **localEducationAgencyId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest**](../Model/EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest.md)|  | [optional] |

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
