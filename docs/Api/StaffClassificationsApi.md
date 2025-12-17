# EdGraph\PlatformClient\StaffClassificationsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createStaffClassification()**](StaffClassificationsApi.md#createStaffClassification) | **POST** /tenants/{tenantId}/staffclassifications | Creates a StaffClassification. |
| [**deleteStaffClassification()**](StaffClassificationsApi.md#deleteStaffClassification) | **DELETE** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Deletes a StaffClassification. |
| [**getStaffClassificationById()**](StaffClassificationsApi.md#getStaffClassificationById) | **GET** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Retrieves a StaffClassification by ID. |
| [**getStaffClassifications()**](StaffClassificationsApi.md#getStaffClassifications) | **GET** /tenants/{tenantId}/staffclassifications | Retrieves a list of StaffClassifications. |
| [**getStaffClassificationsNamespaces()**](StaffClassificationsApi.md#getStaffClassificationsNamespaces) | **GET** /tenants/{tenantId}/staffclassifications/namespaces | Retrieves a list of unique Staff Classification Namespaces. |
| [**updateStaffClassification()**](StaffClassificationsApi.md#updateStaffClassification) | **PUT** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Updates a StaffClassification. |


## `createStaffClassification()`

```php
createStaffClassification($tenantId, $identityApiStaffClassificationV1CreateStaffClassificationRequest): \EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1StaffClassificationCreatedResponse
```

Creates a StaffClassification.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\StaffClassificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$identityApiStaffClassificationV1CreateStaffClassificationRequest = new \EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1CreateStaffClassificationRequest(); // \EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1CreateStaffClassificationRequest | 

try {
    $result = $apiInstance->createStaffClassification($tenantId, $identityApiStaffClassificationV1CreateStaffClassificationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StaffClassificationsApi->createStaffClassification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **identityApiStaffClassificationV1CreateStaffClassificationRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1CreateStaffClassificationRequest**](../Model/IdentityApiStaffClassificationV1CreateStaffClassificationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1StaffClassificationCreatedResponse**](../Model/IdentityApiStaffClassificationV1StaffClassificationCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteStaffClassification()`

```php
deleteStaffClassification($tenantId, $staffClassificationId): \EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1StaffClassificationDeletedResponse
```

Deletes a StaffClassification.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\StaffClassificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$staffClassificationId = 'staffClassificationId_example'; // string | 

try {
    $result = $apiInstance->deleteStaffClassification($tenantId, $staffClassificationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StaffClassificationsApi->deleteStaffClassification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **staffClassificationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1StaffClassificationDeletedResponse**](../Model/IdentityApiStaffClassificationV1StaffClassificationDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStaffClassificationById()`

```php
getStaffClassificationById($tenantId, $staffClassificationId): \EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1StaffClassificationResponse
```

Retrieves a StaffClassification by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\StaffClassificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$staffClassificationId = 'staffClassificationId_example'; // string | 

try {
    $result = $apiInstance->getStaffClassificationById($tenantId, $staffClassificationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StaffClassificationsApi->getStaffClassificationById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **staffClassificationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1StaffClassificationResponse**](../Model/IdentityApiStaffClassificationV1StaffClassificationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStaffClassifications()`

```php
getStaffClassifications($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1GetStaffClassificationsResponse
```

Retrieves a list of StaffClassifications.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\StaffClassificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getStaffClassifications($tenantId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StaffClassificationsApi->getStaffClassifications: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1GetStaffClassificationsResponse**](../Model/IdentityApiStaffClassificationV1GetStaffClassificationsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStaffClassificationsNamespaces()`

```php
getStaffClassificationsNamespaces($tenantId, $pageIndex, $pageSize, $filter): \EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse
```

Retrieves a list of unique Staff Classification Namespaces.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\StaffClassificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getStaffClassificationsNamespaces($tenantId, $pageIndex, $pageSize, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StaffClassificationsApi->getStaffClassificationsNamespaces: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse**](../Model/IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateStaffClassification()`

```php
updateStaffClassification($tenantId, $staffClassificationId, $identityApiStaffClassificationV1UpdateStaffClassificationRequest): \EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse
```

Updates a StaffClassification.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\StaffClassificationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$staffClassificationId = 'staffClassificationId_example'; // string | 
$identityApiStaffClassificationV1UpdateStaffClassificationRequest = new \EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1UpdateStaffClassificationRequest(); // \EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1UpdateStaffClassificationRequest | 

try {
    $result = $apiInstance->updateStaffClassification($tenantId, $staffClassificationId, $identityApiStaffClassificationV1UpdateStaffClassificationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StaffClassificationsApi->updateStaffClassification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **staffClassificationId** | **string**|  | |
| **identityApiStaffClassificationV1UpdateStaffClassificationRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1UpdateStaffClassificationRequest**](../Model/IdentityApiStaffClassificationV1UpdateStaffClassificationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse**](../Model/IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
