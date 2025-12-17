# EdGraph\PlatformClient\AnalyticsConnectorsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createConnector()**](AnalyticsConnectorsApi.md#createConnector) | **POST** /tenants/{tenantId}/analytics/connectors | Creates a new connector |
| [**deleteConnector()**](AnalyticsConnectorsApi.md#deleteConnector) | **DELETE** /tenants/{tenantId}/analytics/connectors/{connectorId} | Deletes a connector by Id |
| [**getADLSGen2ConnectorById()**](AnalyticsConnectorsApi.md#getADLSGen2ConnectorById) | **GET** /tenants/{tenantId}/analytics/connectors/{connectorId} | Retrieves a connector profile by Id |
| [**getPaginatedConnectors()**](AnalyticsConnectorsApi.md#getPaginatedConnectors) | **GET** /tenants/{tenantId}/analytics/connectors | Retrieves paginated connectors |
| [**updateConnector()**](AnalyticsConnectorsApi.md#updateConnector) | **PUT** /tenants/{tenantId}/analytics/connectors/{connectorId} | Updates a connector by Id |


## `createConnector()`

```php
createConnector($tenantId, $body): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeCreatedResponse
```

Creates a new connector

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\AnalyticsConnectorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$body = NULL; // mixed | 

try {
    $result = $apiInstance->createConnector($tenantId, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnalyticsConnectorsApi->createConnector: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **body** | **mixed**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeCreatedResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteConnector()`

```php
deleteConnector($tenantId, $connectorId): \EdGraph\PlatformClient\Model\AnalyticsApiConnectorsV1ConnectorDeletedResponse
```

Deletes a connector by Id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\AnalyticsConnectorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectorId = 'connectorId_example'; // string | 

try {
    $result = $apiInstance->deleteConnector($tenantId, $connectorId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnalyticsConnectorsApi->deleteConnector: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectorId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiConnectorsV1ConnectorDeletedResponse**](../Model/AnalyticsApiConnectorsV1ConnectorDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getADLSGen2ConnectorById()`

```php
getADLSGen2ConnectorById($tenantId, $connectorId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfileDTO
```

Retrieves a connector profile by Id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\AnalyticsConnectorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectorId = 'connectorId_example'; // string | 

try {
    $result = $apiInstance->getADLSGen2ConnectorById($tenantId, $connectorId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnalyticsConnectorsApi->getADLSGen2ConnectorById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectorId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfileDTO**](../Model/EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfileDTO.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPaginatedConnectors()`

```php
getPaginatedConnectors($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorsPaginatedItemsResponse
```

Retrieves paginated connectors

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\AnalyticsConnectorsApi(
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
    $result = $apiInstance->getPaginatedConnectors($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnalyticsConnectorsApi->getPaginatedConnectors: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorsPaginatedItemsResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorsPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateConnector()`

```php
updateConnector($tenantId, $connectorId, $body): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeUpdatedResponse
```

Updates a connector by Id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\AnalyticsConnectorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectorId = 'connectorId_example'; // string | 
$body = NULL; // mixed | 

try {
    $result = $apiInstance->updateConnector($tenantId, $connectorId, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnalyticsConnectorsApi->updateConnector: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectorId** | **string**|  | |
| **body** | **mixed**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeUpdatedResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
