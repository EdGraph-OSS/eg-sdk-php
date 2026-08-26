# EdGraph\PlatformClient\EnrollmentAdminContactsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getEnrollmentContactById()**](EnrollmentAdminContactsApi.md#getEnrollmentContactById) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id} | Gets an Enrollment Contact by its record id, with its linked students. |
| [**getEnrollmentContacts()**](EnrollmentAdminContactsApi.md#getEnrollmentContacts) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts | Searches Enrollment Contacts. |


## `getEnrollmentContactById()`

```php
getEnrollmentContactById($tenantId, $id): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDto
```

Gets an Enrollment Contact by its record id, with its linked students.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnrollmentAdminContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$id = 'id_example'; // string | 

try {
    $result = $apiInstance->getEnrollmentContactById($tenantId, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnrollmentAdminContactsApi->getEnrollmentContactById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **id** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEnrollmentContacts()`

```php
getEnrollmentContacts($tenantId, $pageSize, $pageIndex, $orderBy, $filter, $search, $schoolCode): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDtoPaginatedItemsViewModel
```

Searches Enrollment Contacts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnrollmentAdminContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 50; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 
$search = ''; // string | Free-text match on contact name, email, or phone.
$schoolCode = ''; // string | Narrows to contacts with at least one linked student at this school.

try {
    $result = $apiInstance->getEnrollmentContacts($tenantId, $pageSize, $pageIndex, $orderBy, $filter, $search, $schoolCode);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnrollmentAdminContactsApi->getEnrollmentContacts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 50] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |
| **search** | **string**| Free-text match on contact name, email, or phone. | [optional] [default to &#39;&#39;] |
| **schoolCode** | **string**| Narrows to contacts with at least one linked student at this school. | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDtoPaginatedItemsViewModel**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDtoPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
