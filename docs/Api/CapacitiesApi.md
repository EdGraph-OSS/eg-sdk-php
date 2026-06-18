# EdGraph\PlatformClient\CapacitiesApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**assignMyGroupToCapacity()**](CapacitiesApi.md#assignMyGroupToCapacity) | **POST** /tenants/{tenantId}/analytics/capacities | Assigns the specified group to the specified capacity. |
| [**getAllAnalyticsPowerBiCapacities()**](CapacitiesApi.md#getAllAnalyticsPowerBiCapacities) | **GET** /tenants/{tenantId}/analytics/capacities | Retrieves a list of capacities in Power Bi that the user has access to. |
| [**resumeCapacityAsync()**](CapacitiesApi.md#resumeCapacityAsync) | **POST** /tenants/{tenantId}/analytics/capacities/resume | Resumes currently suspended capacity |
| [**suspendCapacityAsync()**](CapacitiesApi.md#suspendCapacityAsync) | **POST** /tenants/{tenantId}/analytics/capacities/suspend | Suspends currently active capacity |


## `assignMyGroupToCapacity()`

```php
assignMyGroupToCapacity($tenantId, $analyticsApiCapacitiesV1AssignCapacityRequest)
```

Assigns the specified group to the specified capacity.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CapacitiesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$analyticsApiCapacitiesV1AssignCapacityRequest = new \EdGraph\PlatformClient\Model\AnalyticsApiCapacitiesV1AssignCapacityRequest(); // \EdGraph\PlatformClient\Model\AnalyticsApiCapacitiesV1AssignCapacityRequest | 

try {
    $apiInstance->assignMyGroupToCapacity($tenantId, $analyticsApiCapacitiesV1AssignCapacityRequest);
} catch (Exception $e) {
    echo 'Exception when calling CapacitiesApi->assignMyGroupToCapacity: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **analyticsApiCapacitiesV1AssignCapacityRequest** | [**\EdGraph\PlatformClient\Model\AnalyticsApiCapacitiesV1AssignCapacityRequest**](../Model/AnalyticsApiCapacitiesV1AssignCapacityRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllAnalyticsPowerBiCapacities()`

```php
getAllAnalyticsPowerBiCapacities($tenantId): \EdGraph\PlatformClient\Model\AnalyticsApiCapacitiesV1CapacityResponse
```

Retrieves a list of capacities in Power Bi that the user has access to.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CapacitiesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->getAllAnalyticsPowerBiCapacities($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CapacitiesApi->getAllAnalyticsPowerBiCapacities: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiCapacitiesV1CapacityResponse**](../Model/AnalyticsApiCapacitiesV1CapacityResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `resumeCapacityAsync()`

```php
resumeCapacityAsync($tenantId, $analyticsApiCapacitiesV1ResumeCapacityRequest)
```

Resumes currently suspended capacity

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CapacitiesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$analyticsApiCapacitiesV1ResumeCapacityRequest = new \EdGraph\PlatformClient\Model\AnalyticsApiCapacitiesV1ResumeCapacityRequest(); // \EdGraph\PlatformClient\Model\AnalyticsApiCapacitiesV1ResumeCapacityRequest | 

try {
    $apiInstance->resumeCapacityAsync($tenantId, $analyticsApiCapacitiesV1ResumeCapacityRequest);
} catch (Exception $e) {
    echo 'Exception when calling CapacitiesApi->resumeCapacityAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **analyticsApiCapacitiesV1ResumeCapacityRequest** | [**\EdGraph\PlatformClient\Model\AnalyticsApiCapacitiesV1ResumeCapacityRequest**](../Model/AnalyticsApiCapacitiesV1ResumeCapacityRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `suspendCapacityAsync()`

```php
suspendCapacityAsync($tenantId, $analyticsApiCapacitiesV1SuspendCapacityRequest)
```

Suspends currently active capacity

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CapacitiesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$analyticsApiCapacitiesV1SuspendCapacityRequest = new \EdGraph\PlatformClient\Model\AnalyticsApiCapacitiesV1SuspendCapacityRequest(); // \EdGraph\PlatformClient\Model\AnalyticsApiCapacitiesV1SuspendCapacityRequest | 

try {
    $apiInstance->suspendCapacityAsync($tenantId, $analyticsApiCapacitiesV1SuspendCapacityRequest);
} catch (Exception $e) {
    echo 'Exception when calling CapacitiesApi->suspendCapacityAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **analyticsApiCapacitiesV1SuspendCapacityRequest** | [**\EdGraph\PlatformClient\Model\AnalyticsApiCapacitiesV1SuspendCapacityRequest**](../Model/AnalyticsApiCapacitiesV1SuspendCapacityRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
