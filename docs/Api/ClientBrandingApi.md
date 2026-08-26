# EdGraph\PlatformClient\ClientBrandingApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getClientBrandingAsync()**](ClientBrandingApi.md#getClientBrandingAsync) | **GET** /clients/{clientId}/branding | Public (unauthenticated) read of a client&#39;s branding for the sign-in and other pre-auth  surfaces (Azure DevOps #17086). Returns only render fields + the override flag — never secrets,  storage internals, or other client configuration. |


## `getClientBrandingAsync()`

```php
getClientBrandingAsync($clientId): \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesClientBrandingResponse
```

Public (unauthenticated) read of a client's branding for the sign-in and other pre-auth  surfaces (Azure DevOps #17086). Returns only render fields + the override flag — never secrets,  storage internals, or other client configuration.

Unauthenticated by design (branding is shown before login). An unknown client returns a  disabled default rather than 404, so the endpoint cannot be used as a client-existence oracle.  The response is cacheable so downstream CDNs/browsers absorb most traffic; rate limiting is  expected at the gateway.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ClientBrandingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$clientId = 'clientId_example'; // string | The OAuth client id (already URL-decoded by routing).

try {
    $result = $apiInstance->getClientBrandingAsync($clientId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientBrandingApi->getClientBrandingAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **clientId** | **string**| The OAuth client id (already URL-decoded by routing). | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesClientBrandingResponse**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesClientBrandingResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
