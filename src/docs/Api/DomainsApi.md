# EdGraph\PlatformClient\DomainsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTenantDomainAsync()**](DomainsApi.md#createTenantDomainAsync) | **POST** /tenants/{tenantId}/domains | Creates a new domain |
| [**deleteTenantDomainAsync()**](DomainsApi.md#deleteTenantDomainAsync) | **DELETE** /tenants/{tenantId}/domains/{domainName} | Deletes a user |
| [**getAllTenantDomainsAsync()**](DomainsApi.md#getAllTenantDomainsAsync) | **GET** /tenants/{tenantId}/domains | Retrieves a list of domains associated to this tenant |
| [**getTenantDomainProfileByNameAsync()**](DomainsApi.md#getTenantDomainProfileByNameAsync) | **GET** /tenants/{tenantId}/domains/{domainName} | Retrieves a domain |
| [**updateTenantDomainAsync()**](DomainsApi.md#updateTenantDomainAsync) | **PUT** /tenants/{tenantId}/domains/{domainName} | Updates a domain |
| [**verifyTenantDomainAsync()**](DomainsApi.md#verifyTenantDomainAsync) | **PUT** /tenants/{tenantId}/domains/{domainName}/verify | Verify a  tenant&#39;s domain |


## `createTenantDomainAsync()`

```php
createTenantDomainAsync($tenantId, $tenantApiTenantV1CreateDomainRequest): \EdGraph\PlatformClient\Model\TenantApiTenantV1DomainCreatedResponse
```

Creates a new domain

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\DomainsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$tenantApiTenantV1CreateDomainRequest = new \EdGraph\PlatformClient\Model\TenantApiTenantV1CreateDomainRequest(); // \EdGraph\PlatformClient\Model\TenantApiTenantV1CreateDomainRequest | 

try {
    $result = $apiInstance->createTenantDomainAsync($tenantId, $tenantApiTenantV1CreateDomainRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainsApi->createTenantDomainAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **tenantApiTenantV1CreateDomainRequest** | [**\EdGraph\PlatformClient\Model\TenantApiTenantV1CreateDomainRequest**](../Model/TenantApiTenantV1CreateDomainRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1DomainCreatedResponse**](../Model/TenantApiTenantV1DomainCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteTenantDomainAsync()`

```php
deleteTenantDomainAsync($tenantId, $domainName)
```

Deletes a user

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\DomainsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$domainName = 'domainName_example'; // string | 

try {
    $apiInstance->deleteTenantDomainAsync($tenantId, $domainName);
} catch (Exception $e) {
    echo 'Exception when calling DomainsApi->deleteTenantDomainAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **domainName** | **string**|  | |

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

## `getAllTenantDomainsAsync()`

```php
getAllTenantDomainsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDtoPaginatedItemsViewModel
```

Retrieves a list of domains associated to this tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\DomainsApi(
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
    $result = $apiInstance->getAllTenantDomainsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainsApi->getAllTenantDomainsAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDtoPaginatedItemsViewModel**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDtoPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantDomainProfileByNameAsync()`

```php
getTenantDomainProfileByNameAsync($tenantId, $domainName): \EdGraph\PlatformClient\Model\TenantApiTenantV1DomainProfileResponse
```

Retrieves a domain

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\DomainsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$domainName = 'domainName_example'; // string | 

try {
    $result = $apiInstance->getTenantDomainProfileByNameAsync($tenantId, $domainName);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainsApi->getTenantDomainProfileByNameAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **domainName** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1DomainProfileResponse**](../Model/TenantApiTenantV1DomainProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTenantDomainAsync()`

```php
updateTenantDomainAsync($tenantId, $domainName, $tenantApiTenantV1UpdateDomainRequest): \EdGraph\PlatformClient\Model\TenantApiTenantV1DomainUpdatedResponse
```

Updates a domain

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\DomainsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$domainName = 'domainName_example'; // string | 
$tenantApiTenantV1UpdateDomainRequest = new \EdGraph\PlatformClient\Model\TenantApiTenantV1UpdateDomainRequest(); // \EdGraph\PlatformClient\Model\TenantApiTenantV1UpdateDomainRequest | 

try {
    $result = $apiInstance->updateTenantDomainAsync($tenantId, $domainName, $tenantApiTenantV1UpdateDomainRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainsApi->updateTenantDomainAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **domainName** | **string**|  | |
| **tenantApiTenantV1UpdateDomainRequest** | [**\EdGraph\PlatformClient\Model\TenantApiTenantV1UpdateDomainRequest**](../Model/TenantApiTenantV1UpdateDomainRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1DomainUpdatedResponse**](../Model/TenantApiTenantV1DomainUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `verifyTenantDomainAsync()`

```php
verifyTenantDomainAsync($tenantId, $domainName, $tenantApiTenantV1VerifyDomainRequest): \EdGraph\PlatformClient\Model\TenantApiTenantV1DomainVerifiedResponse
```

Verify a  tenant's domain

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\DomainsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$domainName = 'domainName_example'; // string | 
$tenantApiTenantV1VerifyDomainRequest = new \EdGraph\PlatformClient\Model\TenantApiTenantV1VerifyDomainRequest(); // \EdGraph\PlatformClient\Model\TenantApiTenantV1VerifyDomainRequest | 

try {
    $result = $apiInstance->verifyTenantDomainAsync($tenantId, $domainName, $tenantApiTenantV1VerifyDomainRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainsApi->verifyTenantDomainAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **domainName** | **string**|  | |
| **tenantApiTenantV1VerifyDomainRequest** | [**\EdGraph\PlatformClient\Model\TenantApiTenantV1VerifyDomainRequest**](../Model/TenantApiTenantV1VerifyDomainRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1DomainVerifiedResponse**](../Model/TenantApiTenantV1DomainVerifiedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
