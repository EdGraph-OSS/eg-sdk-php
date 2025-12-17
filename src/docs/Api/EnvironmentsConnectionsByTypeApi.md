# EdGraph\PlatformClient\EnvironmentsConnectionsByTypeApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createOrUpdateStateReportingConnectionByType()**](EnvironmentsConnectionsByTypeApi.md#createOrUpdateStateReportingConnectionByType) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/connectionsByType/{connectionType} | Creates or Update a Connection by ConnectionType. |
| [**deleteStateReportingByTypeConnection()**](EnvironmentsConnectionsByTypeApi.md#deleteStateReportingByTypeConnection) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/connectionsByType/{connectionType} | Deletes a Connection by Type |
| [**getStateReportingConnectionByType()**](EnvironmentsConnectionsByTypeApi.md#getStateReportingConnectionByType) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/connectionsByType/{connectionType} | Retrieves a Connection by Type. |


## `createOrUpdateStateReportingConnectionByType()`

```php
createOrUpdateStateReportingConnectionByType($tenantId, $environmentId, $connectionType, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse
```

Creates or Update a Connection by ConnectionType.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsConnectionsByTypeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$connectionType = 'connectionType_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest | 

try {
    $result = $apiInstance->createOrUpdateStateReportingConnectionByType($tenantId, $environmentId, $connectionType, $edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsConnectionsByTypeApi->createOrUpdateStateReportingConnectionByType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **connectionType** | **string**|  | |
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

## `deleteStateReportingByTypeConnection()`

```php
deleteStateReportingByTypeConnection($tenantId, $environmentId, $connectionType): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse
```

Deletes a Connection by Type

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsConnectionsByTypeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$connectionType = 'connectionType_example'; // string | 

try {
    $result = $apiInstance->deleteStateReportingByTypeConnection($tenantId, $environmentId, $connectionType);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsConnectionsByTypeApi->deleteStateReportingByTypeConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **connectionType** | **string**|  | |

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

## `getStateReportingConnectionByType()`

```php
getStateReportingConnectionByType($tenantId, $environmentId, $connectionType): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse
```

Retrieves a Connection by Type.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsConnectionsByTypeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$connectionType = 'connectionType_example'; // string | 

try {
    $result = $apiInstance->getStateReportingConnectionByType($tenantId, $environmentId, $connectionType);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsConnectionsByTypeApi->getStateReportingConnectionByType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **connectionType** | **string**|  | |

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
