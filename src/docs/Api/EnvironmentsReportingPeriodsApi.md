# EdGraph\PlatformClient\EnvironmentsReportingPeriodsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**cancelStateReportingPeriodRun()**](EnvironmentsReportingPeriodsApi.md#cancelStateReportingPeriodRun) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/run | Cancel the Validation Run of a Reporting Period. |
| [**closeStateReportingPeriod()**](EnvironmentsReportingPeriodsApi.md#closeStateReportingPeriod) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/close | Closes a Reporting Period. |
| [**createStateReportingPeriod()**](EnvironmentsReportingPeriodsApi.md#createStateReportingPeriod) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods | Creates a new Reporting Period. |
| [**deleteStateReportingPeriod()**](EnvironmentsReportingPeriodsApi.md#deleteStateReportingPeriod) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId} | Deletes a Reporting Period. |
| [**getStateReportingPeriod()**](EnvironmentsReportingPeriodsApi.md#getStateReportingPeriod) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId} | Retrieves a Reporting Period by ID. |
| [**getStateReportingPeriodCertificationStatus()**](EnvironmentsReportingPeriodsApi.md#getStateReportingPeriodCertificationStatus) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/certificationstatus | Retrieves the Certification Status of Reporting Period. |
| [**getStateReportingPeriodValidationSummary()**](EnvironmentsReportingPeriodsApi.md#getStateReportingPeriodValidationSummary) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/validationsummary | Retrieves the Validation Summary of Reporting Period. |
| [**getStateReportingPeriodValidationSummaryByCategory()**](EnvironmentsReportingPeriodsApi.md#getStateReportingPeriodValidationSummaryByCategory) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/validationsummary/categories/{categoryId} | Retrieves the Validation Summary of Reporting Period by Category. |
| [**postStateReportingPeriod()**](EnvironmentsReportingPeriodsApi.md#postStateReportingPeriod) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/post | Posts a Reporting Period. |
| [**runStateReportingPeriod()**](EnvironmentsReportingPeriodsApi.md#runStateReportingPeriod) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/run | Run a Reporting Period. |
| [**searchStateReportingPeriods()**](EnvironmentsReportingPeriodsApi.md#searchStateReportingPeriods) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods | Retrieves a list of Reporting Periods. |
| [**setStateReportingPeriodCurrentStep()**](EnvironmentsReportingPeriodsApi.md#setStateReportingPeriodCurrentStep) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/steps/current | Sets the current step of a Reporting Period. |
| [**setStateReportingPeriodStepStatus()**](EnvironmentsReportingPeriodsApi.md#setStateReportingPeriodStepStatus) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/steps/{stepNumber} | Sets the status of a Reporting Period step. |
| [**toggleStateReportingPeriodSelected()**](EnvironmentsReportingPeriodsApi.md#toggleStateReportingPeriodSelected) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/toggle | Toggles the Selected state of a Reporting Period. |
| [**updateStateReportingPeriod()**](EnvironmentsReportingPeriodsApi.md#updateStateReportingPeriod) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId} | Updates a Reporting Period. |
| [**updateStateReportingPeriodBulk()**](EnvironmentsReportingPeriodsApi.md#updateStateReportingPeriodBulk) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods | Updates Reporting Periods in bulk. |


## `cancelStateReportingPeriodRun()`

```php
cancelStateReportingPeriodRun($tenantId, $environmentId, $reportingPeriodId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodValidationsCancelledResponse
```

Cancel the Validation Run of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->cancelStateReportingPeriodRun($tenantId, $environmentId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->cancelStateReportingPeriodRun: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodValidationsCancelledResponse**](../Model/EdGraphServicesStateReportingV1ReportingPeriodValidationsCancelledResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `closeStateReportingPeriod()`

```php
closeStateReportingPeriod($tenantId, $environmentId, $reportingPeriodId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse
```

Closes a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->closeStateReportingPeriod($tenantId, $environmentId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->closeStateReportingPeriod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse**](../Model/EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createStateReportingPeriod()`

```php
createStateReportingPeriod($tenantId, $environmentId, $edGraphServicesStateReportingV1CreateReportingPeriodRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse
```

Creates a new Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$edGraphServicesStateReportingV1CreateReportingPeriodRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1CreateReportingPeriodRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1CreateReportingPeriodRequest | 

try {
    $result = $apiInstance->createStateReportingPeriod($tenantId, $environmentId, $edGraphServicesStateReportingV1CreateReportingPeriodRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->createStateReportingPeriod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **edGraphServicesStateReportingV1CreateReportingPeriodRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1CreateReportingPeriodRequest**](../Model/EdGraphServicesStateReportingV1CreateReportingPeriodRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse**](../Model/EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteStateReportingPeriod()`

```php
deleteStateReportingPeriod($tenantId, $environmentId, $reportingPeriodId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodDeletedResponse
```

Deletes a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->deleteStateReportingPeriod($tenantId, $environmentId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->deleteStateReportingPeriod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodDeletedResponse**](../Model/EdGraphServicesStateReportingV1ReportingPeriodDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStateReportingPeriod()`

```php
getStateReportingPeriod($tenantId, $environmentId, $reportingPeriodId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodProfileResponse
```

Retrieves a Reporting Period by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->getStateReportingPeriod($tenantId, $environmentId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->getStateReportingPeriod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodProfileResponse**](../Model/EdGraphServicesStateReportingV1ReportingPeriodProfileResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStateReportingPeriodCertificationStatus()`

```php
getStateReportingPeriodCertificationStatus($tenantId, $environmentId, $reportingPeriodId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodCertificationStatus
```

Retrieves the Certification Status of Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->getStateReportingPeriodCertificationStatus($tenantId, $environmentId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->getStateReportingPeriodCertificationStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodCertificationStatus**](../Model/EdGraphServicesStateReportingV1ReportingPeriodCertificationStatus.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStateReportingPeriodValidationSummary()`

```php
getStateReportingPeriodValidationSummary($tenantId, $environmentId, $reportingPeriodId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodValidationSummary
```

Retrieves the Validation Summary of Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->getStateReportingPeriodValidationSummary($tenantId, $environmentId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->getStateReportingPeriodValidationSummary: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodValidationSummary**](../Model/EdGraphServicesStateReportingV1ReportingPeriodValidationSummary.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStateReportingPeriodValidationSummaryByCategory()`

```php
getStateReportingPeriodValidationSummaryByCategory($tenantId, $environmentId, $reportingPeriodId, $categoryId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodValidationSummaryByCategoryId
```

Retrieves the Validation Summary of Reporting Period by Category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$categoryId = 'categoryId_example'; // string | 

try {
    $result = $apiInstance->getStateReportingPeriodValidationSummaryByCategory($tenantId, $environmentId, $reportingPeriodId, $categoryId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->getStateReportingPeriodValidationSummaryByCategory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **categoryId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodValidationSummaryByCategoryId**](../Model/EdGraphServicesStateReportingV1ReportingPeriodValidationSummaryByCategoryId.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postStateReportingPeriod()`

```php
postStateReportingPeriod($tenantId, $environmentId, $reportingPeriodId, $edGraphServicesStateReportingV1PostReportingPeriodRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodPostedResponse
```

Posts a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$edGraphServicesStateReportingV1PostReportingPeriodRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PostReportingPeriodRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PostReportingPeriodRequest | 

try {
    $result = $apiInstance->postStateReportingPeriod($tenantId, $environmentId, $reportingPeriodId, $edGraphServicesStateReportingV1PostReportingPeriodRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->postStateReportingPeriod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **edGraphServicesStateReportingV1PostReportingPeriodRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PostReportingPeriodRequest**](../Model/EdGraphServicesStateReportingV1PostReportingPeriodRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodPostedResponse**](../Model/EdGraphServicesStateReportingV1ReportingPeriodPostedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `runStateReportingPeriod()`

```php
runStateReportingPeriod($tenantId, $environmentId, $reportingPeriodId, $edGraphServicesStateReportingV1RunReportingPeriodRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodRunResponse
```

Run a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$edGraphServicesStateReportingV1RunReportingPeriodRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1RunReportingPeriodRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1RunReportingPeriodRequest | 

try {
    $result = $apiInstance->runStateReportingPeriod($tenantId, $environmentId, $reportingPeriodId, $edGraphServicesStateReportingV1RunReportingPeriodRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->runStateReportingPeriod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **edGraphServicesStateReportingV1RunReportingPeriodRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1RunReportingPeriodRequest**](../Model/EdGraphServicesStateReportingV1RunReportingPeriodRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodRunResponse**](../Model/EdGraphServicesStateReportingV1ReportingPeriodRunResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchStateReportingPeriods()`

```php
searchStateReportingPeriods($tenantId, $environmentId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedReportingPeriods
```

Retrieves a list of Reporting Periods.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$orderBy = 'orderBy_example'; // string | 
$filter = 'filter_example'; // string | 

try {
    $result = $apiInstance->searchStateReportingPeriods($tenantId, $environmentId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->searchStateReportingPeriods: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **orderBy** | **string**|  | [optional] |
| **filter** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedReportingPeriods**](../Model/EdGraphServicesStateReportingV1PaginatedReportingPeriods.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setStateReportingPeriodCurrentStep()`

```php
setStateReportingPeriodCurrentStep($tenantId, $environmentId, $reportingPeriodId, $edGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodCurrentStepSetResponse
```

Sets the current step of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$edGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest | 

try {
    $result = $apiInstance->setStateReportingPeriodCurrentStep($tenantId, $environmentId, $reportingPeriodId, $edGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->setStateReportingPeriodCurrentStep: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **edGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest**](../Model/EdGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodCurrentStepSetResponse**](../Model/EdGraphServicesStateReportingV1ReportingPeriodCurrentStepSetResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setStateReportingPeriodStepStatus()`

```php
setStateReportingPeriodStepStatus($tenantId, $environmentId, $reportingPeriodId, $stepNumber, $edGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse
```

Sets the status of a Reporting Period step.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$stepNumber = 56; // int | 
$edGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest | 

try {
    $result = $apiInstance->setStateReportingPeriodStepStatus($tenantId, $environmentId, $reportingPeriodId, $stepNumber, $edGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->setStateReportingPeriodStepStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **stepNumber** | **int**|  | |
| **edGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest**](../Model/EdGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse**](../Model/EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `toggleStateReportingPeriodSelected()`

```php
toggleStateReportingPeriodSelected($tenantId, $environmentId, $reportingPeriodId, $edGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodToggledResponse
```

Toggles the Selected state of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$edGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest | 

try {
    $result = $apiInstance->toggleStateReportingPeriodSelected($tenantId, $environmentId, $reportingPeriodId, $edGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->toggleStateReportingPeriodSelected: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **edGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest**](../Model/EdGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodToggledResponse**](../Model/EdGraphServicesStateReportingV1ReportingPeriodToggledResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateStateReportingPeriod()`

```php
updateStateReportingPeriod($tenantId, $environmentId, $reportingPeriodId, $edGraphServicesStateReportingV1UpdateReportingPeriodRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodUpdatedResponse
```

Updates a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$edGraphServicesStateReportingV1UpdateReportingPeriodRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1UpdateReportingPeriodRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1UpdateReportingPeriodRequest | 

try {
    $result = $apiInstance->updateStateReportingPeriod($tenantId, $environmentId, $reportingPeriodId, $edGraphServicesStateReportingV1UpdateReportingPeriodRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->updateStateReportingPeriod: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **edGraphServicesStateReportingV1UpdateReportingPeriodRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1UpdateReportingPeriodRequest**](../Model/EdGraphServicesStateReportingV1UpdateReportingPeriodRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodUpdatedResponse**](../Model/EdGraphServicesStateReportingV1ReportingPeriodUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateStateReportingPeriodBulk()`

```php
updateStateReportingPeriodBulk($tenantId, $environmentId, $edGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodUpdatedBulkResponse
```

Updates Reporting Periods in bulk.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$edGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest | 

try {
    $result = $apiInstance->updateStateReportingPeriodBulk($tenantId, $environmentId, $edGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsApi->updateStateReportingPeriodBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **edGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest**](../Model/EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodUpdatedBulkResponse**](../Model/EdGraphServicesStateReportingV1ReportingPeriodUpdatedBulkResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
