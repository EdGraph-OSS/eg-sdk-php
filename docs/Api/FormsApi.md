# EdGraph\PlatformClient\FormsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createForm()**](FormsApi.md#createForm) | **POST** /tenants/{tenantId}/forms | Creates a new Form for a given tenant |
| [**createFullForm()**](FormsApi.md#createFullForm) | **POST** /tenants/{tenantId}/forms/full | Fully creates a new Form for a given tenant (with Sections and Questions). |
| [**deleteForm()**](FormsApi.md#deleteForm) | **DELETE** /tenants/{tenantId}/forms/{formId} | Deletes a Form. |
| [**duplicateForm()**](FormsApi.md#duplicateForm) | **POST** /tenants/{tenantId}/forms/{formId}/duplicate | Duplicates all Form data for a given tenant (with Sections and Questions). |
| [**getForm()**](FormsApi.md#getForm) | **GET** /tenants/{tenantId}/forms/{formId} | Get Form. |
| [**getFormAccess()**](FormsApi.md#getFormAccess) | **GET** /tenants/{tenantId}/forms/{formId}/access | Get the Access Type for a Form. |
| [**importForm()**](FormsApi.md#importForm) | **POST** /tenants/{tenantId}/forms/import | Imports all form data for a given tenant. |
| [**searchForms()**](FormsApi.md#searchForms) | **GET** /tenants/{tenantId}/forms | Search Forms |
| [**setFormAccess()**](FormsApi.md#setFormAccess) | **PUT** /tenants/{tenantId}/forms/{formId}/access | Sets the Access Type for a Form. |
| [**updateForm()**](FormsApi.md#updateForm) | **PUT** /tenants/{tenantId}/forms/{formId} | Updates a Form. |
| [**updateFullForm()**](FormsApi.md#updateFullForm) | **PUT** /tenants/{tenantId}/forms/{formId}/full | Fully updates a Form for a given tenant (with Sections and Questions). |


## `createForm()`

```php
createForm($tenantId, $formApiFormsV1CreateFormRequest): \EdGraph\PlatformClient\Model\FormApiFormsV1FormCreatedResponse
```

Creates a new Form for a given tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\FormsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formApiFormsV1CreateFormRequest = new \EdGraph\PlatformClient\Model\FormApiFormsV1CreateFormRequest(); // \EdGraph\PlatformClient\Model\FormApiFormsV1CreateFormRequest | 

try {
    $result = $apiInstance->createForm($tenantId, $formApiFormsV1CreateFormRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FormsApi->createForm: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formApiFormsV1CreateFormRequest** | [**\EdGraph\PlatformClient\Model\FormApiFormsV1CreateFormRequest**](../Model/FormApiFormsV1CreateFormRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiFormsV1FormCreatedResponse**](../Model/FormApiFormsV1FormCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createFullForm()`

```php
createFullForm($tenantId, $formApiFormsV1CreateFullFormRequest): \EdGraph\PlatformClient\Model\FormApiFormsV1FullFormCreatedResponse
```

Fully creates a new Form for a given tenant (with Sections and Questions).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\FormsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formApiFormsV1CreateFullFormRequest = new \EdGraph\PlatformClient\Model\FormApiFormsV1CreateFullFormRequest(); // \EdGraph\PlatformClient\Model\FormApiFormsV1CreateFullFormRequest | 

try {
    $result = $apiInstance->createFullForm($tenantId, $formApiFormsV1CreateFullFormRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FormsApi->createFullForm: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formApiFormsV1CreateFullFormRequest** | [**\EdGraph\PlatformClient\Model\FormApiFormsV1CreateFullFormRequest**](../Model/FormApiFormsV1CreateFullFormRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiFormsV1FullFormCreatedResponse**](../Model/FormApiFormsV1FullFormCreatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteForm()`

```php
deleteForm($tenantId, $formId): \EdGraph\PlatformClient\Model\FormApiFormsV1FormDeletedResponse
```

Deletes a Form.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\FormsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 

try {
    $result = $apiInstance->deleteForm($tenantId, $formId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FormsApi->deleteForm: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiFormsV1FormDeletedResponse**](../Model/FormApiFormsV1FormDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `duplicateForm()`

```php
duplicateForm($tenantId, $formId): \EdGraph\PlatformClient\Model\FormApiFormsV1FormDuplicatedResponse
```

Duplicates all Form data for a given tenant (with Sections and Questions).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\FormsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 

try {
    $result = $apiInstance->duplicateForm($tenantId, $formId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FormsApi->duplicateForm: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiFormsV1FormDuplicatedResponse**](../Model/FormApiFormsV1FormDuplicatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getForm()`

```php
getForm($tenantId, $formId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesFormsV1Form
```

Get Form.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\FormsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 

try {
    $result = $apiInstance->getForm($tenantId, $formId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FormsApi->getForm: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesFormsV1Form**](../Model/EdGraphHttpAggregatorsTenantApiServicesFormsV1Form.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getFormAccess()`

```php
getFormAccess($tenantId, $formId): \EdGraph\PlatformClient\Model\FormApiFormsV1FormAccessResponse
```

Get the Access Type for a Form.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\FormsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 

try {
    $result = $apiInstance->getFormAccess($tenantId, $formId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FormsApi->getFormAccess: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiFormsV1FormAccessResponse**](../Model/FormApiFormsV1FormAccessResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `importForm()`

```php
importForm($tenantId, $body): object
```

Imports all form data for a given tenant.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\FormsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$body = array('key' => new \stdClass); // object | 

try {
    $result = $apiInstance->importForm($tenantId, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FormsApi->importForm: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **body** | **object**|  | [optional] |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchForms()`

```php
searchForms($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesFormsV1FormPaginatedItemsViewModel
```

Search Forms

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\FormsApi(
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
    $result = $apiInstance->searchForms($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FormsApi->searchForms: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesFormsV1FormPaginatedItemsViewModel**](../Model/EdGraphHttpAggregatorsTenantApiServicesFormsV1FormPaginatedItemsViewModel.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setFormAccess()`

```php
setFormAccess($tenantId, $formId, $formApiFormsV1SetFormAccessRequest): \EdGraph\PlatformClient\Model\FormApiFormsV1FormAccessSetResponse
```

Sets the Access Type for a Form.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\FormsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$formApiFormsV1SetFormAccessRequest = new \EdGraph\PlatformClient\Model\FormApiFormsV1SetFormAccessRequest(); // \EdGraph\PlatformClient\Model\FormApiFormsV1SetFormAccessRequest | 

try {
    $result = $apiInstance->setFormAccess($tenantId, $formId, $formApiFormsV1SetFormAccessRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FormsApi->setFormAccess: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **formApiFormsV1SetFormAccessRequest** | [**\EdGraph\PlatformClient\Model\FormApiFormsV1SetFormAccessRequest**](../Model/FormApiFormsV1SetFormAccessRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiFormsV1FormAccessSetResponse**](../Model/FormApiFormsV1FormAccessSetResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateForm()`

```php
updateForm($tenantId, $formId, $formApiFormsV1UpdateFormRequest): \EdGraph\PlatformClient\Model\FormApiFormsV1FormUpdatedResponse
```

Updates a Form.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\FormsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$formApiFormsV1UpdateFormRequest = new \EdGraph\PlatformClient\Model\FormApiFormsV1UpdateFormRequest(); // \EdGraph\PlatformClient\Model\FormApiFormsV1UpdateFormRequest | 

try {
    $result = $apiInstance->updateForm($tenantId, $formId, $formApiFormsV1UpdateFormRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FormsApi->updateForm: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **formApiFormsV1UpdateFormRequest** | [**\EdGraph\PlatformClient\Model\FormApiFormsV1UpdateFormRequest**](../Model/FormApiFormsV1UpdateFormRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiFormsV1FormUpdatedResponse**](../Model/FormApiFormsV1FormUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateFullForm()`

```php
updateFullForm($tenantId, $formId, $formApiFormsV1UpdateFullFormRequest): \EdGraph\PlatformClient\Model\FormApiFormsV1FullFormUpdatedResponse
```

Fully updates a Form for a given tenant (with Sections and Questions).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\FormsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$formId = 'formId_example'; // string | 
$formApiFormsV1UpdateFullFormRequest = new \EdGraph\PlatformClient\Model\FormApiFormsV1UpdateFullFormRequest(); // \EdGraph\PlatformClient\Model\FormApiFormsV1UpdateFullFormRequest | 

try {
    $result = $apiInstance->updateFullForm($tenantId, $formId, $formApiFormsV1UpdateFullFormRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FormsApi->updateFullForm: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **formId** | **string**|  | |
| **formApiFormsV1UpdateFullFormRequest** | [**\EdGraph\PlatformClient\Model\FormApiFormsV1UpdateFullFormRequest**](../Model/FormApiFormsV1UpdateFullFormRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\FormApiFormsV1FullFormUpdatedResponse**](../Model/FormApiFormsV1FullFormUpdatedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
