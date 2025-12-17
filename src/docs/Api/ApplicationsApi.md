# EdGraph\PlatformClient\ApplicationsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getTenantApplicationProfileByIdAsync()**](ApplicationsApi.md#getTenantApplicationProfileByIdAsync) | **GET** /tenants/{tenantId}/applications/{applicationId} | Retrieves an application |
| [**getTenantApplicationsAsync()**](ApplicationsApi.md#getTenantApplicationsAsync) | **GET** /tenants/{tenantId}/applications | Retrieves a list of applications associated to this tenant |


## `getTenantApplicationProfileByIdAsync()`

```php
getTenantApplicationProfileByIdAsync($tenantId, $applicationId): \EdGraph\PlatformClient\Model\ApplicationApiApplicationV1ApplicationProfileResponse
```

Retrieves an application

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$applicationId = 'applicationId_example'; // string | 

try {
    $result = $apiInstance->getTenantApplicationProfileByIdAsync($tenantId, $applicationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsApi->getTenantApplicationProfileByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **applicationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ApplicationApiApplicationV1ApplicationProfileResponse**](../Model/ApplicationApiApplicationV1ApplicationProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantApplicationsAsync()`

```php
getTenantApplicationsAsync($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\ApplicationApiApplicationV1ApplicationListResponse
```

Retrieves a list of applications associated to this tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ApplicationsApi(
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
    $result = $apiInstance->getTenantApplicationsAsync($tenantId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsApi->getTenantApplicationsAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\ApplicationApiApplicationV1ApplicationListResponse**](../Model/ApplicationApiApplicationV1ApplicationListResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
