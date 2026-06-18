# EdGraph\PlatformClient\InstancesAuthorizationStrategiesApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAuthorizationStrategiesAsync()**](InstancesAuthorizationStrategiesApi.md#getAuthorizationStrategiesAsync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/authorizationstrategies | Retrieves a list of Authorization Strategies. |


## `getAuthorizationStrategiesAsync()`

```php
getAuthorizationStrategiesAsync($tenantId, $instanceId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1AuthorizationStrategiesResponse
```

Retrieves a list of Authorization Strategies.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InstancesAuthorizationStrategiesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$instanceId = 'instanceId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getAuthorizationStrategiesAsync($tenantId, $instanceId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstancesAuthorizationStrategiesApi->getAuthorizationStrategiesAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1AuthorizationStrategiesResponse**](../Model/EdfiAdminApiEdfiAdminV1AuthorizationStrategiesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
