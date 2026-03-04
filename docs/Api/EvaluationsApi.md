# EdGraph\PlatformClient\EvaluationsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createEvaluation()**](EvaluationsApi.md#createEvaluation) | **POST** /tenants/{tenantId}/evaluations | Creates a new Evaluation for a given tenant |
| [**deleteEvaluation()**](EvaluationsApi.md#deleteEvaluation) | **DELETE** /tenants/{tenantId}/evaluations/{evaluationId} | Deletes an Evaluation for a given tenant |
| [**getEvaluation()**](EvaluationsApi.md#getEvaluation) | **GET** /tenants/{tenantId}/evaluations/{evaluationId} | Get an Evaluation for a given tenant |
| [**getEvaluationCount()**](EvaluationsApi.md#getEvaluationCount) | **GET** /tenants/{tenantId}/evaluations/count |  |
| [**searchEvaluationAppraisers()**](EvaluationsApi.md#searchEvaluationAppraisers) | **GET** /tenants/{tenantId}/evaluations/appraisers | Searches the Appraisers associated with an Evaluation for a given Tenant. |
| [**searchEvaluationCampuses()**](EvaluationsApi.md#searchEvaluationCampuses) | **GET** /tenants/{tenantId}/evaluations/campuses | Searches the Campuses associated with an Evaluation for a given Tenant. |
| [**searchEvaluationForms()**](EvaluationsApi.md#searchEvaluationForms) | **GET** /tenants/{tenantId}/evaluations/forms | Searches the Forms associated with an Evaluation for a given Tenant. |
| [**searchEvaluationStaff()**](EvaluationsApi.md#searchEvaluationStaff) | **GET** /tenants/{tenantId}/evaluations/staff | Searches the Staff associated with an Evaluation for a given Tenant. |
| [**searchEvaluations()**](EvaluationsApi.md#searchEvaluations) | **GET** /tenants/{tenantId}/evaluations | Searches the Evaluations for a given tenant |
| [**updateEvaluation()**](EvaluationsApi.md#updateEvaluation) | **PUT** /tenants/{tenantId}/evaluations/{evaluationId} | Updates an Evaluation for a given tenant |


## `createEvaluation()`

```php
createEvaluation($tenantId, $evaluationApiEvaluationsV1CreateEvaluationRequest): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationCreatedResponse
```

Creates a new Evaluation for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EvaluationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$evaluationApiEvaluationsV1CreateEvaluationRequest = new \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1CreateEvaluationRequest(); // \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1CreateEvaluationRequest | 

try {
    $result = $apiInstance->createEvaluation($tenantId, $evaluationApiEvaluationsV1CreateEvaluationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EvaluationsApi->createEvaluation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **evaluationApiEvaluationsV1CreateEvaluationRequest** | [**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1CreateEvaluationRequest**](../Model/EvaluationApiEvaluationsV1CreateEvaluationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationCreatedResponse**](../Model/EvaluationApiEvaluationsV1EvaluationCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteEvaluation()`

```php
deleteEvaluation($tenantId, $evaluationId): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationDeletedResponse
```

Deletes an Evaluation for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EvaluationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$evaluationId = 'evaluationId_example'; // string | 

try {
    $result = $apiInstance->deleteEvaluation($tenantId, $evaluationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EvaluationsApi->deleteEvaluation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **evaluationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationDeletedResponse**](../Model/EvaluationApiEvaluationsV1EvaluationDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEvaluation()`

```php
getEvaluation($tenantId, $evaluationId): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationResponse
```

Get an Evaluation for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EvaluationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$evaluationId = 'evaluationId_example'; // string | 

try {
    $result = $apiInstance->getEvaluation($tenantId, $evaluationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EvaluationsApi->getEvaluation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **evaluationId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationResponse**](../Model/EvaluationApiEvaluationsV1EvaluationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEvaluationCount()`

```php
getEvaluationCount($tenantId): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationCountResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EvaluationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string

try {
    $result = $apiInstance->getEvaluationCount($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EvaluationsApi->getEvaluationCount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationCountResponse**](../Model/EvaluationApiEvaluationsV1EvaluationCountResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchEvaluationAppraisers()`

```php
searchEvaluationAppraisers($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse
```

Searches the Appraisers associated with an Evaluation for a given Tenant.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EvaluationsApi(
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
    $result = $apiInstance->searchEvaluationAppraisers($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EvaluationsApi->searchEvaluationAppraisers: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchEvaluationCampuses()`

```php
searchEvaluationCampuses($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel
```

Searches the Campuses associated with an Evaluation for a given Tenant.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EvaluationsApi(
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
    $result = $apiInstance->searchEvaluationCampuses($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EvaluationsApi->searchEvaluationCampuses: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel**](../Model/EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchEvaluationForms()`

```php
searchEvaluationForms($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel
```

Searches the Forms associated with an Evaluation for a given Tenant.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EvaluationsApi(
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
    $result = $apiInstance->searchEvaluationForms($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EvaluationsApi->searchEvaluationForms: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel**](../Model/EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchEvaluationStaff()`

```php
searchEvaluationStaff($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse
```

Searches the Staff associated with an Evaluation for a given Tenant.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EvaluationsApi(
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
    $result = $apiInstance->searchEvaluationStaff($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EvaluationsApi->searchEvaluationStaff: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchEvaluations()`

```php
searchEvaluations($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel
```

Searches the Evaluations for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EvaluationsApi(
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
    $result = $apiInstance->searchEvaluations($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EvaluationsApi->searchEvaluations: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel**](../Model/EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateEvaluation()`

```php
updateEvaluation($tenantId, $evaluationId, $evaluationApiEvaluationsV1UpdateEvaluationRequest): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationUpdatedResponse
```

Updates an Evaluation for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EvaluationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$evaluationId = 'evaluationId_example'; // string | 
$evaluationApiEvaluationsV1UpdateEvaluationRequest = new \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1UpdateEvaluationRequest(); // \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1UpdateEvaluationRequest | 

try {
    $result = $apiInstance->updateEvaluation($tenantId, $evaluationId, $evaluationApiEvaluationsV1UpdateEvaluationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EvaluationsApi->updateEvaluation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **evaluationId** | **string**|  | |
| **evaluationApiEvaluationsV1UpdateEvaluationRequest** | [**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1UpdateEvaluationRequest**](../Model/EvaluationApiEvaluationsV1UpdateEvaluationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationUpdatedResponse**](../Model/EvaluationApiEvaluationsV1EvaluationUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
