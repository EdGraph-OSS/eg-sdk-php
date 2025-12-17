# EdGraph\PlatformClient\UsersEducationOrganizationsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addUserEducationOrganization()**](UsersEducationOrganizationsApi.md#addUserEducationOrganization) | **POST** /tenants/{tenantId}/users/{userId}/educationorganizations | Adds an Education Organization to a user. |
| [**getUserEducationOrganizations()**](UsersEducationOrganizationsApi.md#getUserEducationOrganizations) | **GET** /tenants/{tenantId}/users/{userId}/educationorganizations | Gets the Education Organizations of a user. |
| [**removeUserEducationOrganization()**](UsersEducationOrganizationsApi.md#removeUserEducationOrganization) | **DELETE** /tenants/{tenantId}/users/{userId}/educationorganizations/{educationOrganizationId} | Removes an Education Organization from a user. |
| [**updateUserEducationOrganization()**](UsersEducationOrganizationsApi.md#updateUserEducationOrganization) | **PUT** /tenants/{tenantId}/users/{userId}/educationorganizations/{educationOrganizationId} | Updates the Education Organization of a user. |


## `addUserEducationOrganization()`

```php
addUserEducationOrganization($tenantId, $userId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1EducationOrganizationAddedResponse
```

Adds an Education Organization to a user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersEducationOrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest | 

try {
    $result = $apiInstance->addUserEducationOrganization($tenantId, $userId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersEducationOrganizationsApi->addUserEducationOrganization: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1EducationOrganizationAddedResponse**](../Model/IdentityApiUserV1EducationOrganizationAddedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getUserEducationOrganizations()`

```php
getUserEducationOrganizations($tenantId, $userId): \EdGraph\PlatformClient\Model\IdentityApiUserV1EducationOrganizationPaginatedItemsResponse
```

Gets the Education Organizations of a user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersEducationOrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 

try {
    $result = $apiInstance->getUserEducationOrganizations($tenantId, $userId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersEducationOrganizationsApi->getUserEducationOrganizations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1EducationOrganizationPaginatedItemsResponse**](../Model/IdentityApiUserV1EducationOrganizationPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeUserEducationOrganization()`

```php
removeUserEducationOrganization($tenantId, $userId, $educationOrganizationId): \EdGraph\PlatformClient\Model\IdentityApiUserV1EducationOrganizationRemovedResponse
```

Removes an Education Organization from a user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersEducationOrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$educationOrganizationId = 56; // int | 

try {
    $result = $apiInstance->removeUserEducationOrganization($tenantId, $userId, $educationOrganizationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersEducationOrganizationsApi->removeUserEducationOrganization: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **educationOrganizationId** | **int**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1EducationOrganizationRemovedResponse**](../Model/IdentityApiUserV1EducationOrganizationRemovedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateUserEducationOrganization()`

```php
updateUserEducationOrganization($tenantId, $userId, $educationOrganizationId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1EducationOrganizationUpdatedResponse
```

Updates the Education Organization of a user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersEducationOrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$educationOrganizationId = 56; // int | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest | 

try {
    $result = $apiInstance->updateUserEducationOrganization($tenantId, $userId, $educationOrganizationId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersEducationOrganizationsApi->updateUserEducationOrganization: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **educationOrganizationId** | **int**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1EducationOrganizationUpdatedResponse**](../Model/IdentityApiUserV1EducationOrganizationUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
