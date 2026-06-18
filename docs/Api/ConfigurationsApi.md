# EdGraph\PlatformClient\ConfigurationsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createAnalyticsConfigurationAsync()**](ConfigurationsApi.md#createAnalyticsConfigurationAsync) | **POST** /tenants/{tenantId}/analytics/configurations | Creates a new configuration. |
| [**deleteAnalyticsConfigurationAsync()**](ConfigurationsApi.md#deleteAnalyticsConfigurationAsync) | **DELETE** /tenants/{tenantId}/analytics/configurations/{configurationId} | Deletes a configuration. |
| [**getAllAnalyticsConfigurationsAsync()**](ConfigurationsApi.md#getAllAnalyticsConfigurationsAsync) | **GET** /tenants/{tenantId}/analytics/configurations | Retrieves all configurations. |
| [**getAnalyticsConfigurationByIdAsync()**](ConfigurationsApi.md#getAnalyticsConfigurationByIdAsync) | **GET** /tenants/{tenantId}/analytics/configurations/{configurationId} | Retrieves a configuration by ID. |
| [**getAnalyticsConfigurationByTenantIdAsync()**](ConfigurationsApi.md#getAnalyticsConfigurationByTenantIdAsync) | **GET** /tenants/{tenantId}/analytics/configurations/default | Retrieves current default configuration. |
| [**hasValidAnalyticsConfigurationAsync()**](ConfigurationsApi.md#hasValidAnalyticsConfigurationAsync) | **GET** /tenants/{tenantId}/analytics/configurations/default/valid | Verifies if current default configuration has required values for correct functionality. |
| [**updateAnalyticsConfigurationAsync()**](ConfigurationsApi.md#updateAnalyticsConfigurationAsync) | **PUT** /tenants/{tenantId}/analytics/configurations/{configurationId} | Updates a configuration. |
| [**validateAADTokenAsync()**](ConfigurationsApi.md#validateAADTokenAsync) | **POST** /tenants/{tenantId}/analytics/configurations/azure/testconnection | Verifies if AAD token generation is possible with user provided values. |


## `createAnalyticsConfigurationAsync()`

```php
createAnalyticsConfigurationAsync($tenantId, $workspaceName, $analyticsApiConfigurationsV1CreateConfigurationRequest): \EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsConfiguration
```

Creates a new configuration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConfigurationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$workspaceName = 'workspaceName_example'; // string | 
$analyticsApiConfigurationsV1CreateConfigurationRequest = new \EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1CreateConfigurationRequest(); // \EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1CreateConfigurationRequest | 

try {
    $result = $apiInstance->createAnalyticsConfigurationAsync($tenantId, $workspaceName, $analyticsApiConfigurationsV1CreateConfigurationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationsApi->createAnalyticsConfigurationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **workspaceName** | **string**|  | |
| **analyticsApiConfigurationsV1CreateConfigurationRequest** | [**\EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1CreateConfigurationRequest**](../Model/AnalyticsApiConfigurationsV1CreateConfigurationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsConfiguration**](../Model/AnalyticsApiConfigurationsV1AnalyticsConfiguration.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteAnalyticsConfigurationAsync()`

```php
deleteAnalyticsConfigurationAsync($tenantId, $configurationId)
```

Deletes a configuration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConfigurationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$configurationId = 'configurationId_example'; // string | 

try {
    $apiInstance->deleteAnalyticsConfigurationAsync($tenantId, $configurationId);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationsApi->deleteAnalyticsConfigurationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **configurationId** | **string**|  | |

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

## `getAllAnalyticsConfigurationsAsync()`

```php
getAllAnalyticsConfigurationsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel
```

Retrieves all configurations.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConfigurationsApi(
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
    $result = $apiInstance->getAllAnalyticsConfigurationsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationsApi->getAllAnalyticsConfigurationsAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel**](../Model/AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAnalyticsConfigurationByIdAsync()`

```php
getAnalyticsConfigurationByIdAsync($tenantId, $configurationId): \EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsConfiguration
```

Retrieves a configuration by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConfigurationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$configurationId = 'configurationId_example'; // string | 

try {
    $result = $apiInstance->getAnalyticsConfigurationByIdAsync($tenantId, $configurationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationsApi->getAnalyticsConfigurationByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **configurationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsConfiguration**](../Model/AnalyticsApiConfigurationsV1AnalyticsConfiguration.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAnalyticsConfigurationByTenantIdAsync()`

```php
getAnalyticsConfigurationByTenantIdAsync($tenantId): \EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsConfiguration
```

Retrieves current default configuration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConfigurationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->getAnalyticsConfigurationByTenantIdAsync($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationsApi->getAnalyticsConfigurationByTenantIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsConfiguration**](../Model/AnalyticsApiConfigurationsV1AnalyticsConfiguration.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `hasValidAnalyticsConfigurationAsync()`

```php
hasValidAnalyticsConfigurationAsync($tenantId): \EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1HasValidConfigurationResponse
```

Verifies if current default configuration has required values for correct functionality.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConfigurationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->hasValidAnalyticsConfigurationAsync($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationsApi->hasValidAnalyticsConfigurationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1HasValidConfigurationResponse**](../Model/AnalyticsApiConfigurationsV1HasValidConfigurationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateAnalyticsConfigurationAsync()`

```php
updateAnalyticsConfigurationAsync($tenantId, $configurationId, $analyticsApiConfigurationsV1UpdateConfigurationRequest): \EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1ConfigurationResponse
```

Updates a configuration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConfigurationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$configurationId = 'configurationId_example'; // string
$analyticsApiConfigurationsV1UpdateConfigurationRequest = new \EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1UpdateConfigurationRequest(); // \EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1UpdateConfigurationRequest | 

try {
    $result = $apiInstance->updateAnalyticsConfigurationAsync($tenantId, $configurationId, $analyticsApiConfigurationsV1UpdateConfigurationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationsApi->updateAnalyticsConfigurationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **configurationId** | **string**|  | |
| **analyticsApiConfigurationsV1UpdateConfigurationRequest** | [**\EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1UpdateConfigurationRequest**](../Model/AnalyticsApiConfigurationsV1UpdateConfigurationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1ConfigurationResponse**](../Model/AnalyticsApiConfigurationsV1ConfigurationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `validateAADTokenAsync()`

```php
validateAADTokenAsync($tenantId, $analyticsApiConfigurationsV1AnalyticsAzureAd): \EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1TestConnectionResponse
```

Verifies if AAD token generation is possible with user provided values.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ConfigurationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$analyticsApiConfigurationsV1AnalyticsAzureAd = new \EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsAzureAd(); // \EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsAzureAd | 

try {
    $result = $apiInstance->validateAADTokenAsync($tenantId, $analyticsApiConfigurationsV1AnalyticsAzureAd);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationsApi->validateAADTokenAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **analyticsApiConfigurationsV1AnalyticsAzureAd** | [**\EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsAzureAd**](../Model/AnalyticsApiConfigurationsV1AnalyticsAzureAd.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1TestConnectionResponse**](../Model/AnalyticsApiConfigurationsV1TestConnectionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
