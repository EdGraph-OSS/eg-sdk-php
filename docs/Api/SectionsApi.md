# EdGraph\PlatformClient\SectionsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createSection()**](SectionsApi.md#createSection) | **POST** /tenants/{tenantId}/forms/{formId}/sections | Creates a new Section for a given form |
| [**deleteSection()**](SectionsApi.md#deleteSection) | **DELETE** /tenants/{tenantId}/forms/{formId}/sections/{sectionId} | Deletes a Section. |
| [**getSection()**](SectionsApi.md#getSection) | **GET** /tenants/{tenantId}/forms/{formId}/sections/{sectionId} | Get Section. |
| [**getSectionAcademicSubjects()**](SectionsApi.md#getSectionAcademicSubjects) | **GET** /tenants/{tenantId}/sections/academicSubjects | Retrieves a list of Section Academic Subjects. |
| [**getSectionById()**](SectionsApi.md#getSectionById) | **GET** /tenants/{tenantId}/sections/{sectionId} | Retrieves a Section by ID. |
| [**getSectionCourses()**](SectionsApi.md#getSectionCourses) | **GET** /tenants/{tenantId}/sections/courses | Retrieves a list of Section Courses. |
| [**getSectionGradeLevels()**](SectionsApi.md#getSectionGradeLevels) | **GET** /tenants/{tenantId}/sections/gradeLevels | Retrieves a list of Section Grade Levels. |
| [**getSectionSchools()**](SectionsApi.md#getSectionSchools) | **GET** /tenants/{tenantId}/sections/schools | Retrieves a list of Section Schools. |
| [**getSectionSessions()**](SectionsApi.md#getSectionSessions) | **GET** /tenants/{tenantId}/sections/sessions | Retrieves a list of Section Sessions. |
| [**getSectionTerms()**](SectionsApi.md#getSectionTerms) | **GET** /tenants/{tenantId}/sections/terms | Retrieves a list of Section Terms. |
| [**getSections()**](SectionsApi.md#getSections) | **GET** /tenants/{tenantId}/sections | Retrieves a list of Sections. |
| [**searchSections()**](SectionsApi.md#searchSections) | **GET** /tenants/{tenantId}/forms/{formId}/sections | Search Sections |
| [**updateSection()**](SectionsApi.md#updateSection) | **PUT** /tenants/{tenantId}/forms/{formId}/sections/{sectionId} | Updates a Section. |


## `createSection()`

```php
createSection($tenantId, $formId, $formApiSectionsV1CreateSectionRequest): \EdGraph\PlatformClient\Model\FormApiSectionsV1SectionCreatedResponse
```

Creates a new Section for a given form

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$formApiSectionsV1CreateSectionRequest = new \EdGraph\PlatformClient\Model\FormApiSectionsV1CreateSectionRequest(); // \EdGraph\PlatformClient\Model\FormApiSectionsV1CreateSectionRequest | 

try {
    $result = $apiInstance->createSection($tenantId, $formId, $formApiSectionsV1CreateSectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SectionsApi->createSection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **formApiSectionsV1CreateSectionRequest** | [**\EdGraph\PlatformClient\Model\FormApiSectionsV1CreateSectionRequest**](../Model/FormApiSectionsV1CreateSectionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiSectionsV1SectionCreatedResponse**](../Model/FormApiSectionsV1SectionCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteSection()`

```php
deleteSection($tenantId, $formId, $sectionId): \EdGraph\PlatformClient\Model\FormApiSectionsV1SectionDeletedResponse
```

Deletes a Section.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$sectionId = 'sectionId_example'; // string | 

try {
    $result = $apiInstance->deleteSection($tenantId, $formId, $sectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SectionsApi->deleteSection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **sectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiSectionsV1SectionDeletedResponse**](../Model/FormApiSectionsV1SectionDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSection()`

```php
getSection($tenantId, $formId, $sectionId): \EdGraph\PlatformClient\Model\FormApiSectionsV1SectionResponse
```

Get Section.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$sectionId = 'sectionId_example'; // string | 

try {
    $result = $apiInstance->getSection($tenantId, $formId, $sectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SectionsApi->getSection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **sectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiSectionsV1SectionResponse**](../Model/FormApiSectionsV1SectionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSectionAcademicSubjects()`

```php
getSectionAcademicSubjects($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedAcademicSubjectsResponse
```

Retrieves a list of Section Academic Subjects.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getSectionAcademicSubjects($tenantId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SectionsApi->getSectionAcademicSubjects: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedAcademicSubjectsResponse**](../Model/TenantApiSectionsV1PaginatedAcademicSubjectsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSectionById()`

```php
getSectionById($tenantId, $sectionId): \EdGraph\PlatformClient\Model\TenantApiSectionsV1SectionProfileResponse
```

Retrieves a Section by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$sectionId = 'sectionId_example'; // string | 

try {
    $result = $apiInstance->getSectionById($tenantId, $sectionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SectionsApi->getSectionById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **sectionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiSectionsV1SectionProfileResponse**](../Model/TenantApiSectionsV1SectionProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSectionCourses()`

```php
getSectionCourses($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedCoursesResponse
```

Retrieves a list of Section Courses.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getSectionCourses($tenantId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SectionsApi->getSectionCourses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedCoursesResponse**](../Model/TenantApiSectionsV1PaginatedCoursesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSectionGradeLevels()`

```php
getSectionGradeLevels($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedGradeLevelsResponse
```

Retrieves a list of Section Grade Levels.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getSectionGradeLevels($tenantId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SectionsApi->getSectionGradeLevels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedGradeLevelsResponse**](../Model/TenantApiSectionsV1PaginatedGradeLevelsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSectionSchools()`

```php
getSectionSchools($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedSchoolsResponse
```

Retrieves a list of Section Schools.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getSectionSchools($tenantId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SectionsApi->getSectionSchools: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedSchoolsResponse**](../Model/TenantApiSectionsV1PaginatedSchoolsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSectionSessions()`

```php
getSectionSessions($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedSessionsResponse
```

Retrieves a list of Section Sessions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getSectionSessions($tenantId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SectionsApi->getSectionSessions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedSessionsResponse**](../Model/TenantApiSectionsV1PaginatedSessionsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSectionTerms()`

```php
getSectionTerms($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedTermsResponse
```

Retrieves a list of Section Terms.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getSectionTerms($tenantId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SectionsApi->getSectionTerms: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedTermsResponse**](../Model/TenantApiSectionsV1PaginatedTermsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSections()`

```php
getSections($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedItemsResponse
```

Retrieves a list of Sections.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getSections($tenantId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SectionsApi->getSections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiSectionsV1PaginatedItemsResponse**](../Model/TenantApiSectionsV1PaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchSections()`

```php
searchSections($tenantId, $formId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\FormApiSectionsV1SectionResponsePaginatedItemsViewModel
```

Search Sections

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->searchSections($tenantId, $formId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SectionsApi->searchSections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiSectionsV1SectionResponsePaginatedItemsViewModel**](../Model/FormApiSectionsV1SectionResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSection()`

```php
updateSection($tenantId, $formId, $sectionId, $formApiSectionsV1UpdateSectionRequest): \EdGraph\PlatformClient\Model\FormApiSectionsV1SectionUpdatedResponse
```

Updates a Section.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$sectionId = 'sectionId_example'; // string | 
$formApiSectionsV1UpdateSectionRequest = new \EdGraph\PlatformClient\Model\FormApiSectionsV1UpdateSectionRequest(); // \EdGraph\PlatformClient\Model\FormApiSectionsV1UpdateSectionRequest | 

try {
    $result = $apiInstance->updateSection($tenantId, $formId, $sectionId, $formApiSectionsV1UpdateSectionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SectionsApi->updateSection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **sectionId** | **string**|  | |
| **formApiSectionsV1UpdateSectionRequest** | [**\EdGraph\PlatformClient\Model\FormApiSectionsV1UpdateSectionRequest**](../Model/FormApiSectionsV1UpdateSectionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiSectionsV1SectionUpdatedResponse**](../Model/FormApiSectionsV1SectionUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
