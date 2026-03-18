# EdGraph\PlatformClient\ObservationsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createObservation()**](ObservationsApi.md#createObservation) | **POST** /tenants/{tenantId}/observations | Creates a new Observation for a given tenant |
| [**deleteObservation()**](ObservationsApi.md#deleteObservation) | **DELETE** /tenants/{tenantId}/observations/{observationId} | Deletes an Observation for a given tenant |
| [**getObservationById()**](ObservationsApi.md#getObservationById) | **GET** /tenants/{tenantId}/observations/{observationId} | Get an Observation for a given tenant |
| [**getPaginatedAvailableCampuses()**](ObservationsApi.md#getPaginatedAvailableCampuses) | **GET** /tenants/{tenantId}/observations/campuses | Get Available Campuses |
| [**getPaginatedAvailableForms()**](ObservationsApi.md#getPaginatedAvailableForms) | **GET** /tenants/{tenantId}/observations/forms/available | Get Paginated Available Forms |
| [**getPaginatedEvaluees()**](ObservationsApi.md#getPaginatedEvaluees) | **GET** /tenants/{tenantId}/observations/evaluees | Get paginated evaluees |
| [**getPaginatedObservations()**](ObservationsApi.md#getPaginatedObservations) | **GET** /tenants/{tenantId}/observations | Get Paginated Observations for a given tenant |
| [**getSubmittedObservationsCount()**](ObservationsApi.md#getSubmittedObservationsCount) | **GET** /tenants/{tenantId}/submittedobservations | Get submitted Observations count |


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

## `getPaginatedAvailableCampuses()`

```php
getPaginatedAvailableCampuses($tenantId, $pageSize, $pageIndex, $orderBy): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse
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

try {
    $result = $apiInstance->getPaginatedAvailableCampuses($tenantId, $pageSize, $pageIndex, $orderBy);
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
getPaginatedAvailableForms($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse
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

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse.md)

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
getPaginatedEvaluees($tenantId, $pageSize, $pageIndex, $orderBy, $campus, $evalueeId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse
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

try {
    $result = $apiInstance->getPaginatedEvaluees($tenantId, $pageSize, $pageIndex, $orderBy, $campus, $evalueeId);
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
