# EdGraph\PlatformClient\InstancesApplicationsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createApplicationAsync()**](InstancesApplicationsApi.md#createApplicationAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications | Creates an Application. |
| [**createApplicationUserAccessAsync()**](InstancesApplicationsApi.md#createApplicationUserAccessAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access | Creates a new application access. |
| [**deleteApplicationAsync()**](InstancesApplicationsApi.md#deleteApplicationAsync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Deletes an Application. |
| [**deleteApplicationUserAccessAsync()**](InstancesApplicationsApi.md#deleteApplicationUserAccessAsync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Deletes an application user access. |
| [**getApplicationAccessAsync()**](InstancesApplicationsApi.md#getApplicationAccessAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access | Retrieves a list of application accesses. |
| [**getApplicationAccessByIdAsync()**](InstancesApplicationsApi.md#getApplicationAccessByIdAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Retrieves an application access by ID. |
| [**getApplicationApiClientByIdAsync()**](InstancesApplicationsApi.md#getApplicationApiClientByIdAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId} | Retrieves an API Client of an Application by ID. |
| [**getApplicationApiClientsAsync()**](InstancesApplicationsApi.md#getApplicationApiClientsAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients | Retrieves the API Clients of an Application. |
| [**getApplicationByIdAsync()**](InstancesApplicationsApi.md#getApplicationByIdAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Retrieves an Application by ID. |
| [**getApplicationsAsync()**](InstancesApplicationsApi.md#getApplicationsAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications | Retrieves a list of Applications. |
| [**regenerateApiClientSecretAsync()**](InstancesApplicationsApi.md#regenerateApiClientSecretAsync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/regenerate | Regenerates the secret of an API Client. |
| [**regenerateApplicationApiClientCredentials()**](InstancesApplicationsApi.md#regenerateApplicationApiClientCredentials) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/regenerate | Regenerates an application&#39;s API Client Credentials |
| [**syncApplicationAsync()**](InstancesApplicationsApi.md#syncApplicationAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/sync | Copies an Application from one instance to another/other instance(s) |
| [**updateApplicationAsync()**](InstancesApplicationsApi.md#updateApplicationAsync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Updates an Application. |
| [**updateApplicationUserAccessAsync()**](InstancesApplicationsApi.md#updateApplicationUserAccessAsync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Updates a new application access. |


## `createApplicationAsync()`

```php
createApplicationAsync($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse
```

Creates an Application.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest | 

try {
    $result = $apiInstance->createApplicationAsync($tenantId, $instanceId, $edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->createApplicationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest**](../Model/EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse**](../Model/EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createApplicationUserAccessAsync()`

```php
createApplicationUserAccessAsync($tenantId, $instanceId, $applicationId, $apiClientId, $edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest)
```

Creates a new application access.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 
$apiClientId = 'apiClientId_example'; // string | 
$edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest = new \EdGraph\PlatformClient\Model\EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest(); // \EdGraph\PlatformClient\Model\EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest | 

try {
    $apiInstance->createApplicationUserAccessAsync($tenantId, $instanceId, $applicationId, $apiClientId, $edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->createApplicationUserAccessAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |
| **apiClientId** | **string**|  | |
| **edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest** | [**\EdGraph\PlatformClient\Model\EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest**](../Model/EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest.md)|  | [optional] |

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

## `deleteApplicationAsync()`

```php
deleteApplicationAsync($tenantId, $instanceId, $applicationId)
```

Deletes an Application.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 56; // int | 

try {
    $apiInstance->deleteApplicationAsync($tenantId, $instanceId, $applicationId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->deleteApplicationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **int**|  | |

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

## `deleteApplicationUserAccessAsync()`

```php
deleteApplicationUserAccessAsync($tenantId, $instanceId, $applicationId, $apiClientId, $accessId)
```

Deletes an application user access.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 
$apiClientId = 'apiClientId_example'; // string | 
$accessId = 'accessId_example'; // string | 

try {
    $apiInstance->deleteApplicationUserAccessAsync($tenantId, $instanceId, $applicationId, $apiClientId, $accessId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->deleteApplicationUserAccessAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |
| **apiClientId** | **string**|  | |
| **accessId** | **string**|  | |

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

## `getApplicationAccessAsync()`

```php
getApplicationAccessAsync($tenantId, $instanceId, $applicationId, $apiClientId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel
```

Retrieves a list of application accesses.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string
$applicationId = 'applicationId_example'; // string
$apiClientId = 'apiClientId_example'; // string
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getApplicationAccessAsync($tenantId, $instanceId, $applicationId, $apiClientId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->getApplicationAccessAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |
| **apiClientId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel**](../Model/EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getApplicationAccessByIdAsync()`

```php
getApplicationAccessByIdAsync($tenantId, $instanceId, $applicationId, $apiClientId, $accessId): \EdGraph\PlatformClient\Model\EdFiAdminApiApplicationAccessV1ApplicationAccessResponse
```

Retrieves an application access by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 56; // int | 
$apiClientId = 56; // int | 
$accessId = 'accessId_example'; // string | 

try {
    $result = $apiInstance->getApplicationAccessByIdAsync($tenantId, $instanceId, $applicationId, $apiClientId, $accessId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->getApplicationAccessByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **int**|  | |
| **apiClientId** | **int**|  | |
| **accessId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdFiAdminApiApplicationAccessV1ApplicationAccessResponse**](../Model/EdFiAdminApiApplicationAccessV1ApplicationAccessResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getApplicationApiClientByIdAsync()`

```php
getApplicationApiClientByIdAsync($tenantId, $instanceId, $applicationId, $apiClientId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse
```

Retrieves an API Client of an Application by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 
$apiClientId = 56; // int | 

try {
    $result = $apiInstance->getApplicationApiClientByIdAsync($tenantId, $instanceId, $applicationId, $apiClientId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->getApplicationApiClientByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |
| **apiClientId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse**](../Model/EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getApplicationApiClientsAsync()`

```php
getApplicationApiClientsAsync($tenantId, $instanceId, $applicationId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel
```

Retrieves the API Clients of an Application.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 

try {
    $result = $apiInstance->getApplicationApiClientsAsync($tenantId, $instanceId, $applicationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->getApplicationApiClientsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel**](../Model/EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getApplicationByIdAsync()`

```php
getApplicationByIdAsync($tenantId, $instanceId, $applicationId, $year, $loadEducationOrganizations): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse
```

Retrieves an Application by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 56; // int | 
$year = 56; // int | 
$loadEducationOrganizations = True; // bool | 

try {
    $result = $apiInstance->getApplicationByIdAsync($tenantId, $instanceId, $applicationId, $year, $loadEducationOrganizations);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->getApplicationByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **int**|  | |
| **year** | **int**|  | [optional] |
| **loadEducationOrganizations** | **bool**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse**](../Model/EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getApplicationsAsync()`

```php
getApplicationsAsync($tenantId, $instanceId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel
```

Retrieves a list of Applications.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
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
    $result = $apiInstance->getApplicationsAsync($tenantId, $instanceId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->getApplicationsAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel**](../Model/EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `regenerateApiClientSecretAsync()`

```php
regenerateApiClientSecretAsync($tenantId, $instanceId, $applicationId, $apiClientId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse
```

Regenerates the secret of an API Client.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 56; // int | 
$apiClientId = 56; // int | 

try {
    $result = $apiInstance->regenerateApiClientSecretAsync($tenantId, $instanceId, $applicationId, $apiClientId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->regenerateApiClientSecretAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **int**|  | |
| **apiClientId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse**](../Model/EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `regenerateApplicationApiClientCredentials()`

```php
regenerateApplicationApiClientCredentials($tenantId, $instanceId, $applicationId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse
```

Regenerates an application's API Client Credentials

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 56; // int | 

try {
    $result = $apiInstance->regenerateApplicationApiClientCredentials($tenantId, $instanceId, $applicationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->regenerateApplicationApiClientCredentials: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse**](../Model/EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `syncApplicationAsync()`

```php
syncApplicationAsync($tenantId, $instanceId, $applicationId, $edfiAdminApiEdfiAdminV1SyncApplicationRequest)
```

Copies an Application from one instance to another/other instance(s)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 56; // int | 
$edfiAdminApiEdfiAdminV1SyncApplicationRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncApplicationRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncApplicationRequest | 

try {
    $apiInstance->syncApplicationAsync($tenantId, $instanceId, $applicationId, $edfiAdminApiEdfiAdminV1SyncApplicationRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->syncApplicationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **int**|  | |
| **edfiAdminApiEdfiAdminV1SyncApplicationRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1SyncApplicationRequest**](../Model/EdfiAdminApiEdfiAdminV1SyncApplicationRequest.md)|  | [optional] |

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

## `updateApplicationAsync()`

```php
updateApplicationAsync($tenantId, $instanceId, $applicationId, $edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest)
```

Updates an Application.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 
$edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest | 

try {
    $apiInstance->updateApplicationAsync($tenantId, $instanceId, $applicationId, $edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->updateApplicationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest**](../Model/EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest.md)|  | [optional] |

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

## `updateApplicationUserAccessAsync()`

```php
updateApplicationUserAccessAsync($tenantId, $instanceId, $applicationId, $apiClientId, $accessId, $edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest)
```

Updates a new application access.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 
$apiClientId = 'apiClientId_example'; // string | 
$accessId = 'accessId_example'; // string | 
$edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest = new \EdGraph\PlatformClient\Model\EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest(); // \EdGraph\PlatformClient\Model\EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest | 

try {
    $apiInstance->updateApplicationUserAccessAsync($tenantId, $instanceId, $applicationId, $apiClientId, $accessId, $edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesApplicationsApi->updateApplicationUserAccessAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **applicationId** | **string**|  | |
| **apiClientId** | **string**|  | |
| **accessId** | **string**|  | |
| **edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest** | [**\EdGraph\PlatformClient\Model\EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest**](../Model/EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest.md)|  | [optional] |

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
