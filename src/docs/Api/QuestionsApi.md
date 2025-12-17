# EdGraph\PlatformClient\QuestionsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createQuestion()**](QuestionsApi.md#createQuestion) | **POST** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions | Creates a new Question for a given section |
| [**deleteQuestion()**](QuestionsApi.md#deleteQuestion) | **DELETE** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions/{questionId} | Deletes a Question. |
| [**getQuestion()**](QuestionsApi.md#getQuestion) | **GET** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions/{questionId} | Get Question. |
| [**searchQuestions()**](QuestionsApi.md#searchQuestions) | **GET** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions | Search Questions |
| [**updateQuestion()**](QuestionsApi.md#updateQuestion) | **PUT** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions/{questionId} | Updates a Question. |


## `createQuestion()`

```php
createQuestion($tenantId, $formId, $sectionId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto): \EdGraph\PlatformClient\Model\FormApiQuestionsV1QuestionCreatedResponse
```

Creates a new Question for a given section

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\QuestionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$sectionId = 'sectionId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto | 

try {
    $result = $apiInstance->createQuestion($tenantId, $formId, $sectionId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QuestionsApi->createQuestion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **sectionId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiQuestionsV1QuestionCreatedResponse**](../Model/FormApiQuestionsV1QuestionCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteQuestion()`

```php
deleteQuestion($tenantId, $formId, $sectionId, $questionId): \EdGraph\PlatformClient\Model\FormApiQuestionsV1QuestionDeletedResponse
```

Deletes a Question.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\QuestionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$sectionId = 'sectionId_example'; // string | 
$questionId = 'questionId_example'; // string | 

try {
    $result = $apiInstance->deleteQuestion($tenantId, $formId, $sectionId, $questionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QuestionsApi->deleteQuestion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **sectionId** | **string**|  | |
| **questionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiQuestionsV1QuestionDeletedResponse**](../Model/FormApiQuestionsV1QuestionDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getQuestion()`

```php
getQuestion($tenantId, $formId, $sectionId, $questionId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDto
```

Get Question.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\QuestionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$sectionId = 'sectionId_example'; // string | 
$questionId = 'questionId_example'; // string | 

try {
    $result = $apiInstance->getQuestion($tenantId, $formId, $sectionId, $questionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QuestionsApi->getQuestion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **sectionId** | **string**|  | |
| **questionId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchQuestions()`

```php
searchQuestions($tenantId, $formId, $sectionId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel
```

Search Questions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\QuestionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$sectionId = 'sectionId_example'; // string | 
$pageSize = 10; // int | 
$pageIndex = 0; // int | 
$orderBy = ''; // string | 
$filter = ''; // string | 

try {
    $result = $apiInstance->searchQuestions($tenantId, $formId, $sectionId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QuestionsApi->searchQuestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **sectionId** | **string**|  | |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **orderBy** | **string**|  | [optional] [default to &#39;&#39;] |
| **filter** | **string**|  | [optional] [default to &#39;&#39;] |

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

## `updateQuestion()`

```php
updateQuestion($tenantId, $formId, $sectionId, $questionId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto): \EdGraph\PlatformClient\Model\FormApiQuestionsV1QuestionUpdatedResponse
```

Updates a Question.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\QuestionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$sectionId = 'sectionId_example'; // string | 
$questionId = 'questionId_example'; // string | 
$edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto | 

try {
    $result = $apiInstance->updateQuestion($tenantId, $formId, $sectionId, $questionId, $edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QuestionsApi->updateQuestion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **sectionId** | **string**|  | |
| **questionId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto**](../Model/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiQuestionsV1QuestionUpdatedResponse**](../Model/FormApiQuestionsV1QuestionUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
