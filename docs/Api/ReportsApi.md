# EdGraph\PlatformClient\ReportsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createReportAsync()**](ReportsApi.md#createReportAsync) | **POST** /tenants/{tenantId}/analytics/reports | Creates a new report (Does not upload pbix file). |
| [**deleteReportAsync()**](ReportsApi.md#deleteReportAsync) | **DELETE** /tenants/{tenantId}/analytics/reports/{reportId} | Removes a report. |
| [**downloadReportAsync()**](ReportsApi.md#downloadReportAsync) | **GET** /tenants/{tenantId}/analytics/reports/download/{reportId}/{groupId} | Retrieves the PBIX for any report in the list in order to download |
| [**getAllTenantAnalyticsWorkspaceReportsAsync()**](ReportsApi.md#getAllTenantAnalyticsWorkspaceReportsAsync) | **GET** /tenants/{tenantId}/analytics/reports | Retrieves all reports. |
| [**getReportByIdAsync()**](ReportsApi.md#getReportByIdAsync) | **GET** /tenants/{tenantId}/analytics/reports/{reportId} | Retrieves a Report by ID. |
| [**syncLatestVersion()**](ReportsApi.md#syncLatestVersion) | **POST** /tenants/{tenantId}/analytics/reports/synclatestversion | Sync latest version |
| [**syncWorkspacesAsync()**](ReportsApi.md#syncWorkspacesAsync) | **POST** /tenants/{tenantId}/analytics/reports/sync | Triggers workspace, ODS and DW automation. |
| [**updateReportAsync()**](ReportsApi.md#updateReportAsync) | **PUT** /tenants/{tenantId}/analytics/reports/{reportId} | Updates a report. |


## `createReportAsync()`

```php
createReportAsync($tenantId, $file, $name, $shortDescription, $description, $tags, $isVisible, $version, $identityRequired, $rolesRequired, $state): \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportIdResponse
```

Creates a new report (Does not upload pbix file).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$file = "/path/to/file.txt"; // \SplFileObject
$name = 'name_example'; // string
$shortDescription = 'shortDescription_example'; // string
$description = 'description_example'; // string
$tags = 'tags_example'; // string
$isVisible = True; // bool
$version = 'version_example'; // string
$identityRequired = True; // bool
$rolesRequired = True; // bool
$state = 'state_example'; // string

try {
    $result = $apiInstance->createReportAsync($tenantId, $file, $name, $shortDescription, $description, $tags, $isVisible, $version, $identityRequired, $rolesRequired, $state);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->createReportAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **file** | **\SplFileObject****\SplFileObject**|  | [optional] |
| **name** | **string**|  | [optional] |
| **shortDescription** | **string**|  | [optional] |
| **description** | **string**|  | [optional] |
| **tags** | **string**|  | [optional] |
| **isVisible** | **bool**|  | [optional] |
| **version** | **string**|  | [optional] |
| **identityRequired** | **bool**|  | [optional] |
| **rolesRequired** | **bool**|  | [optional] |
| **state** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportIdResponse**](../Model/AnalyticsApiReportsV1ReportIdResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteReportAsync()`

```php
deleteReportAsync($tenantId, $reportId)
```

Removes a report.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportId = 'reportId_example'; // string | 

try {
    $apiInstance->deleteReportAsync($tenantId, $reportId);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->deleteReportAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportId** | **string**|  | |

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

## `downloadReportAsync()`

```php
downloadReportAsync($tenantId, $reportId, $groupId): \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1DownloadReportResponse
```

Retrieves the PBIX for any report in the list in order to download

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string
$reportId = 'reportId_example'; // string | 
$groupId = 'groupId_example'; // string | 

try {
    $result = $apiInstance->downloadReportAsync($tenantId, $reportId, $groupId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->downloadReportAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportId** | **string**|  | |
| **groupId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiReportsV1DownloadReportResponse**](../Model/AnalyticsApiReportsV1DownloadReportResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllTenantAnalyticsWorkspaceReportsAsync()`

```php
getAllTenantAnalyticsWorkspaceReportsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportPaginatedItemsResponse
```

Retrieves all reports.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getAllTenantAnalyticsWorkspaceReportsAsync($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->getAllTenantAnalyticsWorkspaceReportsAsync: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportPaginatedItemsResponse**](../Model/AnalyticsApiReportsV1ReportPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReportByIdAsync()`

```php
getReportByIdAsync($tenantId, $reportId): \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportResponse
```

Retrieves a Report by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportId = 'reportId_example'; // string | 

try {
    $result = $apiInstance->getReportByIdAsync($tenantId, $reportId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->getReportByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportResponse**](../Model/AnalyticsApiReportsV1ReportResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `syncLatestVersion()`

```php
syncLatestVersion($tenantId, $analyticsApiReportsV1SyncLatestVersionRequest): object
```

Sync latest version

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$analyticsApiReportsV1SyncLatestVersionRequest = new \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1SyncLatestVersionRequest(); // \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1SyncLatestVersionRequest | 

try {
    $result = $apiInstance->syncLatestVersion($tenantId, $analyticsApiReportsV1SyncLatestVersionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->syncLatestVersion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **analyticsApiReportsV1SyncLatestVersionRequest** | [**\EdGraph\PlatformClient\Model\AnalyticsApiReportsV1SyncLatestVersionRequest**](../Model/AnalyticsApiReportsV1SyncLatestVersionRequest.md)|  | [optional] |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `syncWorkspacesAsync()`

```php
syncWorkspacesAsync($tenantId, $analyticsApiReportsV1SyncWorkspacesRequest): object
```

Triggers workspace, ODS and DW automation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$analyticsApiReportsV1SyncWorkspacesRequest = new \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1SyncWorkspacesRequest(); // \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1SyncWorkspacesRequest | 

try {
    $result = $apiInstance->syncWorkspacesAsync($tenantId, $analyticsApiReportsV1SyncWorkspacesRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->syncWorkspacesAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **analyticsApiReportsV1SyncWorkspacesRequest** | [**\EdGraph\PlatformClient\Model\AnalyticsApiReportsV1SyncWorkspacesRequest**](../Model/AnalyticsApiReportsV1SyncWorkspacesRequest.md)|  | [optional] |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateReportAsync()`

```php
updateReportAsync($tenantId, $reportId, $file, $id, $name, $shortDescription, $description, $tags, $isVisible, $version, $rolesRequired, $identityRequired, $state): \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1AnalyticsReport
```

Updates a report.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportId = 'reportId_example'; // string | 
$file = "/path/to/file.txt"; // \SplFileObject
$id = 'id_example'; // string
$name = 'name_example'; // string
$shortDescription = 'shortDescription_example'; // string
$description = 'description_example'; // string
$tags = 'tags_example'; // string
$isVisible = True; // bool
$version = 'version_example'; // string
$rolesRequired = True; // bool
$identityRequired = True; // bool
$state = 'state_example'; // string

try {
    $result = $apiInstance->updateReportAsync($tenantId, $reportId, $file, $id, $name, $shortDescription, $description, $tags, $isVisible, $version, $rolesRequired, $identityRequired, $state);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->updateReportAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportId** | **string**|  | |
| **file** | **\SplFileObject****\SplFileObject**|  | [optional] |
| **id** | **string**|  | [optional] |
| **name** | **string**|  | [optional] |
| **shortDescription** | **string**|  | [optional] |
| **description** | **string**|  | [optional] |
| **tags** | **string**|  | [optional] |
| **isVisible** | **bool**|  | [optional] |
| **version** | **string**|  | [optional] |
| **rolesRequired** | **bool**|  | [optional] |
| **identityRequired** | **bool**|  | [optional] |
| **state** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiReportsV1AnalyticsReport**](../Model/AnalyticsApiReportsV1AnalyticsReport.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
