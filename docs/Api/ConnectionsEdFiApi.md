# EdGraph\PlatformClient\ConnectionsEdFiApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getTenantDataSyncConnectionEdFiDistricts()**](ConnectionsEdFiApi.md#getTenantDataSyncConnectionEdFiDistricts) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/districts | Retrieves a list of districts from an Ed-Fi API using the DataSync connection metadata |
| [**getTenantDataSyncConnectionEdFiEducationOrganizationIdDescriptors()**](ConnectionsEdFiApi.md#getTenantDataSyncConnectionEdFiEducationOrganizationIdDescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/educationorganizationidentificationsystemdescriptors | Retrieves a list of education organization identification system descriptors from an Ed-Fi API using the DataSync connection metadata |
| [**getTenantDataSyncConnectionEdFiSchoolYears()**](ConnectionsEdFiApi.md#getTenantDataSyncConnectionEdFiSchoolYears) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/schoolyears | Retrieves a list of school years from an Ed-Fi API using the DataSync connection metadata |
| [**getTenantDataSyncConnectionEdFiStaffIdDescriptors()**](ConnectionsEdFiApi.md#getTenantDataSyncConnectionEdFiStaffIdDescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/staffidentificationsystemdescriptors | Retrieves a list of staff identification system descriptors from an Ed-Fi API using the DataSync connection metadata |
| [**getTenantDataSyncConnectionEdFiStudentIdDescriptors()**](ConnectionsEdFiApi.md#getTenantDataSyncConnectionEdFiStudentIdDescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/studentidentificationsystemdescriptors | Retrieves a list of student identification system descriptors from an Ed-Fi API using the DataSync connection metadata |
| [**getTenantDataSyncConnectionEdFiTermDescriptors()**](ConnectionsEdFiApi.md#getTenantDataSyncConnectionEdFiTermDescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/termdescriptors | Retrieves a list of term descriptors from an Ed-Fi API using the DataSync connection metadata |


## `getTenantDataSyncConnectionEdFiDistricts()`

```php
getTenantDataSyncConnectionEdFiDistricts($tenantId, $connectionId): \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse[]
```

Retrieves a list of districts from an Ed-Fi API using the DataSync connection metadata

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsEdFiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->getTenantDataSyncConnectionEdFiDistricts($tenantId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsEdFiApi->getTenantDataSyncConnectionEdFiDistricts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse[]**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantDataSyncConnectionEdFiEducationOrganizationIdDescriptors()`

```php
getTenantDataSyncConnectionEdFiEducationOrganizationIdDescriptors($tenantId, $connectionId): \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse[]
```

Retrieves a list of education organization identification system descriptors from an Ed-Fi API using the DataSync connection metadata

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsEdFiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->getTenantDataSyncConnectionEdFiEducationOrganizationIdDescriptors($tenantId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsEdFiApi->getTenantDataSyncConnectionEdFiEducationOrganizationIdDescriptors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse[]**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantDataSyncConnectionEdFiSchoolYears()`

```php
getTenantDataSyncConnectionEdFiSchoolYears($tenantId, $connectionId): \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse[]
```

Retrieves a list of school years from an Ed-Fi API using the DataSync connection metadata

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsEdFiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->getTenantDataSyncConnectionEdFiSchoolYears($tenantId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsEdFiApi->getTenantDataSyncConnectionEdFiSchoolYears: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse[]**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantDataSyncConnectionEdFiStaffIdDescriptors()`

```php
getTenantDataSyncConnectionEdFiStaffIdDescriptors($tenantId, $connectionId): \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse[]
```

Retrieves a list of staff identification system descriptors from an Ed-Fi API using the DataSync connection metadata

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsEdFiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->getTenantDataSyncConnectionEdFiStaffIdDescriptors($tenantId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsEdFiApi->getTenantDataSyncConnectionEdFiStaffIdDescriptors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse[]**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantDataSyncConnectionEdFiStudentIdDescriptors()`

```php
getTenantDataSyncConnectionEdFiStudentIdDescriptors($tenantId, $connectionId): \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse[]
```

Retrieves a list of student identification system descriptors from an Ed-Fi API using the DataSync connection metadata

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsEdFiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->getTenantDataSyncConnectionEdFiStudentIdDescriptors($tenantId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsEdFiApi->getTenantDataSyncConnectionEdFiStudentIdDescriptors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse[]**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantDataSyncConnectionEdFiTermDescriptors()`

```php
getTenantDataSyncConnectionEdFiTermDescriptors($tenantId, $connectionId): \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse[]
```

Retrieves a list of term descriptors from an Ed-Fi API using the DataSync connection metadata

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConnectionsEdFiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$connectionId = 'connectionId_example'; // string | 

try {
    $result = $apiInstance->getTenantDataSyncConnectionEdFiTermDescriptors($tenantId, $connectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsEdFiApi->getTenantDataSyncConnectionEdFiTermDescriptors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **connectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse[]**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
