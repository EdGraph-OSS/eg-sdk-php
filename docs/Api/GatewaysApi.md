# EdGraph\PlatformClient\GatewaysApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllAnalyticsGatewaysAsync()**](GatewaysApi.md#getAllAnalyticsGatewaysAsync) | **GET** /tenants/{tenantId}/analytics/gateways | Retrieves a list of gateways in Power Bi that the user has access to. |


## `getAllAnalyticsGatewaysAsync()`

```php
getAllAnalyticsGatewaysAsync($tenantId): \EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1Instance
```

Retrieves a list of gateways in Power Bi that the user has access to.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\GatewaysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->getAllAnalyticsGatewaysAsync($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GatewaysApi->getAllAnalyticsGatewaysAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

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
