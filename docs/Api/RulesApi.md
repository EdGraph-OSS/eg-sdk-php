# EdGraph\PlatformClient\RulesApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createRule()**](RulesApi.md#createRule) | **POST** /tenants/{tenantId}/validations/rules | Creates a Rule. |
| [**deleteRule()**](RulesApi.md#deleteRule) | **DELETE** /tenants/{tenantId}/validations/rules/{ruleId} | Deletes a Rule. |
| [**getRuleById()**](RulesApi.md#getRuleById) | **GET** /tenants/{tenantId}/validations/rules/{ruleId} | Retrieves a Rule by ID. |
| [**getRules()**](RulesApi.md#getRules) | **GET** /tenants/{tenantId}/validations/rules | Retrieves a list of Rules. |
| [**updateRule()**](RulesApi.md#updateRule) | **PUT** /tenants/{tenantId}/validations/rules/{ruleId} | Updates a Rule. |


## `createRule()`

```php
createRule($tenantId, $validationsApiRulesV1CreateRequest)
```

Creates a Rule.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$validationsApiRulesV1CreateRequest = new \EdGraph\PlatformClient\Model\ValidationsApiRulesV1CreateRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiRulesV1CreateRequest | 

try {
    $apiInstance->createRule($tenantId, $validationsApiRulesV1CreateRequest);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->createRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **validationsApiRulesV1CreateRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiRulesV1CreateRequest**](../Model/ValidationsApiRulesV1CreateRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteRule()`

```php
deleteRule($tenantId, $ruleId)
```

Deletes a Rule.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$ruleId = 'ruleId_example'; // string | 

try {
    $apiInstance->deleteRule($tenantId, $ruleId);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->deleteRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **ruleId** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getRuleById()`

```php
getRuleById($tenantId, $ruleId): \EdGraph\PlatformClient\Model\ValidationsApiRulesV1RuleDto
```

Retrieves a Rule by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$ruleId = 'ruleId_example'; // string | 

try {
    $result = $apiInstance->getRuleById($tenantId, $ruleId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->getRuleById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **ruleId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiRulesV1RuleDto**](../Model/ValidationsApiRulesV1RuleDto.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getRules()`

```php
getRules($tenantId, $pageIndex, $pageSize, $filter, $orderBy): \EdGraph\PlatformClient\Model\ValidationsApiRulesV1PaginatedRules
```

Retrieves a list of Rules.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$pageIndex = 0; // int | 
$pageSize = 10; // int | 
$filter = 'filter_example'; // string | 
$orderBy = 'orderBy_example'; // string | 

try {
    $result = $apiInstance->getRules($tenantId, $pageIndex, $pageSize, $filter, $orderBy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->getRules: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] [default to 0] |
| **pageSize** | **int**|  | [optional] [default to 10] |
| **filter** | **string**|  | [optional] |
| **orderBy** | **string**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\ValidationsApiRulesV1PaginatedRules**](../Model/ValidationsApiRulesV1PaginatedRules.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateRule()`

```php
updateRule($tenantId, $ruleId, $validationsApiRulesV1UpdateRequest)
```

Updates a Rule.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$ruleId = 'ruleId_example'; // string | 
$validationsApiRulesV1UpdateRequest = new \EdGraph\PlatformClient\Model\ValidationsApiRulesV1UpdateRequest(); // \EdGraph\PlatformClient\Model\ValidationsApiRulesV1UpdateRequest | 

try {
    $apiInstance->updateRule($tenantId, $ruleId, $validationsApiRulesV1UpdateRequest);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->updateRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **ruleId** | **string**|  | |
| **validationsApiRulesV1UpdateRequest** | [**\EdGraph\PlatformClient\Model\ValidationsApiRulesV1UpdateRequest**](../Model/ValidationsApiRulesV1UpdateRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
