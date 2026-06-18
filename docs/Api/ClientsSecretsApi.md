# EdGraph\PlatformClient\ClientsSecretsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addClientSecret()**](ClientsSecretsApi.md#addClientSecret) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId}/secrets | Creates a new secret for an OpenId client |
| [**regenerateOneRosterApiClientSecretAsync()**](ClientsSecretsApi.md#regenerateOneRosterApiClientSecretAsync) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId}/regeneratesecret | Regenerate Client Secret |


## `addClientSecret()`

```php
addClientSecret($tenantId, $instanceId, $clientId, $iMSAdminApiV1ClientsAddClientSecretRequest): \EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsClientSecretAddedResponse
```

Creates a new secret for an OpenId client

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ClientsSecretsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$instanceId = 'instanceId_example'; // string
$clientId = 'clientId_example'; // string | 
$iMSAdminApiV1ClientsAddClientSecretRequest = new \EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsAddClientSecretRequest(); // \EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsAddClientSecretRequest | 

try {
    $result = $apiInstance->addClientSecret($tenantId, $instanceId, $clientId, $iMSAdminApiV1ClientsAddClientSecretRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientsSecretsApi->addClientSecret: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **clientId** | **string**|  | |
| **iMSAdminApiV1ClientsAddClientSecretRequest** | [**\EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsAddClientSecretRequest**](../Model/IMSAdminApiV1ClientsAddClientSecretRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsClientSecretAddedResponse**](../Model/IMSAdminApiV1ClientsClientSecretAddedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `regenerateOneRosterApiClientSecretAsync()`

```php
regenerateOneRosterApiClientSecretAsync($tenantId, $instanceId, $clientId, $iMSAdminApiV1ClientsRegenerateClientSecretRequest): \EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsClientSecretRegeneratedResponse
```

Regenerate Client Secret

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ClientsSecretsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$instanceId = 'instanceId_example'; // string | 
$clientId = 'clientId_example'; // string | 
$iMSAdminApiV1ClientsRegenerateClientSecretRequest = new \EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsRegenerateClientSecretRequest(); // \EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsRegenerateClientSecretRequest | 

try {
    $result = $apiInstance->regenerateOneRosterApiClientSecretAsync($tenantId, $instanceId, $clientId, $iMSAdminApiV1ClientsRegenerateClientSecretRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientsSecretsApi->regenerateOneRosterApiClientSecretAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **instanceId** | **string**|  | |
| **clientId** | **string**|  | |
| **iMSAdminApiV1ClientsRegenerateClientSecretRequest** | [**\EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsRegenerateClientSecretRequest**](../Model/IMSAdminApiV1ClientsRegenerateClientSecretRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IMSAdminApiV1ClientsClientSecretRegeneratedResponse**](../Model/IMSAdminApiV1ClientsClientSecretRegeneratedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
