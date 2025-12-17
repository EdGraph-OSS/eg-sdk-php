# EdGraph\PlatformClient\V1Api

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**releaseUserLockout()**](V1Api.md#releaseUserLockout) | **PUT** /tenants/{tenantId}/users/{userId}/releaselockout |  |


## `releaseUserLockout()`

```php
releaseUserLockout($tenantId, $userId): \EdGraph\PlatformClient\Model\IdentityApiUserV1ReleaseUserLockoutResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\V1Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$userId = 'userId_example'; // string

try {
    $result = $apiInstance->releaseUserLockout($tenantId, $userId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling V1Api->releaseUserLockout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1ReleaseUserLockoutResponse**](../Model/IdentityApiUserV1ReleaseUserLockoutResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
