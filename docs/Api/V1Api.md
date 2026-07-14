# EdGraph\PlatformClient\V1Api



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getStudentProfile()**](V1Api.md#getStudentProfile) | **GET** /tenants/{tenantId}/students/{id} | Returns the admin profile for a single student. |
| [**getStudents()**](V1Api.md#getStudents) | **GET** /tenants/{tenantId}/students | Returns a paginated list of students for the given tenant. |
| [**releaseUserLockout()**](V1Api.md#releaseUserLockout) | **PUT** /tenants/{tenantId}/users/{userId}/releaselockout |  |
| [**updateStudentContacts()**](V1Api.md#updateStudentContacts) | **PUT** /tenants/{tenantId}/{studentId}/contacts | Updates the contact overrides for a student. |


## `getStudentProfile()`

```php
getStudentProfile($tenantId, $id)
```

Returns the admin profile for a single student.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\V1Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$id = 'id_example'; // string

try {
    $apiInstance->getStudentProfile($tenantId, $id);
} catch (Exception $e) {
    echo 'Exception when calling V1Api->getStudentProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **id** | **string**|  | |

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

## `getStudents()`

```php
getStudents($tenantId, $campus, $pathway, $status, $pageIndex, $pageSize)
```

Returns a paginated list of students for the given tenant.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\V1Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$campus = 'campus_example'; // string
$pathway = 'pathway_example'; // string
$status = 'status_example'; // string
$pageIndex = 0; // int
$pageSize = 10; // int

try {
    $apiInstance->getStudents($tenantId, $campus, $pathway, $status, $pageIndex, $pageSize);
} catch (Exception $e) {
    echo 'Exception when calling V1Api->getStudents: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **campus** | **string**|  | [optional] |
| **pathway** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |

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

## `releaseUserLockout()`

```php
releaseUserLockout($tenantId, $userId): \EdGraph\PlatformClient\Model\IdentityApiUserV1ReleaseUserLockoutResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\V1Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$userId = 'userId_example'; // string

try {
    $result = $apiInstance->releaseUserLockout($tenantId, $userId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling V1Api->releaseUserLockout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **userId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1ReleaseUserLockoutResponse**](../Model/IdentityApiUserV1ReleaseUserLockoutResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateStudentContacts()`

```php
updateStudentContacts($tenantId, $studentId, $body)
```

Updates the contact overrides for a student.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\V1Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$studentId = 'studentId_example'; // string
$body = NULL; // mixed

try {
    $apiInstance->updateStudentContacts($tenantId, $studentId, $body);
} catch (Exception $e) {
    echo 'Exception when calling V1Api->updateStudentContacts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **studentId** | **string**|  | |
| **body** | **mixed**|  | [optional] |

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
