# EdGraph\PlatformClient\SubmissionsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createSubmission()**](SubmissionsApi.md#createSubmission) | **POST** /tenants/{tenantId}/forms/{formId}/submissions | Creates a new Submission for a given question |
| [**deleteSubmission()**](SubmissionsApi.md#deleteSubmission) | **DELETE** /tenants/{tenantId}/forms/{formId}/submissions/{submissionId} | Deletes a Submission. |
| [**exportSubmissions()**](SubmissionsApi.md#exportSubmissions) | **GET** /tenants/{tenantId}/forms/{formId}/submissions/export | Exports Submission data for a Form for a given tenant. (With JSON and CSV support) |
| [**getSubmission()**](SubmissionsApi.md#getSubmission) | **GET** /tenants/{tenantId}/forms/{formId}/submissions/{submissionId} | Get Submission. |
| [**searchSubmissions()**](SubmissionsApi.md#searchSubmissions) | **GET** /tenants/{tenantId}/forms/{formId}/submissions | Search Submissions |
| [**updateSubmission()**](SubmissionsApi.md#updateSubmission) | **PUT** /tenants/{tenantId}/forms/{formId}/submissions/{submissionId} | Updates a Submission. |


## `createSubmission()`

```php
createSubmission($tenantId, $formId, $formApiSubmissionsV1CreateSubmissionRequest): \EdGraph\PlatformClient\Model\FormApiSubmissionsV1SubmissionCreatedResponse
```

Creates a new Submission for a given question

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$formApiSubmissionsV1CreateSubmissionRequest = new \EdGraph\PlatformClient\Model\FormApiSubmissionsV1CreateSubmissionRequest(); // \EdGraph\PlatformClient\Model\FormApiSubmissionsV1CreateSubmissionRequest | 

try {
    $result = $apiInstance->createSubmission($tenantId, $formId, $formApiSubmissionsV1CreateSubmissionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubmissionsApi->createSubmission: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **formApiSubmissionsV1CreateSubmissionRequest** | [**\EdGraph\PlatformClient\Model\FormApiSubmissionsV1CreateSubmissionRequest**](../Model/FormApiSubmissionsV1CreateSubmissionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiSubmissionsV1SubmissionCreatedResponse**](../Model/FormApiSubmissionsV1SubmissionCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteSubmission()`

```php
deleteSubmission($tenantId, $formId, $submissionId): \EdGraph\PlatformClient\Model\FormApiSubmissionsV1SubmissionDeletedResponse
```

Deletes a Submission.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 

try {
    $result = $apiInstance->deleteSubmission($tenantId, $formId, $submissionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubmissionsApi->deleteSubmission: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **submissionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiSubmissionsV1SubmissionDeletedResponse**](../Model/FormApiSubmissionsV1SubmissionDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `exportSubmissions()`

```php
exportSubmissions($tenantId, $formId, $type): \EdGraph\PlatformClient\Model\FormApiSubmissionsV1SubmissionsExportedResponse
```

Exports Submission data for a Form for a given tenant. (With JSON and CSV support)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$type = new \EdGraph\PlatformClient\Model\FormApiSubmissionsV1ExportType(); // FormApiSubmissionsV1ExportType | 

try {
    $result = $apiInstance->exportSubmissions($tenantId, $formId, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubmissionsApi->exportSubmissions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **type** | [**FormApiSubmissionsV1ExportType**](../Model/.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiSubmissionsV1SubmissionsExportedResponse**](../Model/FormApiSubmissionsV1SubmissionsExportedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSubmission()`

```php
getSubmission($tenantId, $formId, $submissionId): \EdGraph\PlatformClient\Model\FormApiSubmissionsV1SubmissionResponse
```

Get Submission.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 

try {
    $result = $apiInstance->getSubmission($tenantId, $formId, $submissionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubmissionsApi->getSubmission: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **submissionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiSubmissionsV1SubmissionResponse**](../Model/FormApiSubmissionsV1SubmissionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchSubmissions()`

```php
searchSubmissions($tenantId, $formId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\FormApiSubmissionsV1SubmissionResponsePaginatedItemsViewModel
```

Search Submissions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SubmissionsApi(
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
    $result = $apiInstance->searchSubmissions($tenantId, $formId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubmissionsApi->searchSubmissions: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\FormApiSubmissionsV1SubmissionResponsePaginatedItemsViewModel**](../Model/FormApiSubmissionsV1SubmissionResponsePaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSubmission()`

```php
updateSubmission($tenantId, $formId, $submissionId, $formApiSubmissionsV1UpdateSubmissionRequest): \EdGraph\PlatformClient\Model\FormApiSubmissionsV1SubmissionUpdatedResponse
```

Updates a Submission.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\SubmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$submissionId = 'submissionId_example'; // string | 
$formApiSubmissionsV1UpdateSubmissionRequest = new \EdGraph\PlatformClient\Model\FormApiSubmissionsV1UpdateSubmissionRequest(); // \EdGraph\PlatformClient\Model\FormApiSubmissionsV1UpdateSubmissionRequest | 

try {
    $result = $apiInstance->updateSubmission($tenantId, $formId, $submissionId, $formApiSubmissionsV1UpdateSubmissionRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubmissionsApi->updateSubmission: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **submissionId** | **string**|  | |
| **formApiSubmissionsV1UpdateSubmissionRequest** | [**\EdGraph\PlatformClient\Model\FormApiSubmissionsV1UpdateSubmissionRequest**](../Model/FormApiSubmissionsV1UpdateSubmissionRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiSubmissionsV1SubmissionUpdatedResponse**](../Model/FormApiSubmissionsV1SubmissionUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
