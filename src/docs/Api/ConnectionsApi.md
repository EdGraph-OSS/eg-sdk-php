# EdGraph\PlatformClient\ConnectionsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**connectionTestedResponse()**](ConnectionsApi.md#connectionTestedResponse) | **POST** /tenants/{tenantId}/datasync/connections/testconnection | Tests availability of provided connection metadata. |
| [**createEdFiConnection()**](ConnectionsApi.md#createEdFiConnection) | **POST** /tenants/{tenantId}/edfiadmin/connections | Creates a new Ed-Fi Connection. |
| [**createTenantDataSyncConnection()**](ConnectionsApi.md#createTenantDataSyncConnection) | **POST** /tenants/{tenantId}/datasync/connections | Creates a new DataSync connection |
| [**deleteEdFiConnection()**](ConnectionsApi.md#deleteEdFiConnection) | **DELETE** /tenants/{tenantId}/edfiadmin/connections/{connectionId} | Deletes an Ed-Fi Connection. |
| [**deleteTenantDataSyncConnection()**](ConnectionsApi.md#deleteTenantDataSyncConnection) | **DELETE** /tenants/{tenantId}/datasync/connections/{connectionId} | Delete a DataSync connection matching the primary key |
| [**getAllTenantDataSyncConnections()**](ConnectionsApi.md#getAllTenantDataSyncConnections) | **GET** /tenants/{tenantId}/datasync/connections | Retrieves a list of DataSync Connections |
| [**getConnectionById()**](ConnectionsApi.md#getConnectionById) | **GET** /tenants/{tenantId}/oneroster/connections/{connectionId} | Retrieves the profile of a Connection. |
| [**getEdFiConnectionById()**](ConnectionsApi.md#getEdFiConnectionById) | **GET** /tenants/{tenantId}/edfiadmin/connections/{connectionId} | Retrieves an Ed-Fi Connection by ID. |
| [**getEdFiConnectionsAsync()**](ConnectionsApi.md#getEdFiConnectionsAsync) | **GET** /tenants/{tenantId}/edfiadmin/connections | Retrieves a list of Ed-Fi Connections. |
| [**getEdFiOdsBackupCodesDescriptorsAsync()**](ConnectionsApi.md#getEdFiOdsBackupCodesDescriptorsAsync) | **GET** /tenants/{tenantId}/edfiadmin/connections/odsbackupcodes | Retrieves a list of Ed-Fi ODS backup codes. |
| [**getPagedConnections()**](ConnectionsApi.md#getPagedConnections) | **GET** /tenants/{tenantId}/oneroster/connections | Retrieves a list of Connections. |
| [**getTenantDataSyncConnectionProfileById()**](ConnectionsApi.md#getTenantDataSyncConnectionProfileById) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId} | Retrieves a specific DataSync connection using its primary key |
| [**testConnectionDetailsAsync()**](ConnectionsApi.md#testConnectionDetailsAsync) | **POST** /tenants/{tenantId}/oneroster/connections/test | Tests the connection by sending the connection details in the request payload |
| [**testConnectionDetailsByIdAsync()**](ConnectionsApi.md#testConnectionDetailsByIdAsync) | **POST** /tenants/{tenantId}/oneroster/connections/{connectionId}/test | Tests the connection by obtaining the details by ID |
| [**updateEdFiConnection()**](ConnectionsApi.md#updateEdFiConnection) | **PUT** /tenants/{tenantId}/edfiadmin/connections/{connectionId} | Updates an Ed-Fi Connection. |
| [**updateTenantDataSyncConnection()**](ConnectionsApi.md#updateTenantDataSyncConnection) | **PUT** /tenants/{tenantId}/datasync/connections/{connectionId} | Updates a DataSync connection matching the primary key |


## `connectionTestedResponse()`

```php
connectionTestedResponse($tenantId, $dataSyncApiConnectionV1TestConnectionRequest): \EdGraph\PlatformClient\Model\DataSyncApiConnectionV1ConnectionTestedResponse
```

Tests availability of provided connection metadata.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$dataSyncApiConnectionV1TestConnectionRequest = new \EdGraph\PlatformClient\Model\DataSyncApiConnectionV1TestConnectionRequest(); // \EdGraph\PlatformClient\Model\DataSyncApiConnectionV1TestConnectionRequest | 

try {
    $result = $apiInstance->connectionTestedResponse($tenantId, $dataSyncApiConnectionV1TestConnectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->connectionTestedResponse: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **dataSyncApiConnectionV1TestConnectionRequest** | [**\EdGraph\PlatformClient\Model\DataSyncApiConnectionV1TestConnectionRequest**](../Model/DataSyncApiConnectionV1TestConnectionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiConnectionV1ConnectionTestedResponse**](../Model/DataSyncApiConnectionV1ConnectionTestedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createEdFiConnection()`

```php
createEdFiConnection($tenantId, $edfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest)
```

Creates a new Ed-Fi Connection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest | 

try {
    $apiInstance->createEdFiConnection($tenantId, $edfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->createEdFiConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest**](../Model/EdfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest.md)|  | [optional] |

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

## `createTenantDataSyncConnection()`

```php
createTenantDataSyncConnection($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest)
```

Creates a new DataSync connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest | 

try {
    $apiInstance->createTenantDataSyncConnection($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->createTenantDataSyncConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest.md)|  | [optional] |

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

## `deleteEdFiConnection()`

```php
deleteEdFiConnection($tenantId, $connectionId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiConnectionDeletedResponse
```

Deletes an Ed-Fi Connection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->deleteEdFiConnection($tenantId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->deleteEdFiConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiConnectionDeletedResponse**](../Model/EdfiAdminApiEdfiAdminV1EdFiConnectionDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteTenantDataSyncConnection()`

```php
deleteTenantDataSyncConnection($tenantId, $connectionId)
```

Delete a DataSync connection matching the primary key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $apiInstance->deleteTenantDataSyncConnection($tenantId, $connectionId);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->deleteTenantDataSyncConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |

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

## `getAllTenantDataSyncConnections()`

```php
getAllTenantDataSyncConnections($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\DataSyncApiConnectionV1ConnectionListResponsePaginatedItemsViewModel
```

Retrieves a list of DataSync Connections

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getAllTenantDataSyncConnections($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->getAllTenantDataSyncConnections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiConnectionV1ConnectionListResponsePaginatedItemsViewModel**](../Model/DataSyncApiConnectionV1ConnectionListResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getConnectionById()`

```php
getConnectionById($tenantId, $connectionId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsPagedConnectionsResponse
```

Retrieves the profile of a Connection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getConnectionById($tenantId, $connectionId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->getConnectionById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsPagedConnectionsResponse**](../Model/IMSAdminApiV1ConnectionsPagedConnectionsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEdFiConnectionById()`

```php
getEdFiConnectionById($tenantId, $connectionId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiConnection
```

Retrieves an Ed-Fi Connection by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->getEdFiConnectionById($tenantId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->getEdFiConnectionById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiConnection**](../Model/EdfiAdminApiEdfiAdminV1EdFiConnection.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEdFiConnectionsAsync()`

```php
getEdFiConnectionsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiConnectionPaginatedItemsResponse
```

Retrieves a list of Ed-Fi Connections.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getEdFiConnectionsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->getEdFiConnectionsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiConnectionPaginatedItemsResponse**](../Model/EdfiAdminApiEdfiAdminV1EdFiConnectionPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEdFiOdsBackupCodesDescriptorsAsync()`

```php
getEdFiOdsBackupCodesDescriptorsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptorsPaginatedItemsResponse
```

Retrieves a list of Ed-Fi ODS backup codes.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getEdFiOdsBackupCodesDescriptorsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->getEdFiOdsBackupCodesDescriptorsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptorsPaginatedItemsResponse**](../Model/EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptorsPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPagedConnections()`

```php
getPagedConnections($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsPagedConnectionsResponse
```

Retrieves a list of Connections.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getPagedConnections($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->getPagedConnections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsPagedConnectionsResponse**](../Model/IMSAdminApiV1ConnectionsPagedConnectionsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantDataSyncConnectionProfileById()`

```php
getTenantDataSyncConnectionProfileById($tenantId, $connectionId): \EdGraph\PlatformClient\Model\DataSyncApiConnectionV1ConnectionProfileResponse
```

Retrieves a specific DataSync connection using its primary key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->getTenantDataSyncConnectionProfileById($tenantId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->getTenantDataSyncConnectionProfileById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\DataSyncApiConnectionV1ConnectionProfileResponse**](../Model/DataSyncApiConnectionV1ConnectionProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `testConnectionDetailsAsync()`

```php
testConnectionDetailsAsync($tenantId, $iMSAdminApiV1ConnectionsTestConnectionDetailsRequest): \EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsConnectionTestedResponse
```

Tests the connection by sending the connection details in the request payload

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$iMSAdminApiV1ConnectionsTestConnectionDetailsRequest = new \EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsTestConnectionDetailsRequest(); // \EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsTestConnectionDetailsRequest | 

try {
    $result = $apiInstance->testConnectionDetailsAsync($tenantId, $iMSAdminApiV1ConnectionsTestConnectionDetailsRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->testConnectionDetailsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **iMSAdminApiV1ConnectionsTestConnectionDetailsRequest** | [**\EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsTestConnectionDetailsRequest**](../Model/IMSAdminApiV1ConnectionsTestConnectionDetailsRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsConnectionTestedResponse**](../Model/IMSAdminApiV1ConnectionsConnectionTestedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `testConnectionDetailsByIdAsync()`

```php
testConnectionDetailsByIdAsync($tenantId, $connectionId, $iMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest): \EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsConnectionTestedResponse
```

Tests the connection by obtaining the details by ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 
$iMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest = new \EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest(); // \EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest | 

try {
    $result = $apiInstance->testConnectionDetailsByIdAsync($tenantId, $connectionId, $iMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->testConnectionDetailsByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |
| **iMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest** | [**\EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest**](../Model/IMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsConnectionTestedResponse**](../Model/IMSAdminApiV1ConnectionsConnectionTestedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateEdFiConnection()`

```php
updateEdFiConnection($tenantId, $connectionId, $edfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiConnectionUpdatedResponse
```

Updates an Ed-Fi Connection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 
$edfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest | 

try {
    $result = $apiInstance->updateEdFiConnection($tenantId, $connectionId, $edfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->updateEdFiConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest**](../Model/EdfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiConnectionUpdatedResponse**](../Model/EdfiAdminApiEdfiAdminV1EdFiConnectionUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTenantDataSyncConnection()`

```php
updateTenantDataSyncConnection($tenantId, $connectionId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest)
```

Updates a DataSync connection matching the primary key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest | 

try {
    $apiInstance->updateTenantDataSyncConnection($tenantId, $connectionId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->updateTenantDataSyncConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest.md)|  | [optional] |

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
