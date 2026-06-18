# EdGraph\PlatformClient\UsersSectionsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addUserSection()**](UsersSectionsApi.md#addUserSection) | **POST** /tenants/{tenantId}/users/{userId}/sections | Adds a Section to a user. |
| [**addUserSectionBulk()**](UsersSectionsApi.md#addUserSectionBulk) | **POST** /tenants/{tenantId}/users/{userId}/sections/bulk | Adds Sections to a user in bulk. |
| [**getUserSections()**](UsersSectionsApi.md#getUserSections) | **GET** /tenants/{tenantId}/users/{userId}/sections | Gets the Sections of a user. |
| [**removeUserSection()**](UsersSectionsApi.md#removeUserSection) | **DELETE** /tenants/{tenantId}/users/{userId}/sections/{userSectionId} | Removes a Section from a user. |
| [**removeUserSectionBulk()**](UsersSectionsApi.md#removeUserSectionBulk) | **DELETE** /tenants/{tenantId}/users/{userId}/sections/bulk | Removes Sections from a user in bulk. |
| [**updateUserSection()**](UsersSectionsApi.md#updateUserSection) | **PUT** /tenants/{tenantId}/users/{userId}/sections/{userSectionId} | Updates the Section of a user. |
| [**updateUserSectionBulk()**](UsersSectionsApi.md#updateUserSectionBulk) | **PUT** /tenants/{tenantId}/users/{userId}/sections/bulk | Updates the Section of a user in bulk. |


## `addUserSection()`

```php
addUserSection($tenantId, $userId, $identityApiUserV1AddSectionRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1SectionAddedResponse
```

Adds a Section to a user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersSectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$identityApiUserV1AddSectionRequest = new \EdGraph\PlatformClient\Model\IdentityApiUserV1AddSectionRequest(); // \EdGraph\PlatformClient\Model\IdentityApiUserV1AddSectionRequest | 

try {
    $result = $apiInstance->addUserSection($tenantId, $userId, $identityApiUserV1AddSectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersSectionsApi->addUserSection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **identityApiUserV1AddSectionRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiUserV1AddSectionRequest**](../Model/IdentityApiUserV1AddSectionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1SectionAddedResponse**](../Model/IdentityApiUserV1SectionAddedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `addUserSectionBulk()`

```php
addUserSectionBulk($tenantId, $userId, $identityApiUserV1AddSectionBulkRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1SectionAddedBulkResponse
```

Adds Sections to a user in bulk.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersSectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$identityApiUserV1AddSectionBulkRequest = new \EdGraph\PlatformClient\Model\IdentityApiUserV1AddSectionBulkRequest(); // \EdGraph\PlatformClient\Model\IdentityApiUserV1AddSectionBulkRequest | 

try {
    $result = $apiInstance->addUserSectionBulk($tenantId, $userId, $identityApiUserV1AddSectionBulkRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersSectionsApi->addUserSectionBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **identityApiUserV1AddSectionBulkRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiUserV1AddSectionBulkRequest**](../Model/IdentityApiUserV1AddSectionBulkRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1SectionAddedBulkResponse**](../Model/IdentityApiUserV1SectionAddedBulkResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getUserSections()`

```php
getUserSections($tenantId, $userId): \EdGraph\PlatformClient\Model\IdentityApiUserV1GetSectionsResponse
```

Gets the Sections of a user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersSectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 

try {
    $result = $apiInstance->getUserSections($tenantId, $userId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersSectionsApi->getUserSections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1GetSectionsResponse**](../Model/IdentityApiUserV1GetSectionsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeUserSection()`

```php
removeUserSection($tenantId, $userId, $userSectionId): \EdGraph\PlatformClient\Model\IdentityApiUserV1SectionRemovedResponse
```

Removes a Section from a user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersSectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$userSectionId = 'userSectionId_example'; // string | 

try {
    $result = $apiInstance->removeUserSection($tenantId, $userId, $userSectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersSectionsApi->removeUserSection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **userSectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1SectionRemovedResponse**](../Model/IdentityApiUserV1SectionRemovedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeUserSectionBulk()`

```php
removeUserSectionBulk($tenantId, $userId, $identityApiUserV1RemoveSectionBulkRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1SectionRemovedBulkResponse
```

Removes Sections from a user in bulk.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersSectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$identityApiUserV1RemoveSectionBulkRequest = new \EdGraph\PlatformClient\Model\IdentityApiUserV1RemoveSectionBulkRequest(); // \EdGraph\PlatformClient\Model\IdentityApiUserV1RemoveSectionBulkRequest | 

try {
    $result = $apiInstance->removeUserSectionBulk($tenantId, $userId, $identityApiUserV1RemoveSectionBulkRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersSectionsApi->removeUserSectionBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **identityApiUserV1RemoveSectionBulkRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiUserV1RemoveSectionBulkRequest**](../Model/IdentityApiUserV1RemoveSectionBulkRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1SectionRemovedBulkResponse**](../Model/IdentityApiUserV1SectionRemovedBulkResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateUserSection()`

```php
updateUserSection($tenantId, $userId, $userSectionId, $identityApiUserV1UpdateSectionRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1SectionUpdatedResponse
```

Updates the Section of a user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersSectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$userSectionId = 'userSectionId_example'; // string | 
$identityApiUserV1UpdateSectionRequest = new \EdGraph\PlatformClient\Model\IdentityApiUserV1UpdateSectionRequest(); // \EdGraph\PlatformClient\Model\IdentityApiUserV1UpdateSectionRequest | 

try {
    $result = $apiInstance->updateUserSection($tenantId, $userId, $userSectionId, $identityApiUserV1UpdateSectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersSectionsApi->updateUserSection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **userSectionId** | **string**|  | |
| **identityApiUserV1UpdateSectionRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiUserV1UpdateSectionRequest**](../Model/IdentityApiUserV1UpdateSectionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1SectionUpdatedResponse**](../Model/IdentityApiUserV1SectionUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateUserSectionBulk()`

```php
updateUserSectionBulk($tenantId, $userId, $identityApiUserV1UpdateSectionBulkRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1SectionUpdatedBulkResponse
```

Updates the Section of a user in bulk.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\UsersSectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$userId = 'userId_example'; // string | 
$identityApiUserV1UpdateSectionBulkRequest = new \EdGraph\PlatformClient\Model\IdentityApiUserV1UpdateSectionBulkRequest(); // \EdGraph\PlatformClient\Model\IdentityApiUserV1UpdateSectionBulkRequest | 

try {
    $result = $apiInstance->updateUserSectionBulk($tenantId, $userId, $identityApiUserV1UpdateSectionBulkRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersSectionsApi->updateUserSectionBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |
| **identityApiUserV1UpdateSectionBulkRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiUserV1UpdateSectionBulkRequest**](../Model/IdentityApiUserV1UpdateSectionBulkRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1SectionUpdatedBulkResponse**](../Model/IdentityApiUserV1SectionUpdatedBulkResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
