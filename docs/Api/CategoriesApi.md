# EdGraph\PlatformClient\CategoriesApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addCategoryDataSteward()**](CategoriesApi.md#addCategoryDataSteward) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/stewards | Adds a Data Steward to a Category. |
| [**addCategoryDataStewardBulk()**](CategoriesApi.md#addCategoryDataStewardBulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/stewards | Adds a Data Steward to Categories. |
| [**certifyCategory()**](CategoriesApi.md#certifyCategory) | **POST** /tenants/{tenantId}/statereporting/categories/{categoryId}/certify | Certifies a Category. |
| [**getDataUsersBulk()**](CategoriesApi.md#getDataUsersBulk) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/datausers | Get all Data Users |
| [**getStateReportingCategories()**](CategoriesApi.md#getStateReportingCategories) | **GET** /tenants/{tenantId}/statereporting/categories | Retrieves a list of Categories. |
| [**removeCategoryDataOwner()**](CategoriesApi.md#removeCategoryDataOwner) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/owner | Removes the Data Owner of a Category. |
| [**removeCategoryDataSteward()**](CategoriesApi.md#removeCategoryDataSteward) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/stewards/{email} | Removes a Data Steward from a Category. |
| [**requestCategoryCertificationReminder()**](CategoriesApi.md#requestCategoryCertificationReminder) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/certificationreminder | Requests a Certification Reminder to be sent. |
| [**setCategoryDataOwner()**](CategoriesApi.md#setCategoryDataOwner) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/owner | Sets the Data Owner of a Category. |
| [**setCategoryDataOwnerBulk()**](CategoriesApi.md#setCategoryDataOwnerBulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/owner | Sets the Data Owner of Categories. |
| [**uploadStateReportingCategory()**](CategoriesApi.md#uploadStateReportingCategory) | **POST** /tenants/{tenantId}/statereporting/categories/upload | Upload a Category via a JSON file. |
| [**uploadStateReportingPeriodsFromCategoryJson()**](CategoriesApi.md#uploadStateReportingPeriodsFromCategoryJson) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/upload | Upload a Category via a JSON file. |


## `addCategoryDataSteward()`

```php
addCategoryDataSteward($tenantId, $categoryId, $reportingPeriodId, $validationsApiContainersV1AddDataStewardRequest): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1DataStewardAddedResponse
```

Adds a Data Steward to a Category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$categoryId = 'categoryId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$validationsApiContainersV1AddDataStewardRequest = new \EdGraph\PlatformClient\Model\ValidationsApiContainersV1AddDataStewardRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiContainersV1AddDataStewardRequest | 

try {
    $result = $apiInstance->addCategoryDataSteward($tenantId, $categoryId, $reportingPeriodId, $validationsApiContainersV1AddDataStewardRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->addCategoryDataSteward: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **categoryId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **validationsApiContainersV1AddDataStewardRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1AddDataStewardRequest**](../Model/ValidationsApiContainersV1AddDataStewardRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1DataStewardAddedResponse**](../Model/ValidationsApiContainersV1DataStewardAddedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `addCategoryDataStewardBulk()`

```php
addCategoryDataStewardBulk($tenantId, $reportingPeriodId, $validationsApiContainersV1AddDataStewardBulkRequest): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1DataStewardAddedBulkResponse
```

Adds a Data Steward to Categories.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$validationsApiContainersV1AddDataStewardBulkRequest = new \EdGraph\PlatformClient\Model\ValidationsApiContainersV1AddDataStewardBulkRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiContainersV1AddDataStewardBulkRequest | 

try {
    $result = $apiInstance->addCategoryDataStewardBulk($tenantId, $reportingPeriodId, $validationsApiContainersV1AddDataStewardBulkRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->addCategoryDataStewardBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **validationsApiContainersV1AddDataStewardBulkRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1AddDataStewardBulkRequest**](../Model/ValidationsApiContainersV1AddDataStewardBulkRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1DataStewardAddedBulkResponse**](../Model/ValidationsApiContainersV1DataStewardAddedBulkResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `certifyCategory()`

```php
certifyCategory($tenantId, $categoryId): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1CertificationStatusSetResponse
```

Certifies a Category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$categoryId = 'categoryId_example'; // string | 

try {
    $result = $apiInstance->certifyCategory($tenantId, $categoryId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->certifyCategory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **categoryId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1CertificationStatusSetResponse**](../Model/ValidationsApiContainersV1CertificationStatusSetResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDataUsersBulk()`

```php
getDataUsersBulk($tenantId, $reportingPeriodId): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1CategoriesWithDataUsersResponse
```

Get all Data Users

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->getDataUsersBulk($tenantId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->getDataUsersBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1CategoriesWithDataUsersResponse**](../Model/ValidationsApiContainersV1CategoriesWithDataUsersResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStateReportingCategories()`

```php
getStateReportingCategories($tenantId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1PaginatedContainers
```

Retrieves a list of Categories.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$filter = ''; // string | 
$orderBy = ''; // string | 

try {
    $result = $apiInstance->getStateReportingCategories($tenantId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->getStateReportingCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1PaginatedContainers**](../Model/ValidationsApiContainersV1PaginatedContainers.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeCategoryDataOwner()`

```php
removeCategoryDataOwner($tenantId, $reportingPeriodId, $categoryId)
```

Removes the Data Owner of a Category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$categoryId = 'categoryId_example'; // string | 

try {
    $apiInstance->removeCategoryDataOwner($tenantId, $reportingPeriodId, $categoryId);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->removeCategoryDataOwner: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **categoryId** | **string**|  | |

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

## `removeCategoryDataSteward()`

```php
removeCategoryDataSteward($tenantId, $categoryId, $reportingPeriodId, $email)
```

Removes a Data Steward from a Category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$categoryId = 'categoryId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$email = 'email_example'; // string | 

try {
    $apiInstance->removeCategoryDataSteward($tenantId, $categoryId, $reportingPeriodId, $email);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->removeCategoryDataSteward: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **categoryId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **email** | **string**|  | |

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

## `requestCategoryCertificationReminder()`

```php
requestCategoryCertificationReminder($tenantId, $reportingPeriodId, $categoryId): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1CertificationReminderRequestedResponse
```

Requests a Certification Reminder to be sent.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$categoryId = 'categoryId_example'; // string | 

try {
    $result = $apiInstance->requestCategoryCertificationReminder($tenantId, $reportingPeriodId, $categoryId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->requestCategoryCertificationReminder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **categoryId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1CertificationReminderRequestedResponse**](../Model/ValidationsApiContainersV1CertificationReminderRequestedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setCategoryDataOwner()`

```php
setCategoryDataOwner($tenantId, $categoryId, $reportingPeriodId, $validationsApiContainersV1SetDataOwnerRequest): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1DataOwnerSetResponse
```

Sets the Data Owner of a Category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$categoryId = 'categoryId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$validationsApiContainersV1SetDataOwnerRequest = new \EdGraph\PlatformClient\Model\ValidationsApiContainersV1SetDataOwnerRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiContainersV1SetDataOwnerRequest | 

try {
    $result = $apiInstance->setCategoryDataOwner($tenantId, $categoryId, $reportingPeriodId, $validationsApiContainersV1SetDataOwnerRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->setCategoryDataOwner: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **categoryId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **validationsApiContainersV1SetDataOwnerRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1SetDataOwnerRequest**](../Model/ValidationsApiContainersV1SetDataOwnerRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1DataOwnerSetResponse**](../Model/ValidationsApiContainersV1DataOwnerSetResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setCategoryDataOwnerBulk()`

```php
setCategoryDataOwnerBulk($tenantId, $reportingPeriodId, $validationsApiContainersV1SetDataOwnerBulkRequest): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1DataOwnerSetBulkResponse
```

Sets the Data Owner of Categories.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$validationsApiContainersV1SetDataOwnerBulkRequest = new \EdGraph\PlatformClient\Model\ValidationsApiContainersV1SetDataOwnerBulkRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiContainersV1SetDataOwnerBulkRequest | 

try {
    $result = $apiInstance->setCategoryDataOwnerBulk($tenantId, $reportingPeriodId, $validationsApiContainersV1SetDataOwnerBulkRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->setCategoryDataOwnerBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **validationsApiContainersV1SetDataOwnerBulkRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1SetDataOwnerBulkRequest**](../Model/ValidationsApiContainersV1SetDataOwnerBulkRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1DataOwnerSetBulkResponse**](../Model/ValidationsApiContainersV1DataOwnerSetBulkResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadStateReportingCategory()`

```php
uploadStateReportingCategory($tenantId, $contentType, $contentDisposition, $headers, $length, $name, $fileName): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1CollectionUploadedResponse
```

Upload a Category via a JSON file.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$contentType = 'contentType_example'; // string
$contentDisposition = 'contentDisposition_example'; // string
$headers = NULL; // array<string,string[]>
$length = 56; // int
$name = 'name_example'; // string
$fileName = 'fileName_example'; // string

try {
    $result = $apiInstance->uploadStateReportingCategory($tenantId, $contentType, $contentDisposition, $headers, $length, $name, $fileName);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->uploadStateReportingCategory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **contentType** | **string**|  | [optional] |
| **contentDisposition** | **string**|  | [optional] |
| **headers** | [**array<string,string[]>**](../Model/array.md)|  | [optional] |
| **length** | **int**|  | [optional] |
| **name** | **string**|  | [optional] |
| **fileName** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1CollectionUploadedResponse**](../Model/ValidationsApiContainersV1CollectionUploadedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadStateReportingPeriodsFromCategoryJson()`

```php
uploadStateReportingPeriodsFromCategoryJson($tenantId, $environmentId, $contentType, $contentDisposition, $headers, $length, $name, $fileName): \EdGraph\PlatformClient\Model\ValidationsApiContainersV1CollectionUploadedResponse
```

Upload a Category via a JSON file.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$contentType = 'contentType_example'; // string
$contentDisposition = 'contentDisposition_example'; // string
$headers = NULL; // array<string,string[]>
$length = 56; // int
$name = 'name_example'; // string
$fileName = 'fileName_example'; // string

try {
    $result = $apiInstance->uploadStateReportingPeriodsFromCategoryJson($tenantId, $environmentId, $contentType, $contentDisposition, $headers, $length, $name, $fileName);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->uploadStateReportingPeriodsFromCategoryJson: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **contentType** | **string**|  | [optional] |
| **contentDisposition** | **string**|  | [optional] |
| **headers** | [**array<string,string[]>**](../Model/array.md)|  | [optional] |
| **length** | **int**|  | [optional] |
| **name** | **string**|  | [optional] |
| **fileName** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiContainersV1CollectionUploadedResponse**](../Model/ValidationsApiContainersV1CollectionUploadedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
