# EdGraph\PlatformClient\InstancesClientsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createClient()**](InstancesClientsApi.md#createClient) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients | Creates a new client |
| [**deleteClient()**](InstancesClientsApi.md#deleteClient) | **DELETE** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Deletes a client by Id |
| [**getClientById()**](InstancesClientsApi.md#getClientById) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Retrieves a client by Id |
| [**getPagedClients()**](InstancesClientsApi.md#getPagedClients) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients | Retrieves a list of clients for a given instance |
| [**updateClient()**](InstancesClientsApi.md#updateClient) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Updates a client by Id |


## `createClient()`

```php
createClient($tenantId, $instanceId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto): \EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsClientCreatedResponse
```

Creates a new client

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto | 

try {
    $result = $apiInstance->createClient($tenantId, $instanceId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesClientsApi->createClient: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsClientCreatedResponse**](../Model/IMSAdminApiV1ClientsClientCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteClient()`

```php
deleteClient($tenantId, $instanceId, $clientId): \EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsClientDeletedResponse
```

Deletes a client by Id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$clientId = 'clientId_example'; // string | 

try {
    $result = $apiInstance->deleteClient($tenantId, $instanceId, $clientId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesClientsApi->deleteClient: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **clientId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsClientDeletedResponse**](../Model/IMSAdminApiV1ClientsClientDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getClientById()`

```php
getClientById($tenantId, $instanceId, $clientId): \EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsClientProfileResponse
```

Retrieves a client by Id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$clientId = 'clientId_example'; // string | 

try {
    $result = $apiInstance->getClientById($tenantId, $instanceId, $clientId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesClientsApi->getClientById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **clientId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsClientProfileResponse**](../Model/IMSAdminApiV1ClientsClientProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPagedClients()`

```php
getPagedClients($tenantId, $instanceId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsPaginatedItemsResponse
```

Retrieves a list of clients for a given instance

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$pageSize = 10; // int
$pageIndex = 0; // int
$orderBy = ''; // string
$filter = ''; // string

try {
    $result = $apiInstance->getPagedClients($tenantId, $instanceId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesClientsApi->getPagedClients: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsPaginatedItemsResponse**](../Model/IMSAdminApiV1ClientsPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateClient()`

```php
updateClient($tenantId, $instanceId, $clientId, $iMSAdminApiV1ClientsUpdateClientRequest): \EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsClientUpdatedResponse
```

Updates a client by Id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$clientId = 'clientId_example'; // string | 
$iMSAdminApiV1ClientsUpdateClientRequest = new \EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsUpdateClientRequest(); // \EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsUpdateClientRequest

try {
    $result = $apiInstance->updateClient($tenantId, $instanceId, $clientId, $iMSAdminApiV1ClientsUpdateClientRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesClientsApi->updateClient: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **clientId** | **string**|  | |
| **iMSAdminApiV1ClientsUpdateClientRequest** | [**\EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsUpdateClientRequest**](../Model/IMSAdminApiV1ClientsUpdateClientRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsClientUpdatedResponse**](../Model/IMSAdminApiV1ClientsClientUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
