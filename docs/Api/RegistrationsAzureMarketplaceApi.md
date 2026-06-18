# EdGraph\PlatformClient\RegistrationsAzureMarketplaceApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**submitTenantRegistrationAzureMonaAsync()**](RegistrationsAzureMarketplaceApi.md#submitTenantRegistrationAzureMonaAsync) | **POST** /registrations/azure/mona | Submits a tenant&#39;s registration request received through Azure [M]arketplace [On]boarding [A]ccelerator (MONA) |


## `submitTenantRegistrationAzureMonaAsync()`

```php
submitTenantRegistrationAzureMonaAsync($registrationApiRegistrationV2SubmitTenantRegistrationRequest): string
```

Submits a tenant's registration request received through Azure [M]arketplace [On]boarding [A]ccelerator (MONA)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\RegistrationsAzureMarketplaceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$registrationApiRegistrationV2SubmitTenantRegistrationRequest = new \EdGraph\PlatformClient\Model\RegistrationApiRegistrationV2SubmitTenantRegistrationRequest(); // \EdGraph\PlatformClient\Model\RegistrationApiRegistrationV2SubmitTenantRegistrationRequest | 

try {
    $result = $apiInstance->submitTenantRegistrationAzureMonaAsync($registrationApiRegistrationV2SubmitTenantRegistrationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RegistrationsAzureMarketplaceApi->submitTenantRegistrationAzureMonaAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registrationApiRegistrationV2SubmitTenantRegistrationRequest** | [**\EdGraph\PlatformClient\Model\RegistrationApiRegistrationV2SubmitTenantRegistrationRequest**](../Model/RegistrationApiRegistrationV2SubmitTenantRegistrationRequest.md)|  | [optional] |

### Return type

**string**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
