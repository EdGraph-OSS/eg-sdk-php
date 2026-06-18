# EdGraph\PlatformClient\SubscriptionsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTenantSubscriptionAsync()**](SubscriptionsApi.md#createTenantSubscriptionAsync) | **POST** /tenants/{tenantId}/subscriptions | Creates a new subscription |
| [**getAllTenantSubscriptionApplications()**](SubscriptionsApi.md#getAllTenantSubscriptionApplications) | **GET** /tenants/{tenantId}/subscriptions/applications | Retrieves a list of applications available for subscription. |
| [**getAllTenantSubscriptionsAsync()**](SubscriptionsApi.md#getAllTenantSubscriptionsAsync) | **GET** /tenants/{tenantId}/subscriptions | Retrieves a list of subscriptions associated to this tenant |
| [**getTenantSubscriptionProfileByIdAsync()**](SubscriptionsApi.md#getTenantSubscriptionProfileByIdAsync) | **GET** /tenants/{tenantId}/subscriptions/{subscriptionId} | Retrieves a subscription |
| [**updateTenantSubscriptionAsync()**](SubscriptionsApi.md#updateTenantSubscriptionAsync) | **PUT** /tenants/{tenantId}/subscriptions/{subscriptionId} | Updates a subscription |


## `createTenantSubscriptionAsync()`

```php
createTenantSubscriptionAsync($tenantId, $tenantApiTenantV1CreateSubscriptionRequest): \EdGraph\PlatformClient\Model\TenantApiTenantV1SubscriptionCreatedResponse
```

Creates a new subscription

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SubscriptionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$tenantApiTenantV1CreateSubscriptionRequest = new \EdGraph\PlatformClient\Model\TenantApiTenantV1CreateSubscriptionRequest(); // \EdGraph\PlatformClient\Model\TenantApiTenantV1CreateSubscriptionRequest | 

try {
    $result = $apiInstance->createTenantSubscriptionAsync($tenantId, $tenantApiTenantV1CreateSubscriptionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionsApi->createTenantSubscriptionAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **tenantApiTenantV1CreateSubscriptionRequest** | [**\EdGraph\PlatformClient\Model\TenantApiTenantV1CreateSubscriptionRequest**](../Model/TenantApiTenantV1CreateSubscriptionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1SubscriptionCreatedResponse**](../Model/TenantApiTenantV1SubscriptionCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllTenantSubscriptionApplications()`

```php
getAllTenantSubscriptionApplications($tenantId, $pageIndex, $pageSize, $orderBy): \EdGraph\PlatformClient\Model\ApplicationApiApplicationV1PaginatedItemsResponse
```

Retrieves a list of applications available for subscription.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SubscriptionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = 'orderBy_example'; // string | 

try {
    $result = $apiInstance->getAllTenantSubscriptionApplications($tenantId, $pageIndex, $pageSize, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionsApi->getAllTenantSubscriptionApplications: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ApplicationApiApplicationV1PaginatedItemsResponse**](../Model/ApplicationApiApplicationV1PaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllTenantSubscriptionsAsync()`

```php
getAllTenantSubscriptionsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionListResponseDtoPaginatedItemsViewModel
```

Retrieves a list of subscriptions associated to this tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SubscriptionsApi(
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
    $result = $apiInstance->getAllTenantSubscriptionsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionsApi->getAllTenantSubscriptionsAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionListResponseDtoPaginatedItemsViewModel**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionListResponseDtoPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantSubscriptionProfileByIdAsync()`

```php
getTenantSubscriptionProfileByIdAsync($tenantId, $subscriptionId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionProfileResponseDto
```

Retrieves a subscription

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SubscriptionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$subscriptionId = 'subscriptionId_example'; // string | 

try {
    $result = $apiInstance->getTenantSubscriptionProfileByIdAsync($tenantId, $subscriptionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionsApi->getTenantSubscriptionProfileByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **subscriptionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionProfileResponseDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionProfileResponseDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTenantSubscriptionAsync()`

```php
updateTenantSubscriptionAsync($tenantId, $subscriptionId, $tenantApiTenantV1UpdateSubscriptionRequest): \EdGraph\PlatformClient\Model\TenantApiTenantV1SubscriptionUpdatedResponse
```

Updates a subscription

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SubscriptionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$subscriptionId = 'subscriptionId_example'; // string | 
$tenantApiTenantV1UpdateSubscriptionRequest = new \EdGraph\PlatformClient\Model\TenantApiTenantV1UpdateSubscriptionRequest(); // \EdGraph\PlatformClient\Model\TenantApiTenantV1UpdateSubscriptionRequest | 

try {
    $result = $apiInstance->updateTenantSubscriptionAsync($tenantId, $subscriptionId, $tenantApiTenantV1UpdateSubscriptionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionsApi->updateTenantSubscriptionAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **subscriptionId** | **string**|  | |
| **tenantApiTenantV1UpdateSubscriptionRequest** | [**\EdGraph\PlatformClient\Model\TenantApiTenantV1UpdateSubscriptionRequest**](../Model/TenantApiTenantV1UpdateSubscriptionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiTenantV1SubscriptionUpdatedResponse**](../Model/TenantApiTenantV1SubscriptionUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
