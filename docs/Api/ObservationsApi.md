# EdGraph\PlatformClient\ObservationsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createObservation()**](ObservationsApi.md#createObservation) | **POST** /tenants/{tenantId}/observations | Creates a new Observation for a given tenant |
| [**deleteObservation()**](ObservationsApi.md#deleteObservation) | **DELETE** /tenants/{tenantId}/observations/{observationId} | Deletes an Observation for a given tenant |
| [**getObservation()**](ObservationsApi.md#getObservation) | **GET** /tenants/{tenantId}/observations/{observationId} | Get an Observation for a given tenant |
| [**getObservationCount()**](ObservationsApi.md#getObservationCount) | **GET** /tenants/{tenantId}/observations/count |  |
| [**searchObservationCampuses()**](ObservationsApi.md#searchObservationCampuses) | **GET** /tenants/{tenantId}/observations/campuses | Searches the Campuses associated with an Observation for a given Tenant. |
| [**searchObservationEvaluees()**](ObservationsApi.md#searchObservationEvaluees) | **GET** /tenants/{tenantId}/observations/evaluees | Searches the Staff associated with an Observation for a given Tenant. |
| [**searchObservationForms()**](ObservationsApi.md#searchObservationForms) | **GET** /tenants/{tenantId}/observations/forms | Searches the Forms associated with an Observation for a given Tenant. |
| [**searchObservationObservers()**](ObservationsApi.md#searchObservationObservers) | **GET** /tenants/{tenantId}/observations/observers | Searches the Appraisers associated with an Observation for a given Tenant. |
| [**searchObservations()**](ObservationsApi.md#searchObservations) | **GET** /tenants/{tenantId}/observations | Searches the Observations for a given tenant |
| [**updateObservation()**](ObservationsApi.md#updateObservation) | **PUT** /tenants/{tenantId}/observations/{observationId} | Updates an Observation for a given tenant |


## `createObservation()`

```php
createObservation($tenantId, $evaluationApiEvaluationsV1CreateEvaluationRequest): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationCreatedResponse
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
$evaluationApiEvaluationsV1CreateEvaluationRequest = new \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1CreateEvaluationRequest(); // \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1CreateEvaluationRequest | 

try {
    $result = $apiInstance->createObservation($tenantId, $evaluationApiEvaluationsV1CreateEvaluationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->createObservation: ', $e->getMessage(), PHP_EOL;
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

## `deleteObservation()`

```php
deleteObservation($tenantId, $observationId): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationDeletedResponse
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

[**\EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationDeletedResponse**](../Model/EvaluationApiEvaluationsV1EvaluationDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getObservation()`

```php
getObservation($tenantId, $observationId): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationResponse
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
    $result = $apiInstance->getObservation($tenantId, $observationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getObservation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **observationId** | **string**|  | |

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

## `getObservationCount()`

```php
getObservationCount($tenantId): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationCountResponse
```



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
$tenantId = 'tenantId_example'; // string

try {
    $result = $apiInstance->getObservationCount($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->getObservationCount: ', $e->getMessage(), PHP_EOL;
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

## `searchObservationCampuses()`

```php
searchObservationCampuses($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel
```

Searches the Campuses associated with an Observation for a given Tenant.

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
$filter = ''; // string | 

try {
    $result = $apiInstance->searchObservationCampuses($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->searchObservationCampuses: ', $e->getMessage(), PHP_EOL;
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

## `searchObservationEvaluees()`

```php
searchObservationEvaluees($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse
```

Searches the Staff associated with an Observation for a given Tenant.

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
$filter = ''; // string | 

try {
    $result = $apiInstance->searchObservationEvaluees($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->searchObservationEvaluees: ', $e->getMessage(), PHP_EOL;
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

## `searchObservationForms()`

```php
searchObservationForms($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel
```

Searches the Forms associated with an Observation for a given Tenant.

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
$filter = ''; // string | 

try {
    $result = $apiInstance->searchObservationForms($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->searchObservationForms: ', $e->getMessage(), PHP_EOL;
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

## `searchObservationObservers()`

```php
searchObservationObservers($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse
```

Searches the Appraisers associated with an Observation for a given Tenant.

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
$filter = ''; // string | 

try {
    $result = $apiInstance->searchObservationObservers($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->searchObservationObservers: ', $e->getMessage(), PHP_EOL;
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

## `searchObservations()`

```php
searchObservations($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel
```

Searches the Observations for a given tenant

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
$filter = ''; // string | 

try {
    $result = $apiInstance->searchObservations($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationsApi->searchObservations: ', $e->getMessage(), PHP_EOL;
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

## `updateObservation()`

```php
updateObservation($tenantId, $observationId, $evaluationApiEvaluationsV1UpdateEvaluationRequest): \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1EvaluationUpdatedResponse
```

Updates an Observation for a given tenant

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
$evaluationApiEvaluationsV1UpdateEvaluationRequest = new \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1UpdateEvaluationRequest(); // \EdGraph\PlatformClient\Model\EvaluationApiEvaluationsV1UpdateEvaluationRequest | 

try {
    $result = $apiInstance->updateObservation($tenantId, $observationId, $evaluationApiEvaluationsV1UpdateEvaluationRequest);
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
