# EdGraph\PlatformClient\ValidationResultsAPIApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**findResultsApiJobRunRecordsAsync()**](ValidationResultsAPIApi.md#findResultsApiJobRunRecordsAsync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/records | Retrieves a list of Job Run Records from the Validation Results API. |
| [**findResultsApiJobRunRuleRecordsAsync()**](ValidationResultsAPIApi.md#findResultsApiJobRunRuleRecordsAsync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/{ruleId}/records | Retrieves a list of Job Run Rule Records from the Validation Results API. |
| [**findResultsApiJobRunRulesAsync()**](ValidationResultsAPIApi.md#findResultsApiJobRunRulesAsync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules | Retrieves a list of Job Run Rules from the Validation Results API. |
| [**findResultsApiJobRunsAsync()**](ValidationResultsAPIApi.md#findResultsApiJobRunsAsync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs | Retrieves a list of Job Runs from the Validation Results API. |
| [**findResultsApiJobsAsync()**](ValidationResultsAPIApi.md#findResultsApiJobsAsync) | **GET** /tenants/{tenantId}/validations/results-api/jobs | Retrieves a list of Jobs from the Validation Results API. |
| [**findResultsApiRuleSummaries()**](ValidationResultsAPIApi.md#findResultsApiRuleSummaries) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/summary | Retrieves a list Rule Summaries from the Validation Results API. |
| [**findResultsApiRulesAsync()**](ValidationResultsAPIApi.md#findResultsApiRulesAsync) | **GET** /tenants/{tenantId}/validations/results-api/rules | Retrieves a list of Rules from Validation Results API. |
| [**getLatestJobRunAsync()**](ValidationResultsAPIApi.md#getLatestJobRunAsync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/latest | Retrieves the latest Job Run from the Validation Results API. |
| [**getResultsApiJobById()**](ValidationResultsAPIApi.md#getResultsApiJobById) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId} | Retrieves a Job by ID from the Validation Results API. |
| [**getResultsApiJobRunByIdAsync()**](ValidationResultsAPIApi.md#getResultsApiJobRunByIdAsync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId} | Retrieves a Job Run by ID from the Validation Results API. |
| [**getResultsApiJobRunRuleByIdAsync()**](ValidationResultsAPIApi.md#getResultsApiJobRunRuleByIdAsync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/{ruleId} | Retrieves a Job Run Rule by ID from the Validation Results API. |
| [**getResultsApiRuleByIdAsync()**](ValidationResultsAPIApi.md#getResultsApiRuleByIdAsync) | **GET** /tenants/{tenantId}/validations/results-api/rules/{ruleId} | Retrieves a Rule by ID from the Validation Results API. |
| [**getResultsApiRuleSummary()**](ValidationResultsAPIApi.md#getResultsApiRuleSummary) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/{ruleId}/summary | Get Rule Summary by ID from the Validation Results API. |


## `findResultsApiJobRunRecordsAsync()`

```php
findResultsApiJobRunRecordsAsync($tenantId, $jobId, $runId, $offset, $limit): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto[]
```

Retrieves a list of Job Run Records from the Validation Results API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ValidationResultsAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$runId = 'runId_example'; // string | 
$offset = 0; // int | 
$limit = 25; // int | 

try {
    $result = $apiInstance->findResultsApiJobRunRecordsAsync($tenantId, $jobId, $runId, $offset, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationResultsAPIApi->findResultsApiJobRunRecordsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **runId** | **string**|  | |
| **offset** | **int**|  | [optional] [default to 0] |
| **limit** | **int**|  | [optional] [default to 25] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto[]**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `findResultsApiJobRunRuleRecordsAsync()`

```php
findResultsApiJobRunRuleRecordsAsync($tenantId, $jobId, $runId, $ruleId, $offset, $limit): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto[]
```

Retrieves a list of Job Run Rule Records from the Validation Results API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ValidationResultsAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$runId = 'runId_example'; // string | 
$ruleId = 'ruleId_example'; // string | 
$offset = 0; // int | 
$limit = 25; // int | 

try {
    $result = $apiInstance->findResultsApiJobRunRuleRecordsAsync($tenantId, $jobId, $runId, $ruleId, $offset, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationResultsAPIApi->findResultsApiJobRunRuleRecordsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **runId** | **string**|  | |
| **ruleId** | **string**|  | |
| **offset** | **int**|  | [optional] [default to 0] |
| **limit** | **int**|  | [optional] [default to 25] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto[]**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `findResultsApiJobRunRulesAsync()`

```php
findResultsApiJobRunRulesAsync($tenantId, $jobId, $runId, $offset, $limit): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto[]
```

Retrieves a list of Job Run Rules from the Validation Results API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ValidationResultsAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$runId = 'runId_example'; // string | 
$offset = 0; // int | 
$limit = 25; // int | 

try {
    $result = $apiInstance->findResultsApiJobRunRulesAsync($tenantId, $jobId, $runId, $offset, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationResultsAPIApi->findResultsApiJobRunRulesAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **runId** | **string**|  | |
| **offset** | **int**|  | [optional] [default to 0] |
| **limit** | **int**|  | [optional] [default to 25] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto[]**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `findResultsApiJobRunsAsync()`

```php
findResultsApiJobRunsAsync($tenantId, $jobId, $offset, $limit): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto[]
```

Retrieves a list of Job Runs from the Validation Results API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ValidationResultsAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$offset = 0; // int | 
$limit = 25; // int | 

try {
    $result = $apiInstance->findResultsApiJobRunsAsync($tenantId, $jobId, $offset, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationResultsAPIApi->findResultsApiJobRunsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **offset** | **int**|  | [optional] [default to 0] |
| **limit** | **int**|  | [optional] [default to 25] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto[]**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `findResultsApiJobsAsync()`

```php
findResultsApiJobsAsync($tenantId, $offset, $limit): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto[]
```

Retrieves a list of Jobs from the Validation Results API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ValidationResultsAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$offset = 0; // int | 
$limit = 25; // int | 

try {
    $result = $apiInstance->findResultsApiJobsAsync($tenantId, $offset, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationResultsAPIApi->findResultsApiJobsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **offset** | **int**|  | [optional] [default to 0] |
| **limit** | **int**|  | [optional] [default to 25] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto[]**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `findResultsApiRuleSummaries()`

```php
findResultsApiRuleSummaries($tenantId, $jobId, $runId, $offset, $limit): \EdGraph\PlatformClient\Model\ValidationsApiResultsV1RuleSummary[]
```

Retrieves a list Rule Summaries from the Validation Results API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ValidationResultsAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$runId = 'runId_example'; // string | 
$offset = 0; // int | 
$limit = 25; // int | 

try {
    $result = $apiInstance->findResultsApiRuleSummaries($tenantId, $jobId, $runId, $offset, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationResultsAPIApi->findResultsApiRuleSummaries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **runId** | **string**|  | |
| **offset** | **int**|  | [optional] [default to 0] |
| **limit** | **int**|  | [optional] [default to 25] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiResultsV1RuleSummary[]**](../Model/ValidationsApiResultsV1RuleSummary.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `findResultsApiRulesAsync()`

```php
findResultsApiRulesAsync($tenantId, $offset, $limit): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto[]
```

Retrieves a list of Rules from Validation Results API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ValidationResultsAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$offset = 0; // int | 
$limit = 25; // int | 

try {
    $result = $apiInstance->findResultsApiRulesAsync($tenantId, $offset, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationResultsAPIApi->findResultsApiRulesAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **offset** | **int**|  | [optional] [default to 0] |
| **limit** | **int**|  | [optional] [default to 25] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto[]**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getLatestJobRunAsync()`

```php
getLatestJobRunAsync($tenantId, $jobId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto
```

Retrieves the latest Job Run from the Validation Results API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ValidationResultsAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 

try {
    $result = $apiInstance->getLatestJobRunAsync($tenantId, $jobId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationResultsAPIApi->getLatestJobRunAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getResultsApiJobById()`

```php
getResultsApiJobById($tenantId, $jobId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto
```

Retrieves a Job by ID from the Validation Results API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ValidationResultsAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 

try {
    $result = $apiInstance->getResultsApiJobById($tenantId, $jobId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationResultsAPIApi->getResultsApiJobById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getResultsApiJobRunByIdAsync()`

```php
getResultsApiJobRunByIdAsync($tenantId, $jobId, $runId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto
```

Retrieves a Job Run by ID from the Validation Results API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ValidationResultsAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$runId = 'runId_example'; // string | 

try {
    $result = $apiInstance->getResultsApiJobRunByIdAsync($tenantId, $jobId, $runId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationResultsAPIApi->getResultsApiJobRunByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **runId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getResultsApiJobRunRuleByIdAsync()`

```php
getResultsApiJobRunRuleByIdAsync($tenantId, $jobId, $runId, $ruleId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto
```

Retrieves a Job Run Rule by ID from the Validation Results API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ValidationResultsAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$runId = 'runId_example'; // string | 
$ruleId = 'ruleId_example'; // string | 

try {
    $result = $apiInstance->getResultsApiJobRunRuleByIdAsync($tenantId, $jobId, $runId, $ruleId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationResultsAPIApi->getResultsApiJobRunRuleByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **runId** | **string**|  | |
| **ruleId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getResultsApiRuleByIdAsync()`

```php
getResultsApiRuleByIdAsync($tenantId, $ruleId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto
```

Retrieves a Rule by ID from the Validation Results API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ValidationResultsAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$ruleId = 'ruleId_example'; // string | 

try {
    $result = $apiInstance->getResultsApiRuleByIdAsync($tenantId, $ruleId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationResultsAPIApi->getResultsApiRuleByIdAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **ruleId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getResultsApiRuleSummary()`

```php
getResultsApiRuleSummary($tenantId, $jobId, $runId, $ruleId): \EdGraph\PlatformClient\Model\ValidationsApiResultsV1RuleSummary
```

Get Rule Summary by ID from the Validation Results API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ValidationResultsAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$jobId = 'jobId_example'; // string | 
$runId = 'runId_example'; // string | 
$ruleId = 'ruleId_example'; // string | 

try {
    $result = $apiInstance->getResultsApiRuleSummary($tenantId, $jobId, $runId, $ruleId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationResultsAPIApi->getResultsApiRuleSummary: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **jobId** | **string**|  | |
| **runId** | **string**|  | |
| **ruleId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiResultsV1RuleSummary**](../Model/ValidationsApiResultsV1RuleSummary.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
