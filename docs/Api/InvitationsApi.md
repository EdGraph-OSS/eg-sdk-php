# EdGraph\PlatformClient\InvitationsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteTenantInvitationAsync()**](InvitationsApi.md#deleteTenantInvitationAsync) | **DELETE** /tenants/{tenantId}/invitations/{invitationId} | Deletes an invitation |
| [**getAllTenantInvitationsAsync()**](InvitationsApi.md#getAllTenantInvitationsAsync) | **GET** /tenants/{tenantId}/invitations | Retrieves a list of invitations associated to this tenant |
| [**getTenantInvitationByIdAsync()**](InvitationsApi.md#getTenantInvitationByIdAsync) | **GET** /tenants/{tenantId}/invitations/{invitationId} | Retrieves a specific invitation |
| [**sendTenantInvitationAsync()**](InvitationsApi.md#sendTenantInvitationAsync) | **POST** /tenants/{tenantId}/invitations | Creates and sends an invitation to a user |


## `deleteTenantInvitationAsync()`

```php
deleteTenantInvitationAsync($tenantId, $invitationId)
```

Deletes an invitation

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InvitationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$invitationId = 'invitationId_example'; // string | 

try {
    $apiInstance->deleteTenantInvitationAsync($tenantId, $invitationId);
} catch (Exception $e) {
    echo 'Exception when calling InvitationsApi->deleteTenantInvitationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **invitationId** | **string**|  | |

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

## `getAllTenantInvitationsAsync()`

```php
getAllTenantInvitationsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel
```

Retrieves a list of invitations associated to this tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InvitationsApi(
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
    $result = $apiInstance->getAllTenantInvitationsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvitationsApi->getAllTenantInvitationsAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel**](../Model/IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTenantInvitationByIdAsync()`

```php
getTenantInvitationByIdAsync($tenantId, $invitationId): \EdGraph\PlatformClient\Model\IdentityApiInvitationV1InvitationResponse
```

Retrieves a specific invitation

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InvitationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$invitationId = 'invitationId_example'; // string | 

try {
    $result = $apiInstance->getTenantInvitationByIdAsync($tenantId, $invitationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvitationsApi->getTenantInvitationByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **invitationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiInvitationV1InvitationResponse**](../Model/IdentityApiInvitationV1InvitationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendTenantInvitationAsync()`

```php
sendTenantInvitationAsync($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest): \EdGraph\PlatformClient\Model\IdentityApiInvitationV1InvitationSentResponse
```

Creates and sends an invitation to a user

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\InvitationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest | 

try {
    $result = $apiInstance->sendTenantInvitationAsync($tenantId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvitationsApi->sendTenantInvitationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiInvitationV1InvitationSentResponse**](../Model/IdentityApiInvitationV1InvitationSentResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
