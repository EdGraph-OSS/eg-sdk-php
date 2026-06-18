# EdGraph\PlatformClient\ChangeLogsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllChangesAsync()**](ChangeLogsApi.md#getAllChangesAsync) | **GET** /tenants/{tenantId}/changes |  |


## `getAllChangesAsync()`

```php
getAllChangesAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\ChangeLogChangeV1ChangeLogResponsePaginatedItemsViewModel
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ChangeLogsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$pageSize = 10; // int
$pageIndex = 0; // int
$orderBy = ''; // string
$filter = ''; // string

try {
    $result = $apiInstance->getAllChangesAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChangeLogsApi->getAllChangesAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\ChangeLogChangeV1ChangeLogResponsePaginatedItemsViewModel**](../Model/ChangeLogChangeV1ChangeLogResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
