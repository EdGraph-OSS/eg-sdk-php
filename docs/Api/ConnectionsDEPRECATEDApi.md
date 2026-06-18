# EdGraph\PlatformClient\ConnectionsDEPRECATEDApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createStateReportingConnectionV1()**](ConnectionsDEPRECATEDApi.md#createStateReportingConnectionV1) | **POST** /tenants/{tenantId}/statereporting/connections | Creates a new Connection. |
| [**deleteStateReportingConnectionV1()**](ConnectionsDEPRECATEDApi.md#deleteStateReportingConnectionV1) | **DELETE** /tenants/{tenantId}/statereporting/connections/{connectionId} | Deletes a Connection. |
| [**findStateReportingConnectionsV1()**](ConnectionsDEPRECATEDApi.md#findStateReportingConnectionsV1) | **GET** /tenants/{tenantId}/statereporting/connections | Retrieves a list of Connections. |
| [**getStateReportingConnectionV1()**](ConnectionsDEPRECATEDApi.md#getStateReportingConnectionV1) | **GET** /tenants/{tenantId}/statereporting/connections/{connectionId} | Retrieves a Connection by ID. |
| [**testStateReportingConnectionByIdV1()**](ConnectionsDEPRECATEDApi.md#testStateReportingConnectionByIdV1) | **POST** /tenants/{tenantId}/statereporting/connections/{connectionId}/testconnection | Tests a Connection by ID. |
| [**testStateReportingConnectionByTypeV1()**](ConnectionsDEPRECATEDApi.md#testStateReportingConnectionByTypeV1) | **POST** /tenants/{tenantId}/statereporting/connections/testconnection | Tests a Connection by Type. |
| [**updateStateReportingConnectionV1()**](ConnectionsDEPRECATEDApi.md#updateStateReportingConnectionV1) | **PUT** /tenants/{tenantId}/statereporting/connections/{connectionId} | Updates a Connection. |


## `createStateReportingConnectionV1()`

```php
createStateReportingConnectionV1($tenantId, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse
```

Creates a new Connection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsDEPRECATEDApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest | 

try {
    $result = $apiInstance->createStateReportingConnectionV1($tenantId, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsDEPRECATEDApi->createStateReportingConnectionV1: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
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

## `deleteStateReportingConnectionV1()`

```php
deleteStateReportingConnectionV1($tenantId, $connectionId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse
```

Deletes a Connection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsDEPRECATEDApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->deleteStateReportingConnectionV1($tenantId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsDEPRECATEDApi->deleteStateReportingConnectionV1: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
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

## `findStateReportingConnectionsV1()`

```php
findStateReportingConnectionsV1($tenantId, $instanceType, $connectionType): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse
```

Retrieves a list of Connections.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsDEPRECATEDApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceType = 'instanceType_example'; // string | 
$connectionType = 'connectionType_example'; // string | 

try {
    $result = $apiInstance->findStateReportingConnectionsV1($tenantId, $instanceType, $connectionType);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsDEPRECATEDApi->findStateReportingConnectionsV1: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
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

## `getStateReportingConnectionV1()`

```php
getStateReportingConnectionV1($tenantId, $connectionId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse
```

Retrieves a Connection by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsDEPRECATEDApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->getStateReportingConnectionV1($tenantId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsDEPRECATEDApi->getStateReportingConnectionV1: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
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

## `testStateReportingConnectionByIdV1()`

```php
testStateReportingConnectionByIdV1($tenantId, $connectionId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse
```

Tests a Connection by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsDEPRECATEDApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->testStateReportingConnectionByIdV1($tenantId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsDEPRECATEDApi->testStateReportingConnectionByIdV1: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
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

## `testStateReportingConnectionByTypeV1()`

```php
testStateReportingConnectionByTypeV1($tenantId, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse
```

Tests a Connection by Type.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsDEPRECATEDApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest | 

try {
    $result = $apiInstance->testStateReportingConnectionByTypeV1($tenantId, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsDEPRECATEDApi->testStateReportingConnectionByTypeV1: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
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

## `updateStateReportingConnectionV1()`

```php
updateStateReportingConnectionV1($tenantId, $connectionId, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse
```

Updates a Connection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsDEPRECATEDApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest | 

try {
    $result = $apiInstance->updateStateReportingConnectionV1($tenantId, $connectionId, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsDEPRECATEDApi->updateStateReportingConnectionV1: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
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
