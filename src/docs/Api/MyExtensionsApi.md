# EdGraph\PlatformClient\MyExtensionsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**removeUserExtension()**](MyExtensionsApi.md#removeUserExtension) | **DELETE** /me/extensions/{code} | Removes a user&#39;s profile extension. |
| [**setUserExtension()**](MyExtensionsApi.md#setUserExtension) | **POST** /me/extensions | Creates or update a user&#39;s profile extension. |


## `removeUserExtension()`

```php
removeUserExtension($code): \EdGraph\PlatformClient\Model\IdentityApiUserV1UserExtensionRemovedResponse
```

Removes a user's profile extension.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MyExtensionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string | 

try {
    $result = $apiInstance->removeUserExtension($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyExtensionsApi->removeUserExtension: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1UserExtensionRemovedResponse**](../Model/IdentityApiUserV1UserExtensionRemovedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setUserExtension()`

```php
setUserExtension($identityApiUserV1SetUserExtensionRequest): \EdGraph\PlatformClient\Model\IdentityApiUserV1UserExtensionSetResponse
```

Creates or update a user's profile extension.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\MyExtensionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$identityApiUserV1SetUserExtensionRequest = new \EdGraph\PlatformClient\Model\IdentityApiUserV1SetUserExtensionRequest(); // \EdGraph\PlatformClient\Model\IdentityApiUserV1SetUserExtensionRequest | 

try {
    $result = $apiInstance->setUserExtension($identityApiUserV1SetUserExtensionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyExtensionsApi->setUserExtension: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **identityApiUserV1SetUserExtensionRequest** | [**\EdGraph\PlatformClient\Model\IdentityApiUserV1SetUserExtensionRequest**](../Model/IdentityApiUserV1SetUserExtensionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1UserExtensionSetResponse**](../Model/IdentityApiUserV1UserExtensionSetResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
