# EdGraph\PlatformClient\EnvironmentsConnectionsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createStateReportingConnection()**](EnvironmentsConnectionsApi.md#createStateReportingConnection) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections | Creates a new Connection. |
| [**deleteStateReportingConnection()**](EnvironmentsConnectionsApi.md#deleteStateReportingConnection) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId} | Deletes a Connection. |
| [**findStateReportingConnections()**](EnvironmentsConnectionsApi.md#findStateReportingConnections) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections | Retrieves a list of Connections. |
| [**getStateReportingConnection()**](EnvironmentsConnectionsApi.md#getStateReportingConnection) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId} | Retrieves a Connection by ID. |
| [**testStateReportingConnectionById()**](EnvironmentsConnectionsApi.md#testStateReportingConnectionById) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId}/testconnection | Tests a Connection by ID. |
| [**testStateReportingConnectionByType()**](EnvironmentsConnectionsApi.md#testStateReportingConnectionByType) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/testconnection | Tests a Connection by Type. |
| [**updateStateReportingConnection()**](EnvironmentsConnectionsApi.md#updateStateReportingConnection) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId} | Updates a Connection. |


## `createStateReportingConnection()`

```php
createStateReportingConnection($tenantId, $environmentId, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse
```

Creates a new Connection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest | 

try {
    $result = $apiInstance->createStateReportingConnection($tenantId, $environmentId, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsConnectionsApi->createStateReportingConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteStateReportingConnection()`

```php
deleteStateReportingConnection($tenantId, $environmentId, $connectionId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse
```

Deletes a Connection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->deleteStateReportingConnection($tenantId, $environmentId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsConnectionsApi->deleteStateReportingConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **connectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `findStateReportingConnections()`

```php
findStateReportingConnections($tenantId, $environmentId, $instanceType, $connectionType): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse
```

Retrieves a list of Connections.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$instanceType = 'instanceType_example'; // string | 
$connectionType = 'connectionType_example'; // string | 

try {
    $result = $apiInstance->findStateReportingConnections($tenantId, $environmentId, $instanceType, $connectionType);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsConnectionsApi->findStateReportingConnections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **instanceType** | **string**|  | [optional] |
| **connectionType** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStateReportingConnection()`

```php
getStateReportingConnection($tenantId, $environmentId, $connectionId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse
```

Retrieves a Connection by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->getStateReportingConnection($tenantId, $environmentId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsConnectionsApi->getStateReportingConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **connectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `testStateReportingConnectionById()`

```php
testStateReportingConnectionById($tenantId, $environmentId, $connectionId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse
```

Tests a Connection by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->testStateReportingConnectionById($tenantId, $environmentId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsConnectionsApi->testStateReportingConnectionById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **connectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `testStateReportingConnectionByType()`

```php
testStateReportingConnectionByType($tenantId, $environmentId, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse
```

Tests a Connection by Type.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest | 

try {
    $result = $apiInstance->testStateReportingConnectionByType($tenantId, $environmentId, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsConnectionsApi->testStateReportingConnectionByType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateStateReportingConnection()`

```php
updateStateReportingConnection($tenantId, $environmentId, $connectionId, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse
```

Updates a Connection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest | 

try {
    $result = $apiInstance->updateStateReportingConnection($tenantId, $environmentId, $connectionId, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsConnectionsApi->updateStateReportingConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **connectionId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
