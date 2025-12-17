# EdGraph\PlatformClient\RegistrationsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getOnboardingApplicationsAsync()**](RegistrationsApi.md#getOnboardingApplicationsAsync) | **GET** /public/applications | Gets a list of applications available for registration/onboarding |
| [**getRegistrationApprovalStatusAsync()**](RegistrationsApi.md#getRegistrationApprovalStatusAsync) | **GET** /registrations/{registrationId} | Gets the approval status of a registration |
| [**submitTenantRegistrationAsync()**](RegistrationsApi.md#submitTenantRegistrationAsync) | **POST** /registrations | Submits a tenant&#39;s registration request |


## `getOnboardingApplicationsAsync()`

```php
getOnboardingApplicationsAsync($pageSize, $pageIndex, $orderBy): \EdGraph\PlatformClient\Model\ApplicationApiApplicationV1PaginatedItemsResponse
```

Gets a list of applications available for registration/onboarding

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\RegistrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 

try {
    $result = $apiInstance->getOnboardingApplicationsAsync($pageSize, $pageIndex, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RegistrationsApi->getOnboardingApplicationsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |

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

## `getRegistrationApprovalStatusAsync()`

```php
getRegistrationApprovalStatusAsync($registrationId): \EdGraph\PlatformClient\Model\RegistrationApiRegistrationV2ApprovalStatus
```

Gets the approval status of a registration

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\RegistrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$registrationId = 'registrationId_example'; // string

try {
    $result = $apiInstance->getRegistrationApprovalStatusAsync($registrationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RegistrationsApi->getRegistrationApprovalStatusAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registrationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\RegistrationApiRegistrationV2ApprovalStatus**](../Model/RegistrationApiRegistrationV2ApprovalStatus.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `submitTenantRegistrationAsync()`

```php
submitTenantRegistrationAsync($registrationApiRegistrationV2SubmitTenantRegistrationRequest): string
```

Submits a tenant's registration request

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\RegistrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$registrationApiRegistrationV2SubmitTenantRegistrationRequest = new \EdGraph\PlatformClient\Model\RegistrationApiRegistrationV2SubmitTenantRegistrationRequest(); // \EdGraph\PlatformClient\Model\RegistrationApiRegistrationV2SubmitTenantRegistrationRequest | 

try {
    $result = $apiInstance->submitTenantRegistrationAsync($registrationApiRegistrationV2SubmitTenantRegistrationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RegistrationsApi->submitTenantRegistrationAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registrationApiRegistrationV2SubmitTenantRegistrationRequest** | [**\EdGraph\PlatformClient\Model\RegistrationApiRegistrationV2SubmitTenantRegistrationRequest**](../Model/RegistrationApiRegistrationV2SubmitTenantRegistrationRequest.md)|  | [optional] |

### Return type

**string**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
