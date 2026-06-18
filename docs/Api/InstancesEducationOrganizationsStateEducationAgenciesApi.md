# EdGraph\PlatformClient\InstancesEducationOrganizationsStateEducationAgenciesApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createStateEducationAgencyAsync()**](InstancesEducationOrganizationsStateEducationAgenciesApi.md#createStateEducationAgencyAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies | Creates a StateEducationAgency. |
| [**deleteStateEducationAgencyAsync()**](InstancesEducationOrganizationsStateEducationAgenciesApi.md#deleteStateEducationAgencyAsync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies/{stateEducationAgencyId} | Deletes a StateEducationAgency. |
| [**getStateEducationAgencyByIdAsync()**](InstancesEducationOrganizationsStateEducationAgenciesApi.md#getStateEducationAgencyByIdAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies/{stateEducationAgencyId} | Retrieves a StateEducationAgency by ID. |
| [**updateStateEducationAgencyAsync()**](InstancesEducationOrganizationsStateEducationAgenciesApi.md#updateStateEducationAgencyAsync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies/{stateEducationAgencyId} | Updates a StateEducationAgency. |


## `createStateEducationAgencyAsync()`

```php
createStateEducationAgencyAsync($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StateEducationAgencyCreatedResponse
```

Creates a StateEducationAgency.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsStateEducationAgenciesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$edfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest | 

try {
    $result = $apiInstance->createStateEducationAgencyAsync($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsStateEducationAgenciesApi->createStateEducationAgencyAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **edfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest**](../Model/EdfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StateEducationAgencyCreatedResponse**](../Model/EdfiAdminApiEdfiAdminV1StateEducationAgencyCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteStateEducationAgencyAsync()`

```php
deleteStateEducationAgencyAsync($tenantId, $instanceId, $year, $stateEducationAgencyId)
```

Deletes a StateEducationAgency.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsStateEducationAgenciesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$stateEducationAgencyId = 'stateEducationAgencyId_example'; // string | 

try {
    $apiInstance->deleteStateEducationAgencyAsync($tenantId, $instanceId, $year, $stateEducationAgencyId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsStateEducationAgenciesApi->deleteStateEducationAgencyAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **stateEducationAgencyId** | **string**|  | |

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

## `getStateEducationAgencyByIdAsync()`

```php
getStateEducationAgencyByIdAsync($tenantId, $instanceId, $year, $stateEducationAgencyId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StateEducationAgency
```

Retrieves a StateEducationAgency by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsStateEducationAgenciesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$stateEducationAgencyId = 'stateEducationAgencyId_example'; // string | 

try {
    $result = $apiInstance->getStateEducationAgencyByIdAsync($tenantId, $instanceId, $year, $stateEducationAgencyId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsStateEducationAgenciesApi->getStateEducationAgencyByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **stateEducationAgencyId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1StateEducationAgency**](../Model/EdfiAdminApiEdfiAdminV1StateEducationAgency.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateStateEducationAgencyAsync()`

```php
updateStateEducationAgencyAsync($tenantId, $instanceId, $year, $stateEducationAgencyId, $edfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest)
```

Updates a StateEducationAgency.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsStateEducationAgenciesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$stateEducationAgencyId = 'stateEducationAgencyId_example'; // string | 
$edfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest | 

try {
    $apiInstance->updateStateEducationAgencyAsync($tenantId, $instanceId, $year, $stateEducationAgencyId, $edfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsStateEducationAgenciesApi->updateStateEducationAgencyAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **stateEducationAgencyId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest**](../Model/EdfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest.md)|  | [optional] |

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
