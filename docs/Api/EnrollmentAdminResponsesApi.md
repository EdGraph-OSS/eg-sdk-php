# EdGraph\PlatformClient\EnrollmentAdminResponsesApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getEnrollmentApplicationResponse()**](EnrollmentAdminResponsesApi.md#getEnrollmentApplicationResponse) | **GET** /tenants/{tenantId}/enrollmentadmin/responses/{responseId} | Gets an Enrollment Application Response. |
| [**getEnrollmentApplicationResponses()**](EnrollmentAdminResponsesApi.md#getEnrollmentApplicationResponses) | **GET** /tenants/{tenantId}/enrollmentadmin/responses | Searches Enrollment Application Responses. |


## `getEnrollmentApplicationResponse()`

```php
getEnrollmentApplicationResponse($tenantId, $responseId): \EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse
```

Gets an Enrollment Application Response.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnrollmentAdminResponsesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$responseId = 'responseId_example'; // string | 

try {
    $result = $apiInstance->getEnrollmentApplicationResponse($tenantId, $responseId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnrollmentAdminResponsesApi->getEnrollmentApplicationResponse: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **responseId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse**](../Model/EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEnrollmentApplicationResponses()`

```php
getEnrollmentApplicationResponses($tenantId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponsesSearchResponse
```

Searches Enrollment Application Responses.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnrollmentAdminResponsesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 56; // int | 
$pageSize = 56; // int | 
$filter = 'filter_example'; // string | 
$orderBy = 'orderBy_example'; // string | 

try {
    $result = $apiInstance->getEnrollmentApplicationResponses($tenantId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnrollmentAdminResponsesApi->getEnrollmentApplicationResponses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] |
| **pageSize** | **int**|  | [optional] |
| **filter** | **string**|  | [optional] |
| **orderBy** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponsesSearchResponse**](../Model/EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponsesSearchResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
