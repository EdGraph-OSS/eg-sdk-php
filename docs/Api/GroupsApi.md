# EdGraph\PlatformClient\GroupsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addUsersToGroupAsync()**](GroupsApi.md#addUsersToGroupAsync) | **POST** /tenants/{tenantId}/analytics/groups/{groupId}/users/bulk | Adds users to group. |
| [**createAnalyticsPowerBiGroup()**](GroupsApi.md#createAnalyticsPowerBiGroup) | **POST** /tenants/{tenantId}/analytics/groups | Creates a group. |
| [**deleteAnalyticsPowerBiGroup()**](GroupsApi.md#deleteAnalyticsPowerBiGroup) | **DELETE** /tenants/{tenantId}/analytics/groups/{groupId} | Deletes a group. |
| [**getAnalyticsPowerBiGroupUsers()**](GroupsApi.md#getAnalyticsPowerBiGroupUsers) | **GET** /tenants/{tenantId}/analytics/groups/{groupId}/users | Retrieves all users for a specific group. |
| [**getGroupsAsync()**](GroupsApi.md#getGroupsAsync) | **GET** /tenants/{tenantId}/analytics/groups | Retrieves a list of groups. |


## `addUsersToGroupAsync()`

```php
addUsersToGroupAsync($tenantId, $groupId, $analyticsApiGroupsV1AddGroupUsersRequest)
```

Adds users to group.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\GroupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$groupId = 'groupId_example'; // string | 
$analyticsApiGroupsV1AddGroupUsersRequest = new \EdGraph\PlatformClient\Model\AnalyticsApiGroupsV1AddGroupUsersRequest(); // \EdGraph\PlatformClient\Model\AnalyticsApiGroupsV1AddGroupUsersRequest | 

try {
    $apiInstance->addUsersToGroupAsync($tenantId, $groupId, $analyticsApiGroupsV1AddGroupUsersRequest);
} catch (Exception $e) {
    echo 'Exception when calling GroupsApi->addUsersToGroupAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **groupId** | **string**|  | |
| **analyticsApiGroupsV1AddGroupUsersRequest** | [**\EdGraph\PlatformClient\Model\AnalyticsApiGroupsV1AddGroupUsersRequest**](../Model/AnalyticsApiGroupsV1AddGroupUsersRequest.md)|  | [optional] |

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

## `createAnalyticsPowerBiGroup()`

```php
createAnalyticsPowerBiGroup($tenantId, $analyticsApiGroupsV1CreateGroupRequest): \EdGraph\PlatformClient\Model\AnalyticsApiGroupsV1GroupResponse
```

Creates a group.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\GroupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$analyticsApiGroupsV1CreateGroupRequest = new \EdGraph\PlatformClient\Model\AnalyticsApiGroupsV1CreateGroupRequest(); // \EdGraph\PlatformClient\Model\AnalyticsApiGroupsV1CreateGroupRequest | 

try {
    $result = $apiInstance->createAnalyticsPowerBiGroup($tenantId, $analyticsApiGroupsV1CreateGroupRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupsApi->createAnalyticsPowerBiGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **analyticsApiGroupsV1CreateGroupRequest** | [**\EdGraph\PlatformClient\Model\AnalyticsApiGroupsV1CreateGroupRequest**](../Model/AnalyticsApiGroupsV1CreateGroupRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiGroupsV1GroupResponse**](../Model/AnalyticsApiGroupsV1GroupResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteAnalyticsPowerBiGroup()`

```php
deleteAnalyticsPowerBiGroup($tenantId, $groupId)
```

Deletes a group.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\GroupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$groupId = 'groupId_example'; // string | 

try {
    $apiInstance->deleteAnalyticsPowerBiGroup($tenantId, $groupId);
} catch (Exception $e) {
    echo 'Exception when calling GroupsApi->deleteAnalyticsPowerBiGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **groupId** | **string**|  | |

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

## `getAnalyticsPowerBiGroupUsers()`

```php
getAnalyticsPowerBiGroupUsers($tenantId, $groupId, $skipFirstN, $topFirstN): \EdGraph\PlatformClient\Model\AnalyticsApiGroupsV1GroupUsersResponse
```

Retrieves all users for a specific group.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\GroupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$groupId = 'groupId_example'; // string | 
$skipFirstN = 56; // int | 
$topFirstN = 56; // int | 

try {
    $result = $apiInstance->getAnalyticsPowerBiGroupUsers($tenantId, $groupId, $skipFirstN, $topFirstN);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupsApi->getAnalyticsPowerBiGroupUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **groupId** | **string**|  | |
| **skipFirstN** | **int**|  | [optional] |
| **topFirstN** | **int**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiGroupsV1GroupUsersResponse**](../Model/AnalyticsApiGroupsV1GroupUsersResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGroupsAsync()`

```php
getGroupsAsync($tenantId, $filter): \EdGraph\PlatformClient\Model\AnalyticsApiGroupsV1GroupsResponse
```

Retrieves a list of groups.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\GroupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$filter = 'filter_example'; // string | 

try {
    $result = $apiInstance->getGroupsAsync($tenantId, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupsApi->getGroupsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **filter** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiGroupsV1GroupsResponse**](../Model/AnalyticsApiGroupsV1GroupsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
