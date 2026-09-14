# EdGraph\PlatformClient\InstancesApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addRelatedInstances()**](InstancesApi.md#addRelatedInstances) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/relatedinstances | Add related instances to root instance by Id |
| [**addSchoolYear()**](InstancesApi.md#addSchoolYear) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years | Adds an ODS database to an Instance. |
| [**addSchoolYearRange()**](InstancesApi.md#addSchoolYearRange) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/bulk | Adds multiple ODS databases to an instance. |
| [**changeInstanceDatabaseTierAsync()**](InstancesApi.md#changeInstanceDatabaseTierAsync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/tiers | Changes the selected tier of an ODS database. |
| [**cloneInstanceAsync()**](InstancesApi.md#cloneInstanceAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/clone | Clones an instance. |
| [**createInstance()**](InstancesApi.md#createInstance) | **POST** /tenants/{tenantId}/oneroster/instances | Creates a new Instance. |
| [**createInstanceAsync()**](InstancesApi.md#createInstanceAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances | Creates a new Instance. |
| [**createInstanceV2()**](InstancesApi.md#createInstanceV2) | **POST** /v2/tenants/{tenantId}/instances | Creates a new instance. |
| [**deleteInstance()**](InstancesApi.md#deleteInstance) | **DELETE** /tenants/{tenantId}/oneroster/instances/{instanceId} | Deletes an Instance. |
| [**deleteInstanceAsync()**](InstancesApi.md#deleteInstanceAsync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Deletes an Instance. |
| [**deleteInstanceV2()**](InstancesApi.md#deleteInstanceV2) | **DELETE** /v2/tenants/{tenantId}/instances/{instanceId} | Deletes an instance. |
| [**deleteSchoolYearAsync()**](InstancesApi.md#deleteSchoolYearAsync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year} | Removes an ODS database from an Instance. |
| [**getEdFiAdminInstanceEndpoints()**](InstancesApi.md#getEdFiAdminInstanceEndpoints) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/endpoints | Retrieves the Ed-Fi API endpoint URLs of an Instance. |
| [**getEdFiAdminInstanceYearEndpoints()**](InstancesApi.md#getEdFiAdminInstanceYearEndpoints) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/endpoints | Retrieves the Ed-Fi API endpoint URLs of an Instance. |
| [**getInstanceById()**](InstancesApi.md#getInstanceById) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId} | Retrieves an Instance by ID. |
| [**getInstanceByIdAsync()**](InstancesApi.md#getInstanceByIdAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Retrieves an Instance by ID. |
| [**getInstanceCsvExport()**](InstancesApi.md#getInstanceCsvExport) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/csv/export | Retrieves an Instance by ID. |
| [**getInstanceCsvExportV2()**](InstancesApi.md#getInstanceCsvExportV2) | **GET** /v2/tenants/{tenantId}/oneroster/instances/{instanceId}/csv/export | Retrieves a ZIP bundle containing OneRoster Instance Database contents in CSV format |
| [**getInstanceEndpoints()**](InstancesApi.md#getInstanceEndpoints) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/endpoints | Retrieves the One Roster endpoint URLs of an Instance. |
| [**getInstancesAsync()**](InstancesApi.md#getInstancesAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances | Retrieves a list of Instances. |
| [**getPagedInstances()**](InstancesApi.md#getPagedInstances) | **GET** /tenants/{tenantId}/oneroster/instances | Retrieves a list of Instances. |
| [**getTenantInstanceByIdV2()**](InstancesApi.md#getTenantInstanceByIdV2) | **GET** /v2/tenants/{tenantId}/instances/{instanceId} | Get Instance by Id |
| [**getTenantInstancesV2()**](InstancesApi.md#getTenantInstancesV2) | **GET** /v2/tenants/{tenantId}/instances | Get list of all instances for a tenant - V2 |
| [**isInstanceCustomIdAvailable()**](InstancesApi.md#isInstanceCustomIdAvailable) | **GET** /tenants/{tenantId}/oneroster/instances/isinstancecustomidavailable/{customId} | Validate if instance is available |
| [**loadApiMetadata()**](InstancesApi.md#loadApiMetadata) | **POST** /tenants/{tenantId}/edfiadmin/api-metadata | Loads connection metadata. |
| [**resetInstance()**](InstancesApi.md#resetInstance) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/resetinstance | Resets an Instance. |
| [**resetInstanceAsync()**](InstancesApi.md#resetInstanceAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/resetinstance | Resets an Instance. |
| [**resetInstanceCacheAsync()**](InstancesApi.md#resetInstanceCacheAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/resetcache | Resets the cache of an Instance and the specified ODS database. |
| [**resetSchoolYearAsync()**](InstancesApi.md#resetSchoolYearAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/resetods | Resets the ODS database with the specified school year. |
| [**setInstanceIsDefault()**](InstancesApi.md#setInstanceIsDefault) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/default | Updates the isDefault property for an instance |
| [**testConnectionDetailsByInstanceIdAsync()**](InstancesApi.md#testConnectionDetailsByInstanceIdAsync) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/test | Tests the connection by obtaining the details by Instance ID |
| [**testCredentialsConnection()**](InstancesApi.md#testCredentialsConnection) | **POST** /tenants/{tenantId}/edfiadmin/testconnection | Tests availability of provided connection metadata. |
| [**testInstanceConnection()**](InstancesApi.md#testInstanceConnection) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/testconnection | Tests the connection of the Instance. |
| [**testInstanceYearConnection()**](InstancesApi.md#testInstanceYearConnection) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/testconnection | Tests the connection of the Instance. |
| [**truncateInstance()**](InstancesApi.md#truncateInstance) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/truncate | Truncates the Instance&#39;s database |
| [**updateInstance()**](InstancesApi.md#updateInstance) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId} | Updates an Instance. |
| [**updateInstanceAsync()**](InstancesApi.md#updateInstanceAsync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Updates an Instance. |
| [**updateInstanceV2()**](InstancesApi.md#updateInstanceV2) | **PUT** /v2/tenants/{tenantId}/instances/{instanceId} | Updates an existing instance. |
| [**validateCustomIdAvailable()**](InstancesApi.md#validateCustomIdAvailable) | **GET** /tenants/{tenantId}/edfiadmin/instances/validatecustomidavailable/{customId} | Validate if instance is available |


## `addRelatedInstances()`

```php
addRelatedInstances($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1AddRelatedInstancesRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse
```

Add related instances to root instance by Id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1AddRelatedInstancesRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest | 

try {
    $result = $apiInstance->addRelatedInstances($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1AddRelatedInstancesRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->addRelatedInstances: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1AddRelatedInstancesRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest**](../Model/EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse**](../Model/EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `addSchoolYear()`

```php
addSchoolYear($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1AddSchoolYearRequest)
```

Adds an ODS database to an Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1AddSchoolYearRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1AddSchoolYearRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1AddSchoolYearRequest | 

try {
    $apiInstance->addSchoolYear($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1AddSchoolYearRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->addSchoolYear: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1AddSchoolYearRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1AddSchoolYearRequest**](../Model/EdfiAdminApiEdfiAdminV1AddSchoolYearRequest.md)|  | [optional] |

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

## `addSchoolYearRange()`

```php
addSchoolYearRange($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest)
```

Adds multiple ODS databases to an instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest | 

try {
    $apiInstance->addSchoolYearRange($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->addSchoolYearRange: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest**](../Model/EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest.md)|  | [optional] |

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

## `changeInstanceDatabaseTierAsync()`

```php
changeInstanceDatabaseTierAsync($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest)
```

Changes the selected tier of an ODS database.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$edfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest | 

try {
    $apiInstance->changeInstanceDatabaseTierAsync($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->changeInstanceDatabaseTierAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **edfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest**](../Model/EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest.md)|  | [optional] |

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

## `cloneInstanceAsync()`

```php
cloneInstanceAsync($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1CloneInstanceRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CloneInstanceResponse
```

Clones an instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1CloneInstanceRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CloneInstanceRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CloneInstanceRequest | 

try {
    $result = $apiInstance->cloneInstanceAsync($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1CloneInstanceRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->cloneInstanceAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1CloneInstanceRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CloneInstanceRequest**](../Model/EdfiAdminApiEdfiAdminV1CloneInstanceRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CloneInstanceResponse**](../Model/EdfiAdminApiEdfiAdminV1CloneInstanceResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createInstance()`

```php
createInstance($tenantId, $iMSAdminApiV1InstancesCreateInstanceRequest)
```

Creates a new Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$iMSAdminApiV1InstancesCreateInstanceRequest = new \EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesCreateInstanceRequest(); // \EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesCreateInstanceRequest | 

try {
    $apiInstance->createInstance($tenantId, $iMSAdminApiV1InstancesCreateInstanceRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->createInstance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **iMSAdminApiV1InstancesCreateInstanceRequest** | [**\EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesCreateInstanceRequest**](../Model/IMSAdminApiV1InstancesCreateInstanceRequest.md)|  | [optional] |

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

## `createInstanceAsync()`

```php
createInstanceAsync($tenantId, $edfiAdminApiEdfiAdminV1CreateInstanceRequest)
```

Creates a new Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edfiAdminApiEdfiAdminV1CreateInstanceRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateInstanceRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateInstanceRequest | 

try {
    $apiInstance->createInstanceAsync($tenantId, $edfiAdminApiEdfiAdminV1CreateInstanceRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->createInstanceAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1CreateInstanceRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateInstanceRequest**](../Model/EdfiAdminApiEdfiAdminV1CreateInstanceRequest.md)|  | [optional] |

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

## `createInstanceV2()`

```php
createInstanceV2($tenantId, $body): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceCreatedResponse
```

Creates a new instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$body = NULL; // mixed | 

try {
    $result = $apiInstance->createInstanceV2($tenantId, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->createInstanceV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **body** | **mixed**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceCreatedResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteInstance()`

```php
deleteInstance($tenantId, $instanceId)
```

Deletes an Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $apiInstance->deleteInstance($tenantId, $instanceId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->deleteInstance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

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

## `deleteInstanceAsync()`

```php
deleteInstanceAsync($tenantId, $instanceId)
```

Deletes an Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $apiInstance->deleteInstanceAsync($tenantId, $instanceId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->deleteInstanceAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

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

## `deleteInstanceV2()`

```php
deleteInstanceV2($tenantId, $instanceId)
```

Deletes an instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $apiInstance->deleteInstanceV2($tenantId, $instanceId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->deleteInstanceV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

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

## `deleteSchoolYearAsync()`

```php
deleteSchoolYearAsync($tenantId, $instanceId, $year)
```

Removes an ODS database from an Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 

try {
    $apiInstance->deleteSchoolYearAsync($tenantId, $instanceId, $year);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->deleteSchoolYearAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |

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

## `getEdFiAdminInstanceEndpoints()`

```php
getEdFiAdminInstanceEndpoints($tenantId, $instanceId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse
```

Retrieves the Ed-Fi API endpoint URLs of an Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->getEdFiAdminInstanceEndpoints($tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->getEdFiAdminInstanceEndpoints: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse**](../Model/EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEdFiAdminInstanceYearEndpoints()`

```php
getEdFiAdminInstanceYearEndpoints($tenantId, $instanceId, $year): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse
```

Retrieves the Ed-Fi API endpoint URLs of an Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 

try {
    $result = $apiInstance->getEdFiAdminInstanceYearEndpoints($tenantId, $instanceId, $year);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->getEdFiAdminInstanceYearEndpoints: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse**](../Model/EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInstanceById()`

```php
getInstanceById($tenantId, $instanceId): \EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesInstanceProfileResponse
```

Retrieves an Instance by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->getInstanceById($tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->getInstanceById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesInstanceProfileResponse**](../Model/IMSAdminApiV1InstancesInstanceProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInstanceByIdAsync()`

```php
getInstanceByIdAsync($tenantId, $instanceId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1Instance
```

Retrieves an Instance by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->getInstanceByIdAsync($tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->getInstanceByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1Instance**](../Model/EdfiAdminApiEdfiAdminV1Instance.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInstanceCsvExport()`

```php
getInstanceCsvExport($tenantId, $instanceId): \EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesGetInstanceCsvExportResponse
```

Retrieves an Instance by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->getInstanceCsvExport($tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->getInstanceCsvExport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesGetInstanceCsvExportResponse**](../Model/IMSAdminApiV1InstancesGetInstanceCsvExportResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInstanceCsvExportV2()`

```php
getInstanceCsvExportV2($tenantId, $instanceId): \EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesInstanceCsvExportedResponse
```

Retrieves a ZIP bundle containing OneRoster Instance Database contents in CSV format

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->getInstanceCsvExportV2($tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->getInstanceCsvExportV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesInstanceCsvExportedResponse**](../Model/IMSAdminApiV1InstancesInstanceCsvExportedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInstanceEndpoints()`

```php
getInstanceEndpoints($tenantId, $instanceId): \EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesInstanceEndpointsResponse
```

Retrieves the One Roster endpoint URLs of an Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->getInstanceEndpoints($tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->getInstanceEndpoints: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesInstanceEndpointsResponse**](../Model/IMSAdminApiV1InstancesInstanceEndpointsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInstancesAsync()`

```php
getInstancesAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter, $deleted, $targetTenantId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel
```

Retrieves a list of Instances.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
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
$deleted = false; // bool | 
$targetTenantId = 'targetTenantId_example'; // string | 

try {
    $result = $apiInstance->getInstancesAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter, $deleted, $targetTenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->getInstancesAsync: ', $e->getMessage(), PHP_EOL;
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
| **deleted** | **bool**|  | [optional] [default to false] |
| **targetTenantId** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel**](../Model/EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPagedInstances()`

```php
getPagedInstances($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesPagedInstancesResponse
```

Retrieves a list of Instances.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
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
    $result = $apiInstance->getPagedInstances($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->getPagedInstances: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesPagedInstancesResponse**](../Model/IMSAdminApiV1InstancesPagedInstancesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantInstanceByIdV2()`

```php
getTenantInstanceByIdV2($tenantId, $instanceId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponse
```

Get Instance by Id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->getTenantInstanceByIdV2($tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->getTenantInstanceByIdV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantInstancesV2()`

```php
getTenantInstancesV2($tenantId, $pageSize, $pageIndex, $searchTerm, $type): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel
```

Get list of all instances for a tenant - V2

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$searchTerm = ''; // string | 
$type = ''; // string | 

try {
    $result = $apiInstance->getTenantInstancesV2($tenantId, $pageSize, $pageIndex, $searchTerm, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->getTenantInstancesV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **searchTerm** | **string**|  | [optional] [default to &#39;&#39;] |
| **type** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel**](../Model/EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `isInstanceCustomIdAvailable()`

```php
isInstanceCustomIdAvailable($tenantId, $customId): bool
```

Validate if instance is available

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$customId = 'customId_example'; // string | 

try {
    $result = $apiInstance->isInstanceCustomIdAvailable($tenantId, $customId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->isInstanceCustomIdAvailable: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **customId** | **string**|  | |

### Return type

**bool**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `loadApiMetadata()`

```php
loadApiMetadata($tenantId, $edGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult
```

Loads connection metadata.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest | 

try {
    $result = $apiInstance->loadApiMetadata($tenantId, $edGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->loadApiMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult**](../Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `resetInstance()`

```php
resetInstance($tenantId, $instanceId): \EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesInstanceResetResponse
```

Resets an Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->resetInstance($tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->resetInstance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesInstanceResetResponse**](../Model/IMSAdminApiV1InstancesInstanceResetResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `resetInstanceAsync()`

```php
resetInstanceAsync($tenantId, $instanceId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ResetInstanceResponse
```

Resets an Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->resetInstanceAsync($tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->resetInstanceAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ResetInstanceResponse**](../Model/EdfiAdminApiEdfiAdminV1ResetInstanceResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `resetInstanceCacheAsync()`

```php
resetInstanceCacheAsync($tenantId, $instanceId, $year): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ResetInstanceResponse
```

Resets the cache of an Instance and the specified ODS database.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 

try {
    $result = $apiInstance->resetInstanceCacheAsync($tenantId, $instanceId, $year);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->resetInstanceCacheAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1ResetInstanceResponse**](../Model/EdfiAdminApiEdfiAdminV1ResetInstanceResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `resetSchoolYearAsync()`

```php
resetSchoolYearAsync($tenantId, $instanceId, $year)
```

Resets the ODS database with the specified school year.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 

try {
    $apiInstance->resetSchoolYearAsync($tenantId, $instanceId, $year);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->resetSchoolYearAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |

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

## `setInstanceIsDefault()`

```php
setInstanceIsDefault($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest)
```

Updates the isDefault property for an instance

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest | 

try {
    $apiInstance->setInstanceIsDefault($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->setInstanceIsDefault: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest**](../Model/EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest.md)|  | [optional] |

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

## `testConnectionDetailsByInstanceIdAsync()`

```php
testConnectionDetailsByInstanceIdAsync($tenantId, $instanceId, $iMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest): \EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsConnectionTestedResponse
```

Tests the connection by obtaining the details by Instance ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$iMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest = new \EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest(); // \EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest | 

try {
    $result = $apiInstance->testConnectionDetailsByInstanceIdAsync($tenantId, $instanceId, $iMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->testConnectionDetailsByInstanceIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **iMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest** | [**\EdGraph\PlatformClient\Model\IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest**](../Model/IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest.md)|  | [optional] |

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

## `testCredentialsConnection()`

```php
testCredentialsConnection($tenantId, $body): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse
```

Tests availability of provided connection metadata.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$body = NULL; // mixed | 

try {
    $result = $apiInstance->testCredentialsConnection($tenantId, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->testCredentialsConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **body** | **mixed**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `testInstanceConnection()`

```php
testInstanceConnection($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1TestInstanceConnectionRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse
```

Tests the connection of the Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1TestInstanceConnectionRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest | 

try {
    $result = $apiInstance->testInstanceConnection($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1TestInstanceConnectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->testInstanceConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1TestInstanceConnectionRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest**](../Model/EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse**](../Model/EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `testInstanceYearConnection()`

```php
testInstanceYearConnection($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1TestInstanceConnectionRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse
```

Tests the connection of the Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$edfiAdminApiEdfiAdminV1TestInstanceConnectionRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest | 

try {
    $result = $apiInstance->testInstanceYearConnection($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1TestInstanceConnectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->testInstanceYearConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **edfiAdminApiEdfiAdminV1TestInstanceConnectionRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest**](../Model/EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse**](../Model/EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `truncateInstance()`

```php
truncateInstance($tenantId, $instanceId): \EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesInstanceTruncatedResponse
```

Truncates the Instance's database

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 

try {
    $result = $apiInstance->truncateInstance($tenantId, $instanceId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->truncateInstance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesInstanceTruncatedResponse**](../Model/IMSAdminApiV1InstancesInstanceTruncatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateInstance()`

```php
updateInstance($tenantId, $instanceId, $iMSAdminApiV1InstancesUpdateInstanceRequest)
```

Updates an Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$iMSAdminApiV1InstancesUpdateInstanceRequest = new \EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesUpdateInstanceRequest(); // \EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesUpdateInstanceRequest | 

try {
    $apiInstance->updateInstance($tenantId, $instanceId, $iMSAdminApiV1InstancesUpdateInstanceRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->updateInstance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **iMSAdminApiV1InstancesUpdateInstanceRequest** | [**\EdGraph\PlatformClient\Model\IMSAdminApiV1InstancesUpdateInstanceRequest**](../Model/IMSAdminApiV1InstancesUpdateInstanceRequest.md)|  | [optional] |

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

## `updateInstanceAsync()`

```php
updateInstanceAsync($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1UpdateInstanceRequest)
```

Updates an Instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1UpdateInstanceRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateInstanceRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateInstanceRequest | 

try {
    $apiInstance->updateInstanceAsync($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1UpdateInstanceRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->updateInstanceAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1UpdateInstanceRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateInstanceRequest**](../Model/EdfiAdminApiEdfiAdminV1UpdateInstanceRequest.md)|  | [optional] |

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

## `updateInstanceV2()`

```php
updateInstanceV2($tenantId, $instanceId, $body): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceUpdatedResponse
```

Updates an existing instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$body = NULL; // mixed | 

try {
    $result = $apiInstance->updateInstanceV2($tenantId, $instanceId, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->updateInstanceV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **body** | **mixed**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceUpdatedResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `validateCustomIdAvailable()`

```php
validateCustomIdAvailable($tenantId, $customId): bool
```

Validate if instance is available

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$customId = 'customId_example'; // string | 

try {
    $result = $apiInstance->validateCustomIdAvailable($tenantId, $customId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApi->validateCustomIdAvailable: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **customId** | **string**|  | |

### Return type

**bool**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
