# EdGraph\PlatformClient\InstancesInstanceApplicationsAPIClientsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createInstanceApiClient()**](InstancesInstanceApplicationsAPIClientsApi.md#createInstanceApiClient) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients | Creates an Instance ApiClient |
| [**deleteInstanceApiClient()**](InstancesInstanceApplicationsAPIClientsApi.md#deleteInstanceApiClient) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Deletes an Instance ApiClient |
| [**getInstanceApiClientById()**](InstancesInstanceApplicationsAPIClientsApi.md#getInstanceApiClientById) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Retrieves an Instance ApiClient by ID. |
| [**getInstanceApiClients()**](InstancesInstanceApplicationsAPIClientsApi.md#getInstanceApiClients) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients | Retrieves a paginated list of Instance ApiClients |
| [**updateInstanceApiClient()**](InstancesInstanceApplicationsAPIClientsApi.md#updateInstanceApiClient) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Updates an Instance Application ApiClient |


## `createInstanceApiClient()`

```php
createInstanceApiClient($tenantId, $instanceId, $applicationId, $edfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse
```

Creates an Instance ApiClient

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesInstanceApplicationsAPIClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 
$edfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest | 

try {
    $result = $apiInstance->createInstanceApiClient($tenantId, $instanceId, $applicationId, $edfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesInstanceApplicationsAPIClientsApi->createInstanceApiClient: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest**](../Model/EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse**](../Model/EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteInstanceApiClient()`

```php
deleteInstanceApiClient($tenantId, $instanceId, $applicationId, $apiClientId)
```

Deletes an Instance ApiClient

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesInstanceApplicationsAPIClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 
$apiClientId = 'apiClientId_example'; // string | 

try {
    $apiInstance->deleteInstanceApiClient($tenantId, $instanceId, $applicationId, $apiClientId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesInstanceApplicationsAPIClientsApi->deleteInstanceApiClient: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |
| **apiClientId** | **string**|  | |

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

## `getInstanceApiClientById()`

```php
getInstanceApiClientById($tenantId, $instanceId, $applicationId, $apiClientId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse
```

Retrieves an Instance ApiClient by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesInstanceApplicationsAPIClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 
$apiClientId = 'apiClientId_example'; // string | 

try {
    $result = $apiInstance->getInstanceApiClientById($tenantId, $instanceId, $applicationId, $apiClientId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesInstanceApplicationsAPIClientsApi->getInstanceApiClientById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |
| **apiClientId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse**](../Model/EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInstanceApiClients()`

```php
getInstanceApiClients($tenantId, $instanceId, $applicationId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel
```

Retrieves a paginated list of Instance ApiClients

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesInstanceApplicationsAPIClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getInstanceApiClients($tenantId, $instanceId, $applicationId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesInstanceApplicationsAPIClientsApi->getInstanceApiClients: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel**](../Model/EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateInstanceApiClient()`

```php
updateInstanceApiClient($tenantId, $instanceId, $applicationId, $apiClientId, $edfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse
```

Updates an Instance Application ApiClient

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesInstanceApplicationsAPIClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 
$apiClientId = 'apiClientId_example'; // string | 
$edfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest | 

try {
    $result = $apiInstance->updateInstanceApiClient($tenantId, $instanceId, $applicationId, $apiClientId, $edfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesInstanceApplicationsAPIClientsApi->updateInstanceApiClient: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |
| **apiClientId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest**](../Model/EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse**](../Model/EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
