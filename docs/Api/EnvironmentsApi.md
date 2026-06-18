# EdGraph\PlatformClient\EnvironmentsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createEnvironment()**](EnvironmentsApi.md#createEnvironment) | **POST** /tenants/{tenantId}/validations/environments | Creates an Environment. |
| [**createStateReportingEnvironment()**](EnvironmentsApi.md#createStateReportingEnvironment) | **POST** /tenants/{tenantId}/statereporting/environments | Creates a new Environment. |
| [**deleteEnvironment()**](EnvironmentsApi.md#deleteEnvironment) | **DELETE** /tenants/{tenantId}/validations/environments/{environmentId} | Deletes an Environment. |
| [**deleteStateReportingEnvironment()**](EnvironmentsApi.md#deleteStateReportingEnvironment) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId} | Deletes an Environment. |
| [**getEnvironmentById()**](EnvironmentsApi.md#getEnvironmentById) | **GET** /tenants/{tenantId}/validations/environments/{environmentId} | Retrieves an Environment by ID. |
| [**getEnvironments()**](EnvironmentsApi.md#getEnvironments) | **GET** /tenants/{tenantId}/validations/environments | Retrieves a list of Environments. |
| [**getStateReportingEnvironment()**](EnvironmentsApi.md#getStateReportingEnvironment) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId} | Retrieves an Environment by ID. |
| [**searchStateReportingEnvironments()**](EnvironmentsApi.md#searchStateReportingEnvironments) | **GET** /tenants/{tenantId}/statereporting/environments | Retrieves a list of Environments. |
| [**testEnvironmentConnection()**](EnvironmentsApi.md#testEnvironmentConnection) | **POST** /tenants/{tenantId}/validations/environments/testconnection | Tests if the provided connection string can establish a valid connection. |
| [**updateEnvironment()**](EnvironmentsApi.md#updateEnvironment) | **PUT** /tenants/{tenantId}/validations/environments/{environmentId} | Updates an Environment. |
| [**updateStateReportingEnvironment()**](EnvironmentsApi.md#updateStateReportingEnvironment) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId} | Updates an Environment. |


## `createEnvironment()`

```php
createEnvironment($tenantId, $validationsApiDbEnvironmentsV1CreateRequest): \EdGraph\PlatformClient\Model\ValidationsApiCoreV1CreatedResponse
```

Creates an Environment.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$validationsApiDbEnvironmentsV1CreateRequest = new \EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1CreateRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1CreateRequest | 

try {
    $result = $apiInstance->createEnvironment($tenantId, $validationsApiDbEnvironmentsV1CreateRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsApi->createEnvironment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **validationsApiDbEnvironmentsV1CreateRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1CreateRequest**](../Model/ValidationsApiDbEnvironmentsV1CreateRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiCoreV1CreatedResponse**](../Model/ValidationsApiCoreV1CreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createStateReportingEnvironment()`

```php
createStateReportingEnvironment($tenantId, $edGraphServicesStateReportingV1CreateEnvironmentRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1EnvironmentCreatedResponse
```

Creates a new Environment.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphServicesStateReportingV1CreateEnvironmentRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1CreateEnvironmentRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1CreateEnvironmentRequest | 

try {
    $result = $apiInstance->createStateReportingEnvironment($tenantId, $edGraphServicesStateReportingV1CreateEnvironmentRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsApi->createStateReportingEnvironment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphServicesStateReportingV1CreateEnvironmentRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1CreateEnvironmentRequest**](../Model/EdGraphServicesStateReportingV1CreateEnvironmentRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1EnvironmentCreatedResponse**](../Model/EdGraphServicesStateReportingV1EnvironmentCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteEnvironment()`

```php
deleteEnvironment($tenantId, $environmentId)
```

Deletes an Environment.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 

try {
    $apiInstance->deleteEnvironment($tenantId, $environmentId);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsApi->deleteEnvironment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |

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

## `deleteStateReportingEnvironment()`

```php
deleteStateReportingEnvironment($tenantId, $environmentId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1EnvironmentDeletedResponse
```

Deletes an Environment.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 

try {
    $result = $apiInstance->deleteStateReportingEnvironment($tenantId, $environmentId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsApi->deleteStateReportingEnvironment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1EnvironmentDeletedResponse**](../Model/EdGraphServicesStateReportingV1EnvironmentDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEnvironmentById()`

```php
getEnvironmentById($tenantId, $environmentId): \EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1DbEnvironmentDto
```

Retrieves an Environment by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 

try {
    $result = $apiInstance->getEnvironmentById($tenantId, $environmentId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsApi->getEnvironmentById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1DbEnvironmentDto**](../Model/ValidationsApiDbEnvironmentsV1DbEnvironmentDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEnvironments()`

```php
getEnvironments($tenantId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments
```

Retrieves a list of Environments.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$filter = 'filter_example'; // string | 
$orderBy = 'orderBy_example'; // string | 

try {
    $result = $apiInstance->getEnvironments($tenantId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsApi->getEnvironments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] |
| **orderBy** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments**](../Model/ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStateReportingEnvironment()`

```php
getStateReportingEnvironment($tenantId, $environmentId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1EnvironmentProfileResponse
```

Retrieves an Environment by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 

try {
    $result = $apiInstance->getStateReportingEnvironment($tenantId, $environmentId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsApi->getStateReportingEnvironment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1EnvironmentProfileResponse**](../Model/EdGraphServicesStateReportingV1EnvironmentProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchStateReportingEnvironments()`

```php
searchStateReportingEnvironments($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedEnvironmentsResponse
```

Retrieves a list of Environments.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = 'orderBy_example'; // string | 
$filter = 'filter_example'; // string | 

try {
    $result = $apiInstance->searchStateReportingEnvironments($tenantId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsApi->searchStateReportingEnvironments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] |
| **filter** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedEnvironmentsResponse**](../Model/EdGraphServicesStateReportingV1PaginatedEnvironmentsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `testEnvironmentConnection()`

```php
testEnvironmentConnection($tenantId, $validationsApiDbEnvironmentsV1TestConnectionRequest): \EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1TestConnectionResponse
```

Tests if the provided connection string can establish a valid connection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$validationsApiDbEnvironmentsV1TestConnectionRequest = new \EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1TestConnectionRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1TestConnectionRequest | 

try {
    $result = $apiInstance->testEnvironmentConnection($tenantId, $validationsApiDbEnvironmentsV1TestConnectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsApi->testEnvironmentConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **validationsApiDbEnvironmentsV1TestConnectionRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1TestConnectionRequest**](../Model/ValidationsApiDbEnvironmentsV1TestConnectionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1TestConnectionResponse**](../Model/ValidationsApiDbEnvironmentsV1TestConnectionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateEnvironment()`

```php
updateEnvironment($tenantId, $environmentId, $validationsApiDbEnvironmentsV1UpdateRequest): object
```

Updates an Environment.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$validationsApiDbEnvironmentsV1UpdateRequest = new \EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1UpdateRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1UpdateRequest | 

try {
    $result = $apiInstance->updateEnvironment($tenantId, $environmentId, $validationsApiDbEnvironmentsV1UpdateRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsApi->updateEnvironment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **validationsApiDbEnvironmentsV1UpdateRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiDbEnvironmentsV1UpdateRequest**](../Model/ValidationsApiDbEnvironmentsV1UpdateRequest.md)|  | [optional] |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateStateReportingEnvironment()`

```php
updateStateReportingEnvironment($tenantId, $environmentId, $edGraphServicesStateReportingV1UpdateEnvironmentRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1EnvironmentUpdatedResponse
```

Updates an Environment.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$edGraphServicesStateReportingV1UpdateEnvironmentRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1UpdateEnvironmentRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1UpdateEnvironmentRequest | 

try {
    $result = $apiInstance->updateStateReportingEnvironment($tenantId, $environmentId, $edGraphServicesStateReportingV1UpdateEnvironmentRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsApi->updateStateReportingEnvironment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **edGraphServicesStateReportingV1UpdateEnvironmentRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1UpdateEnvironmentRequest**](../Model/EdGraphServicesStateReportingV1UpdateEnvironmentRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1EnvironmentUpdatedResponse**](../Model/EdGraphServicesStateReportingV1EnvironmentUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
