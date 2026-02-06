# EdGraph\PlatformClient\WebhooksApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createWebhookAsync()**](WebhooksApi.md#createWebhookAsync) | **POST** /tenants/{tenantId}/webhooks | Creates a new Webhook |
| [**deleteWebhookAsync()**](WebhooksApi.md#deleteWebhookAsync) | **DELETE** /tenants/{tenantId}/webhooks/{webhookId} | Removes a webhook. |
| [**getAllWebhookSubscriptionsAsync()**](WebhooksApi.md#getAllWebhookSubscriptionsAsync) | **GET** /tenants/{tenantId}/webhooks/events |  |
| [**getAllWebhooksAsync()**](WebhooksApi.md#getAllWebhooksAsync) | **GET** /tenants/{tenantId}/webhooks | Retrieves a list of webhooks. |
| [**getWebhookByIdAsync()**](WebhooksApi.md#getWebhookByIdAsync) | **GET** /tenants/{tenantId}/webhooks/{webhookId} | Retrieves a webhook by ID. |
| [**updateWebhookAsync()**](WebhooksApi.md#updateWebhookAsync) | **PUT** /tenants/{tenantId}/webhooks/{webhookId} | Updates a webhook |


## `createWebhookAsync()`

```php
createWebhookAsync($tenantId, $tenantApiWebhookV1CreateWebhookRequest): \EdGraph\PlatformClient\Model\TenantApiWebhookV1WebhookIdResponse
```

Creates a new Webhook

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$tenantApiWebhookV1CreateWebhookRequest = new \EdGraph\PlatformClient\Model\TenantApiWebhookV1CreateWebhookRequest(); // \EdGraph\PlatformClient\Model\TenantApiWebhookV1CreateWebhookRequest | 

try {
    $result = $apiInstance->createWebhookAsync($tenantId, $tenantApiWebhookV1CreateWebhookRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->createWebhookAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **tenantApiWebhookV1CreateWebhookRequest** | [**\EdGraph\PlatformClient\Model\TenantApiWebhookV1CreateWebhookRequest**](../Model/TenantApiWebhookV1CreateWebhookRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiWebhookV1WebhookIdResponse**](../Model/TenantApiWebhookV1WebhookIdResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteWebhookAsync()`

```php
deleteWebhookAsync($tenantId, $webhookId): \EdGraph\PlatformClient\Model\TenantApiWebhookV1WebhookIdResponse
```

Removes a webhook.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$webhookId = 'webhookId_example'; // string | 

try {
    $result = $apiInstance->deleteWebhookAsync($tenantId, $webhookId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->deleteWebhookAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **webhookId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiWebhookV1WebhookIdResponse**](../Model/TenantApiWebhookV1WebhookIdResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllWebhookSubscriptionsAsync()`

```php
getAllWebhookSubscriptionsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiWebhookV1PaginatedWebhookEventItemsResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$pageSize = 10; // int
$pageIndex = 0; // int
$orderBy = ''; // string
$filter = ''; // string

try {
    $result = $apiInstance->getAllWebhookSubscriptionsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->getAllWebhookSubscriptionsAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\TenantApiWebhookV1PaginatedWebhookEventItemsResponse**](../Model/TenantApiWebhookV1PaginatedWebhookEventItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllWebhooksAsync()`

```php
getAllWebhooksAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiWebhookV1PaginatedItemsResponse
```

Retrieves a list of webhooks.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\WebhooksApi(
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
    $result = $apiInstance->getAllWebhooksAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->getAllWebhooksAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\TenantApiWebhookV1PaginatedItemsResponse**](../Model/TenantApiWebhookV1PaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getWebhookByIdAsync()`

```php
getWebhookByIdAsync($tenantId, $webhookId): \EdGraph\PlatformClient\Model\TenantApiWebhookV1WebhookResponse
```

Retrieves a webhook by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$webhookId = 'webhookId_example'; // string | 

try {
    $result = $apiInstance->getWebhookByIdAsync($tenantId, $webhookId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->getWebhookByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **webhookId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiWebhookV1WebhookResponse**](../Model/TenantApiWebhookV1WebhookResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateWebhookAsync()`

```php
updateWebhookAsync($tenantId, $webhookId, $tenantApiWebhookV1UpdateWebhookRequest): \EdGraph\PlatformClient\Model\TenantApiWebhookV1WebhookIdResponse
```

Updates a webhook

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$webhookId = 'webhookId_example'; // string | 
$tenantApiWebhookV1UpdateWebhookRequest = new \EdGraph\PlatformClient\Model\TenantApiWebhookV1UpdateWebhookRequest(); // \EdGraph\PlatformClient\Model\TenantApiWebhookV1UpdateWebhookRequest | 

try {
    $result = $apiInstance->updateWebhookAsync($tenantId, $webhookId, $tenantApiWebhookV1UpdateWebhookRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->updateWebhookAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **webhookId** | **string**|  | |
| **tenantApiWebhookV1UpdateWebhookRequest** | [**\EdGraph\PlatformClient\Model\TenantApiWebhookV1UpdateWebhookRequest**](../Model/TenantApiWebhookV1UpdateWebhookRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiWebhookV1WebhookIdResponse**](../Model/TenantApiWebhookV1WebhookIdResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
