# EdGraph\PlatformClient\TenantBrandingApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**updateTenantBranding()**](TenantBrandingApi.md#updateTenantBranding) | **PUT** /tenants/{tenantId}/branding | Updates the branding of tenant |


## `updateTenantBranding()`

```php
updateTenantBranding($tenantId, $logoFile, $backgroundFile, $brandName, $enabled): \EdGraph\PlatformClient\Model\TenantApiTenantV1TenantUpdatedResponse
```

Updates the branding of tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\TenantBrandingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$logoFile = '/path/to/file.txt'; // \SplFileObject
$backgroundFile = '/path/to/file.txt'; // \SplFileObject
$brandName = 'brandName_example'; // string
$enabled = True; // bool

try {
    $result = $apiInstance->updateTenantBranding($tenantId, $logoFile, $backgroundFile, $brandName, $enabled);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantBrandingApi->updateTenantBranding: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **logoFile** | **\SplFileObject****\SplFileObject**|  | [optional] |
| **backgroundFile** | **\SplFileObject****\SplFileObject**|  | [optional] |
| **brandName** | **string**|  | [optional] |
| **enabled** | **bool**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1TenantUpdatedResponse**](../Model/TenantApiTenantV1TenantUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
