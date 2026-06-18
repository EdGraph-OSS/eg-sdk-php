# EdGraph\PlatformClient\InstancesInstanceApplicationsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createInstanceApplication()**](InstancesInstanceApplicationsApi.md#createInstanceApplication) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications | Creates an Instance Application |
| [**deleteInstanceApplication()**](InstancesInstanceApplicationsApi.md#deleteInstanceApplication) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId} | Deletes an Instance Application |
| [**getInstanceApplicationById()**](InstancesInstanceApplicationsApi.md#getInstanceApplicationById) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId} | Retrieves an Instance Application by ID. |
| [**getInstanceApplications()**](InstancesInstanceApplicationsApi.md#getInstanceApplications) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications | Retrieves a paginated list of Instance applications |
| [**updateInstanceApplication()**](InstancesInstanceApplicationsApi.md#updateInstanceApplication) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId} | Updates an Instance Application |


## `createInstanceApplication()`

```php
createInstanceApplication($tenantId, $instanceId, $edGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApplicationCreatedResponse
```

Creates an Instance Application

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesInstanceApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest | 

try {
    $result = $apiInstance->createInstanceApplication($tenantId, $instanceId, $edGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesInstanceApplicationsApi->createInstanceApplication: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApplicationCreatedResponse**](../Model/EdfiAdminApiEdfiAdminV1InstanceApplicationCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteInstanceApplication()`

```php
deleteInstanceApplication($tenantId, $instanceId, $applicationId)
```

Deletes an Instance Application

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesInstanceApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 

try {
    $apiInstance->deleteInstanceApplication($tenantId, $instanceId, $applicationId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesInstanceApplicationsApi->deleteInstanceApplication: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |

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

## `getInstanceApplicationById()`

```php
getInstanceApplicationById($tenantId, $instanceId, $applicationId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApplicationProfileResponse
```

Retrieves an Instance Application by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesInstanceApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 

try {
    $result = $apiInstance->getInstanceApplicationById($tenantId, $instanceId, $applicationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesInstanceApplicationsApi->getInstanceApplicationById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApplicationProfileResponse**](../Model/EdfiAdminApiEdfiAdminV1InstanceApplicationProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInstanceApplications()`

```php
getInstanceApplications($tenantId, $instanceId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponsePaginatedItemsViewModel
```

Retrieves a paginated list of Instance applications

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesInstanceApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getInstanceApplications($tenantId, $instanceId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesInstanceApplicationsApi->getInstanceApplications: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponsePaginatedItemsViewModel**](../Model/EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateInstanceApplication()`

```php
updateInstanceApplication($tenantId, $instanceId, $applicationId, $edfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApplicationUpdatedResponse
```

Updates an Instance Application

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesInstanceApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 
$edfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest | 

try {
    $result = $apiInstance->updateInstanceApplication($tenantId, $instanceId, $applicationId, $edfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesInstanceApplicationsApi->updateInstanceApplication: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest**](../Model/EdfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApplicationUpdatedResponse**](../Model/EdfiAdminApiEdfiAdminV1InstanceApplicationUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
