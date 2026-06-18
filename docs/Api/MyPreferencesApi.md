# EdGraph\PlatformClient\MyPreferencesApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getUserPreferences()**](MyPreferencesApi.md#getUserPreferences) | **GET** /me/preferences | Retrieves the user&#39;s preferences. |
| [**preference()**](MyPreferencesApi.md#preference) | **GET** /me/preferences/{code} | Retrieves a user&#39;s preference by code. |
| [**updateUserPreferenceAsync()**](MyPreferencesApi.md#updateUserPreferenceAsync) | **POST** /me/preferences | Creates or update a user&#39;s preference. |


## `getUserPreferences()`

```php
getUserPreferences($pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\IdentityApiUserV1GetUserPreferencesResponse
```

Retrieves the user's preferences.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MyPreferencesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = 'orderBy_example'; // string | 
$filter = 'filter_example'; // string | 

try {
    $result = $apiInstance->getUserPreferences($pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyPreferencesApi->getUserPreferences: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] |
| **filter** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1GetUserPreferencesResponse**](../Model/IdentityApiUserV1GetUserPreferencesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `preference()`

```php
preference($code): \EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheResponse
```

Retrieves a user's preference by code.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MyPreferencesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string | 

try {
    $result = $apiInstance->preference($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyPreferencesApi->preference: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheResponse**](../Model/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateUserPreferenceAsync()`

```php
updateUserPreferenceAsync($edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1UserPreferenceUpdatedResponse
```

Creates or update a user's preference.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MyPreferencesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest | 

try {
    $result = $apiInstance->updateUserPreferenceAsync($edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyPreferencesApi->updateUserPreferenceAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1UserPreferenceUpdatedResponse**](../Model/IdentityApiUserV1UserPreferenceUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
