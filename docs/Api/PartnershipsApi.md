# EdGraph\PlatformClient\PartnershipsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllPartnerships()**](PartnershipsApi.md#getAllPartnerships) | **GET** /tenants/{tenantId}/partnerships | Retrieves a list of Partnerships. |
| [**getPartnershipById()**](PartnershipsApi.md#getPartnershipById) | **GET** /tenants/{tenantId}/partnerships/{partnershipId} | Retrieves a Partnership by ID. |


## `getAllPartnerships()`

```php
getAllPartnerships($tenantId, $pageIndex, $pageSize, $orderBy, $partnerTenantId, $partnershipType, $excludeSoftDeleted): \EdGraph\PlatformClient\Model\TenantApiPartnershipV1PaginatedItemsResponse
```

Retrieves a list of Partnerships.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\PartnershipsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = 'orderBy_example'; // string | 
$partnerTenantId = 'partnerTenantId_example'; // string | 
$partnershipType = array('partnershipType_example'); // string[] | 
$excludeSoftDeleted = true; // bool | 

try {
    $result = $apiInstance->getAllPartnerships($tenantId, $pageIndex, $pageSize, $orderBy, $partnerTenantId, $partnershipType, $excludeSoftDeleted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartnershipsApi->getAllPartnerships: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] |
| **partnerTenantId** | **string**|  | [optional] |
| **partnershipType** | [**string[]**](../Model/string.md)|  | [optional] |
| **excludeSoftDeleted** | **bool**|  | [optional] [default to true] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiPartnershipV1PaginatedItemsResponse**](../Model/TenantApiPartnershipV1PaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPartnershipById()`

```php
getPartnershipById($tenantId, $partnershipId, $excludeSoftDeleted): \EdGraph\PlatformClient\Model\TenantApiPartnershipV1PartnershipByIdResponse
```

Retrieves a Partnership by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\PartnershipsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$partnershipId = 'partnershipId_example'; // string | 
$excludeSoftDeleted = true; // bool | 

try {
    $result = $apiInstance->getPartnershipById($tenantId, $partnershipId, $excludeSoftDeleted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartnershipsApi->getPartnershipById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **partnershipId** | **string**|  | |
| **excludeSoftDeleted** | **bool**|  | [optional] [default to true] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiPartnershipV1PartnershipByIdResponse**](../Model/TenantApiPartnershipV1PartnershipByIdResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
