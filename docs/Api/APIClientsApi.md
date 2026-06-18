# EdGraph\PlatformClient\APIClientsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTenantApiClientAsync()**](APIClientsApi.md#createTenantApiClientAsync) | **POST** /tenants/{tenantId}/apiclients | Creates a new OpenId API Client |
| [**deleteTenantApiClientAsync()**](APIClientsApi.md#deleteTenantApiClientAsync) | **DELETE** /tenants/{tenantId}/apiclients/{clientId} | Deletes an OpenId API Client |
| [**getAllTenantApiClientsAsync()**](APIClientsApi.md#getAllTenantApiClientsAsync) | **GET** /tenants/{tenantId}/apiclients | Retrieves a list of OpenId API Clients associated to this tenant |
| [**getTenantApiClientByIdAsync()**](APIClientsApi.md#getTenantApiClientByIdAsync) | **GET** /tenants/{tenantId}/apiclients/{clientId} | Retrieves an OpenId API Client |
| [**regenerateTenantApiClientSecretAsync()**](APIClientsApi.md#regenerateTenantApiClientSecretAsync) | **PUT** /tenants/{tenantId}/apiclients/{clientId}/regeneratesecret | Regenerates an OpenId API Client&#39;s secret |
| [**updateTenantApiClientAsync()**](APIClientsApi.md#updateTenantApiClientAsync) | **PUT** /tenants/{tenantId}/apiclients/{clientId} | Updates an OpenId API Client |


## `createTenantApiClientAsync()`

```php
createTenantApiClientAsync($tenantId, $identityApiApiClientV1CreateApiClientRequest): \EdGraph\PlatformClient\Model\IdentityApiApiClientV1ApiClientCreatedResponse
```

Creates a new OpenId API Client

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\APIClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$identityApiApiClientV1CreateApiClientRequest = new \EdGraph\PlatformClient\Model\IdentityApiApiClientV1CreateApiClientRequest(); // \EdGraph\PlatformClient\Model\IdentityApiApiClientV1CreateApiClientRequest | 

try {
    $result = $apiInstance->createTenantApiClientAsync($tenantId, $identityApiApiClientV1CreateApiClientRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling APIClientsApi->createTenantApiClientAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **identityApiApiClientV1CreateApiClientRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiApiClientV1CreateApiClientRequest**](../Model/IdentityApiApiClientV1CreateApiClientRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiApiClientV1ApiClientCreatedResponse**](../Model/IdentityApiApiClientV1ApiClientCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteTenantApiClientAsync()`

```php
deleteTenantApiClientAsync($tenantId, $clientId)
```

Deletes an OpenId API Client

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\APIClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$clientId = 'clientId_example'; // string | 

try {
    $apiInstance->deleteTenantApiClientAsync($tenantId, $clientId);
} catch (Exception $e) {
    echo 'Exception when calling APIClientsApi->deleteTenantApiClientAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllTenantApiClientsAsync()`

```php
getAllTenantApiClientsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel
```

Retrieves a list of OpenId API Clients associated to this tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\APIClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getAllTenantApiClientsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling APIClientsApi->getAllTenantApiClientsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel**](../Model/IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantApiClientByIdAsync()`

```php
getTenantApiClientByIdAsync($tenantId, $clientId): \EdGraph\PlatformClient\Model\IdentityApiApiClientV1ApiClientProfileResponse
```

Retrieves an OpenId API Client

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\APIClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$clientId = 'clientId_example'; // string | 

try {
    $result = $apiInstance->getTenantApiClientByIdAsync($tenantId, $clientId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling APIClientsApi->getTenantApiClientByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiApiClientV1ApiClientProfileResponse**](../Model/IdentityApiApiClientV1ApiClientProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `regenerateTenantApiClientSecretAsync()`

```php
regenerateTenantApiClientSecretAsync($tenantId, $clientId, $identityApiApiClientV1RegenerateApiClientSecretRequest): \EdGraph\PlatformClient\Model\IdentityApiApiClientV1ApiClientSecretRegeneratedResponse
```

Regenerates an OpenId API Client's secret

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\APIClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$clientId = 'clientId_example'; // string | 
$identityApiApiClientV1RegenerateApiClientSecretRequest = new \EdGraph\PlatformClient\Model\IdentityApiApiClientV1RegenerateApiClientSecretRequest(); // \EdGraph\PlatformClient\Model\IdentityApiApiClientV1RegenerateApiClientSecretRequest | 

try {
    $result = $apiInstance->regenerateTenantApiClientSecretAsync($tenantId, $clientId, $identityApiApiClientV1RegenerateApiClientSecretRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling APIClientsApi->regenerateTenantApiClientSecretAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |
| **identityApiApiClientV1RegenerateApiClientSecretRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiApiClientV1RegenerateApiClientSecretRequest**](../Model/IdentityApiApiClientV1RegenerateApiClientSecretRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiApiClientV1ApiClientSecretRegeneratedResponse**](../Model/IdentityApiApiClientV1ApiClientSecretRegeneratedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTenantApiClientAsync()`

```php
updateTenantApiClientAsync($tenantId, $clientId, $identityApiApiClientV1UpdateApiClientRequest): \EdGraph\PlatformClient\Model\IdentityApiApiClientV1ApiClientUpdatedResponse
```

Updates an OpenId API Client

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\APIClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$clientId = 'clientId_example'; // string | 
$identityApiApiClientV1UpdateApiClientRequest = new \EdGraph\PlatformClient\Model\IdentityApiApiClientV1UpdateApiClientRequest(); // \EdGraph\PlatformClient\Model\IdentityApiApiClientV1UpdateApiClientRequest | 

try {
    $result = $apiInstance->updateTenantApiClientAsync($tenantId, $clientId, $identityApiApiClientV1UpdateApiClientRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling APIClientsApi->updateTenantApiClientAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **clientId** | **string**|  | |
| **identityApiApiClientV1UpdateApiClientRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiApiClientV1UpdateApiClientRequest**](../Model/IdentityApiApiClientV1UpdateApiClientRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiApiClientV1ApiClientUpdatedResponse**](../Model/IdentityApiApiClientV1ApiClientUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
