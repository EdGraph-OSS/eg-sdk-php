# EdGraph\PlatformClient\TenantsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getTenantByIdAsync()**](TenantsApi.md#getTenantByIdAsync) | **GET** /tenants/{tenantId} | Retrieves the profile of a specific tenant |
| [**updateTenantAsync()**](TenantsApi.md#updateTenantAsync) | **PUT** /tenants/{tenantId} | Updates a tenant&#39;s profile |


## `getTenantByIdAsync()`

```php
getTenantByIdAsync($tenantId): \EdGraph\PlatformClient\Model\TenantApiTenantV1TenantProfileResponse
```

Retrieves the profile of a specific tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->getTenantByIdAsync($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantsApi->getTenantByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1TenantProfileResponse**](../Model/TenantApiTenantV1TenantProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTenantAsync()`

```php
updateTenantAsync($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest): \EdGraph\PlatformClient\Model\TenantApiTenantV1TenantUpdatedResponse
```

Updates a tenant's profile

Note: Only the tenant's Identity Providers can be updated at this time

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest | 

try {
    $result = $apiInstance->updateTenantAsync($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantsApi->updateTenantAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1TenantUpdatedResponse**](../Model/TenantApiTenantV1TenantUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
