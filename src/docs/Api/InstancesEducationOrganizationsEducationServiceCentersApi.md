# EdGraph\PlatformClient\InstancesEducationOrganizationsEducationServiceCentersApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createEducationServiceCenterAsync()**](InstancesEducationOrganizationsEducationServiceCentersApi.md#createEducationServiceCenterAsync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters | Creates an EducationServiceCenter. |
| [**deleteEducationServiceCenterAsync()**](InstancesEducationOrganizationsEducationServiceCentersApi.md#deleteEducationServiceCenterAsync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Deletes an EducationServiceCenter. |
| [**getEducationServiceCenterByIdAsync()**](InstancesEducationOrganizationsEducationServiceCentersApi.md#getEducationServiceCenterByIdAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Retrieves an EducationServiceCenter by ID. |
| [**updateEducationServiceCenterAsync()**](InstancesEducationOrganizationsEducationServiceCentersApi.md#updateEducationServiceCenterAsync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Updates an EducationServiceCenter. |


## `createEducationServiceCenterAsync()`

```php
createEducationServiceCenterAsync($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse
```

Creates an EducationServiceCenter.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsEducationServiceCentersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$edfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest | 

try {
    $result = $apiInstance->createEducationServiceCenterAsync($tenantId, $instanceId, $year, $edfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsEducationServiceCentersApi->createEducationServiceCenterAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **edfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest**](../Model/EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse**](../Model/EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteEducationServiceCenterAsync()`

```php
deleteEducationServiceCenterAsync($tenantId, $instanceId, $year, $educationServiceCenterId)
```

Deletes an EducationServiceCenter.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsEducationServiceCentersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$educationServiceCenterId = 'educationServiceCenterId_example'; // string | 

try {
    $apiInstance->deleteEducationServiceCenterAsync($tenantId, $instanceId, $year, $educationServiceCenterId);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsEducationServiceCentersApi->deleteEducationServiceCenterAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **educationServiceCenterId** | **string**|  | |

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

## `getEducationServiceCenterByIdAsync()`

```php
getEducationServiceCenterByIdAsync($tenantId, $instanceId, $year, $educationServiceCenterId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EducationServiceCenter
```

Retrieves an EducationServiceCenter by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsEducationServiceCentersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$educationServiceCenterId = 'educationServiceCenterId_example'; // string | 

try {
    $result = $apiInstance->getEducationServiceCenterByIdAsync($tenantId, $instanceId, $year, $educationServiceCenterId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsEducationServiceCentersApi->getEducationServiceCenterByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **educationServiceCenterId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EducationServiceCenter**](../Model/EdfiAdminApiEdfiAdminV1EducationServiceCenter.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateEducationServiceCenterAsync()`

```php
updateEducationServiceCenterAsync($tenantId, $instanceId, $year, $educationServiceCenterId, $edfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest)
```

Updates an EducationServiceCenter.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesEducationOrganizationsEducationServiceCentersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$year = 56; // int | 
$educationServiceCenterId = 'educationServiceCenterId_example'; // string | 
$edfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest = new \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest(); // \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest | 

try {
    $apiInstance->updateEducationServiceCenterAsync($tenantId, $instanceId, $year, $educationServiceCenterId, $edfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest);
} catch (Exception $e) {
    echo 'Exception when calling InstancesEducationOrganizationsEducationServiceCentersApi->updateEducationServiceCenterAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **year** | **int**|  | |
| **educationServiceCenterId** | **string**|  | |
| **edfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest**](../Model/EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest.md)|  | [optional] |

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
