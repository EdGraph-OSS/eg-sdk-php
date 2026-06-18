# EdGraph\PlatformClient\ObservationsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createObservation()**](ObservationsApi.md#createObservation) | **POST** /tenants/{tenantId}/observations | Creates a new Observation for a given tenant |
| [**createObservationSubmission()**](ObservationsApi.md#createObservationSubmission) | **POST** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/submit | Creates a submission for an available form referencing an existing observation |
| [**deleteObservation()**](ObservationsApi.md#deleteObservation) | **DELETE** /tenants/{tenantId}/observations/{observationId} | Deletes an Observation for a given tenant |
| [**getDashboard()**](ObservationsApi.md#getDashboard) | **GET** /tenants/{tenantId}/observations/dashboards/{dashboardId} | Get Observation Dashboard |
| [**getDashboardPreferences()**](ObservationsApi.md#getDashboardPreferences) | **GET** /tenants/{tenantId}/observations/dashboards/{dashboardId}/preferences | Save user preferences for a given Dashboard |
| [**getEvalueeSections()**](ObservationsApi.md#getEvalueeSections) | **GET** /tenants/{tenantId}/observations/evaluees/{evalueeId}/sections | Gets the Sections of an evaluee. |
| [**getFormQuestions()**](ObservationsApi.md#getFormQuestions) | **GET** /tenants/{tenantId}/observations/available-forms/{formId}/sections/{sectionId}/questions | Search Questions |
| [**getFormSections()**](ObservationsApi.md#getFormSections) | **GET** /tenants/{tenantId}/observations/available-forms/{formId}/sections | Search Observation Form Sections |
| [**getObservationById()**](ObservationsApi.md#getObservationById) | **GET** /tenants/{tenantId}/observations/{observationId} | Get an Observation for a given tenant |
| [**getObservationDraft()**](ObservationsApi.md#getObservationDraft) | **GET** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/draft | Get an observation form&#39;s draft |
| [**getObservationSubmission()**](ObservationsApi.md#getObservationSubmission) | **GET** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/submission | Gets a submission for a specific observation |
| [**getPaginatedAvailableCampuses()**](ObservationsApi.md#getPaginatedAvailableCampuses) | **GET** /tenants/{tenantId}/observations/campuses | Get Available Campuses |
| [**getPaginatedAvailableForms()**](ObservationsApi.md#getPaginatedAvailableForms) | **GET** /tenants/{tenantId}/observations/available-forms | Get Paginated Available Forms |
| [**getPaginatedCampusSections()**](ObservationsApi.md#getPaginatedCampusSections) | **GET** /tenants/{tenantId}/observations/campuses/{campusId}/sections | Retrieves a list of Sections for a given available campus. |
| [**getPaginatedEvaluees()**](ObservationsApi.md#getPaginatedEvaluees) | **GET** /tenants/{tenantId}/observations/evaluees | Get paginated evaluees |
| [**getPaginatedObservations()**](ObservationsApi.md#getPaginatedObservations) | **GET** /tenants/{tenantId}/observations | Get Paginated Observations for a given tenant |
| [**getSubmittedObservationsCount()**](ObservationsApi.md#getSubmittedObservationsCount) | **GET** /tenants/{tenantId}/submittedobservations | Get submitted Observations count |
| [**saveDashboardPreferences()**](ObservationsApi.md#saveDashboardPreferences) | **POST** /tenants/{tenantId}/observations/dashboards/{dashboardId}/preferences | Save user preferences for a given Dashboard |
| [**searchPaginatedEvaluees()**](ObservationsApi.md#searchPaginatedEvaluees) | **GET** /tenants/{tenantId}/observations/search/evaluees | Search paginated evaluees |
| [**updateObservation()**](ObservationsApi.md#updateObservation) | **PUT** /tenants/{tenantId}/observations/{observationId} | Update an Observation for a given tenant |
| [**upsertObservationDraft()**](ObservationsApi.md#upsertObservationDraft) | **POST** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/draft | Creates a draft for an observation forms |
| [**verifyDashboardAccess()**](ObservationsApi.md#verifyDashboardAccess) | **POST** /tenants/{tenantId}/observations/dashboards/access | Verify user access to dashboards |


## `createObservation()`

```php
createObservation($tenantId, $edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationResponse
```

Creates a new Observation for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest | 

try {
    $result = $apiInstance->createObservation($tenantId, $edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->createObservation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createObservationSubmission()`

```php
createObservationSubmission($tenantId, $formId, $observationId, $edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionResponse
```

Creates a submission for an available form referencing an existing observation

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$observationId = 'observationId_example'; // string
$edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest | 

try {
    $result = $apiInstance->createObservationSubmission($tenantId, $formId, $observationId, $edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->createObservationSubmission: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **observationId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteObservation()`

```php
deleteObservation($tenantId, $observationId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsDeleteObservationResponse
```

Deletes an Observation for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$observationId = 'observationId_example'; // string | 

try {
    $result = $apiInstance->deleteObservation($tenantId, $observationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->deleteObservation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **observationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsDeleteObservationResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsDeleteObservationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDashboard()`

```php
getDashboard($tenantId, $dashboardId, $personaIdentifier): \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportResponse
```

Get Observation Dashboard

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$dashboardId = 'dashboardId_example'; // string | 
$personaIdentifier = 'personaIdentifier_example'; // string | 

try {
    $result = $apiInstance->getDashboard($tenantId, $dashboardId, $personaIdentifier);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getDashboard: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **dashboardId** | **string**|  | |
| **personaIdentifier** | **string**|  | [optional] |

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

## `getDashboardPreferences()`

```php
getDashboardPreferences($tenantId, $dashboardId): \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportPreferencesResponse
```

Save user preferences for a given Dashboard

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$dashboardId = 'dashboardId_example'; // string | 

try {
    $result = $apiInstance->getDashboardPreferences($tenantId, $dashboardId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getDashboardPreferences: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **dashboardId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportPreferencesResponse**](../Model/AnalyticsApiReportsV1ReportPreferencesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEvalueeSections()`

```php
getEvalueeSections($tenantId, $evalueeId, $pageIndex, $pageSize, $orderBy, $filterBy): \EdGraph\PlatformClient\Model\IdentityApiUserV1SectionResponseGetPaginatedItemsResponse
```

Gets the Sections of an evaluee.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$evalueeId = 'evalueeId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 0; // int | 
$orderBy = ''; // string | 
$filterBy = ''; // string | 

try {
    $result = $apiInstance->getEvalueeSections($tenantId, $evalueeId, $pageIndex, $pageSize, $orderBy, $filterBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getEvalueeSections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **evalueeId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filterBy** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\IdentityApiUserV1SectionResponseGetPaginatedItemsResponse**](../Model/IdentityApiUserV1SectionResponseGetPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getFormQuestions()`

```php
getFormQuestions($tenantId, $formId, $sectionId, $pageIndex, $pageSize): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel
```

Search Questions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$sectionId = 'sectionId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 

try {
    $result = $apiInstance->getFormQuestions($tenantId, $formId, $sectionId, $pageIndex, $pageSize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getFormQuestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **sectionId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getFormSections()`

```php
getFormSections($tenantId, $formId, $pageIndex, $pageSize): \EdGraph\PlatformClient\Model\FormApiSectionsV1SectionResponsePaginatedItemsViewModel
```

Search Observation Form Sections

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 

try {
    $result = $apiInstance->getFormSections($tenantId, $formId, $pageIndex, $pageSize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getFormSections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |

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

## `getObservationById()`

```php
getObservationById($tenantId, $observationId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponse
```

Get an Observation for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$observationId = 'observationId_example'; // string | 

try {
    $result = $apiInstance->getObservationById($tenantId, $observationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getObservationById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **observationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getObservationDraft()`

```php
getObservationDraft($tenantId, $observationId, $formId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsObservationDraftResponse
```

Get an observation form's draft

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$observationId = 'observationId_example'; // string | 
$formId = 'formId_example'; // string | 

try {
    $result = $apiInstance->getObservationDraft($tenantId, $observationId, $formId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getObservationDraft: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **observationId** | **string**|  | |
| **formId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsObservationDraftResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsObservationDraftResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getObservationSubmission()`

```php
getObservationSubmission($tenantId, $observationId, $formId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsObservationSubmissionResponse
```

Gets a submission for a specific observation

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$observationId = 'observationId_example'; // string | 
$formId = 'formId_example'; // string | 

try {
    $result = $apiInstance->getObservationSubmission($tenantId, $observationId, $formId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getObservationSubmission: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **observationId** | **string**|  | |
| **formId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsObservationSubmissionResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsObservationSubmissionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPaginatedAvailableCampuses()`

```php
getPaginatedAvailableCampuses($tenantId, $pageSize, $pageIndex, $orderBy, $nameOfInstitution): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse
```

Get Available Campuses

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$nameOfInstitution = ''; // string | 

try {
    $result = $apiInstance->getPaginatedAvailableCampuses($tenantId, $pageSize, $pageIndex, $orderBy, $nameOfInstitution);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getPaginatedAvailableCampuses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **nameOfInstitution** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPaginatedAvailableForms()`

```php
getPaginatedAvailableForms($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesFormsV1FormGetPaginatedItemsResponse
```

Get Paginated Available Forms

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
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
    $result = $apiInstance->getPaginatedAvailableForms($tenantId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getPaginatedAvailableForms: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesFormsV1FormGetPaginatedItemsResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesFormsV1FormGetPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPaginatedCampusSections()`

```php
getPaginatedCampusSections($tenantId, $campusId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\TenantApiSectionsV1SectionListResponseGetPaginatedItemsResponse
```

Retrieves a list of Sections for a given available campus.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$campusId = 'campusId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->getPaginatedCampusSections($tenantId, $campusId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getPaginatedCampusSections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **campusId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\TenantApiSectionsV1SectionListResponseGetPaginatedItemsResponse**](../Model/TenantApiSectionsV1SectionListResponseGetPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPaginatedEvaluees()`

```php
getPaginatedEvaluees($tenantId, $pageSize, $pageIndex, $orderBy, $campus, $evalueeId, $firstName, $lastName): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse
```

Get paginated evaluees

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$campus = ''; // string | 
$evalueeId = ''; // string | 
$firstName = ''; // string | 
$lastName = ''; // string | 

try {
    $result = $apiInstance->getPaginatedEvaluees($tenantId, $pageSize, $pageIndex, $orderBy, $campus, $evalueeId, $firstName, $lastName);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getPaginatedEvaluees: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **campus** | **string**|  | [optional] [default to &#39;&#39;] |
| **evalueeId** | **string**|  | [optional] [default to &#39;&#39;] |
| **firstName** | **string**|  | [optional] [default to &#39;&#39;] |
| **lastName** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPaginatedObservations()`

```php
getPaginatedObservations($tenantId, $pageSize, $pageIndex, $orderBy, $campus, $evalueeName, $evalueeId, $formId, $status, $from, $to): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponsePaginatedItemsViewModel
```

Get Paginated Observations for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$campus = ''; // string | 
$evalueeName = ''; // string | 
$evalueeId = ''; // string | 
$formId = ''; // string | 
$status = ''; // string | 
$from = ''; // string | 
$to = ''; // string | 

try {
    $result = $apiInstance->getPaginatedObservations($tenantId, $pageSize, $pageIndex, $orderBy, $campus, $evalueeName, $evalueeId, $formId, $status, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getPaginatedObservations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **campus** | **string**|  | [optional] [default to &#39;&#39;] |
| **evalueeName** | **string**|  | [optional] [default to &#39;&#39;] |
| **evalueeId** | **string**|  | [optional] [default to &#39;&#39;] |
| **formId** | **string**|  | [optional] [default to &#39;&#39;] |
| **status** | **string**|  | [optional] [default to &#39;&#39;] |
| **from** | **string**|  | [optional] [default to &#39;&#39;] |
| **to** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponsePaginatedItemsViewModel**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSubmittedObservationsCount()`

```php
getSubmittedObservationsCount($tenantId, $evalueeId, $campus): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsGetSubmittedObservationsCountResponse
```

Get submitted Observations count

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$evalueeId = 'evalueeId_example'; // string | 
$campus = 'campus_example'; // string | 

try {
    $result = $apiInstance->getSubmittedObservationsCount($tenantId, $evalueeId, $campus);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getSubmittedObservationsCount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **evalueeId** | **string**|  | [optional] |
| **campus** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsGetSubmittedObservationsCountResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsGetSubmittedObservationsCountResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `saveDashboardPreferences()`

```php
saveDashboardPreferences($tenantId, $dashboardId, $edGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest): \EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportPreferencesSavedResponse
```

Save user preferences for a given Dashboard

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$dashboardId = 'dashboardId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest | 

try {
    $result = $apiInstance->saveDashboardPreferences($tenantId, $dashboardId, $edGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->saveDashboardPreferences: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **dashboardId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\AnalyticsApiReportsV1ReportPreferencesSavedResponse**](../Model/AnalyticsApiReportsV1ReportPreferencesSavedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchPaginatedEvaluees()`

```php
searchPaginatedEvaluees($tenantId, $pageSize, $pageIndex, $orderBy, $firstName, $lastName): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponsePaginatedItemsViewModel
```

Search paginated evaluees

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$firstName = ''; // string | 
$lastName = ''; // string | 

try {
    $result = $apiInstance->searchPaginatedEvaluees($tenantId, $pageSize, $pageIndex, $orderBy, $firstName, $lastName);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->searchPaginatedEvaluees: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **firstName** | **string**|  | [optional] [default to &#39;&#39;] |
| **lastName** | **string**|  | [optional] [default to &#39;&#39;] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponsePaginatedItemsViewModel**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateObservation()`

```php
updateObservation($tenantId, $observationId, $edGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationResponse
```

Update an Observation for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$observationId = 'observationId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest | 

try {
    $result = $apiInstance->updateObservation($tenantId, $observationId, $edGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->updateObservation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **observationId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `upsertObservationDraft()`

```php
upsertObservationDraft($tenantId, $observationId, $formId, $edGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftResponse
```

Creates a draft for an observation forms

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$observationId = 'observationId_example'; // string | 
$formId = 'formId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest | 

try {
    $result = $apiInstance->upsertObservationDraft($tenantId, $observationId, $formId, $edGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->upsertObservationDraft: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **observationId** | **string**|  | |
| **formId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `verifyDashboardAccess()`

```php
verifyDashboardAccess($tenantId, $edGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessResponse
```

Verify user access to dashboards

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest | 

try {
    $result = $apiInstance->verifyDashboardAccess($tenantId, $edGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->verifyDashboardAccess: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
