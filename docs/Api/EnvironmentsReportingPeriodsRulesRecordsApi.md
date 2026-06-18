# EdGraph\PlatformClient\EnvironmentsReportingPeriodsRulesRecordsApi



All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteStateReportingPeriodRules()**](EnvironmentsReportingPeriodsRulesRecordsApi.md#deleteStateReportingPeriodRules) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules | Deletes the Rules of a Reporting Period. |
| [**searchStateReportingPeriodRecords()**](EnvironmentsReportingPeriodsRulesRecordsApi.md#searchStateReportingPeriodRecords) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/records | Retrieves the Invalid Records of all the Rules within a Reporting Period. |
| [**searchStateReportingPeriodRuleRecords()**](EnvironmentsReportingPeriodsRulesRecordsApi.md#searchStateReportingPeriodRuleRecords) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records | Retrieves the Invalid Records of a Rule. |
| [**setStateReportingPeriodRuleRecordPostFlag()**](EnvironmentsReportingPeriodsRulesRecordsApi.md#setStateReportingPeriodRuleRecordPostFlag) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records/{recordId}/excludefrompost | Toggles the \&quot;ExcludeFromPost\&quot; flag of a Rule&#39;s Invalid Record. |
| [**setStateReportingPeriodRuleRecordPostFlagBulk()**](EnvironmentsReportingPeriodsRulesRecordsApi.md#setStateReportingPeriodRuleRecordPostFlagBulk) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records/excludefrompost | Toggles the \&quot;ExcludeFromPost\&quot; flag of a Rule&#39;s Invalid Records in bulk. |


## `deleteStateReportingPeriodRules()`

```php
deleteStateReportingPeriodRules($tenantId, $environmentId, $reportingPeriodId): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodRulesDeletedResponse
```

Deletes the Rules of a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsRulesRecordsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 

try {
    $result = $apiInstance->deleteStateReportingPeriodRules($tenantId, $environmentId, $reportingPeriodId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi->deleteStateReportingPeriodRules: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodRulesDeletedResponse**](../Model/EdGraphServicesStateReportingV1ReportingPeriodRulesDeletedResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchStateReportingPeriodRecords()`

```php
searchStateReportingPeriodRecords($tenantId, $environmentId, $reportingPeriodId, $pageIndex, $pageSize, $excludeFromPost): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedRecords
```

Retrieves the Invalid Records of all the Rules within a Reporting Period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsRulesRecordsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$pageIndex = 56; // int | 
$pageSize = 56; // int | 
$excludeFromPost = True; // bool | 

try {
    $result = $apiInstance->searchStateReportingPeriodRecords($tenantId, $environmentId, $reportingPeriodId, $pageIndex, $pageSize, $excludeFromPost);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi->searchStateReportingPeriodRecords: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] |
| **pageSize** | **int**|  | [optional] |
| **excludeFromPost** | **bool**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedRecords**](../Model/EdGraphServicesStateReportingV1PaginatedRecords.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchStateReportingPeriodRuleRecords()`

```php
searchStateReportingPeriodRuleRecords($tenantId, $environmentId, $reportingPeriodId, $ruleId, $pageIndex, $pageSize): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedRuleRecords
```

Retrieves the Invalid Records of a Rule.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsRulesRecordsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$ruleId = 'ruleId_example'; // string | 
$pageIndex = 56; // int | 
$pageSize = 56; // int | 

try {
    $result = $apiInstance->searchStateReportingPeriodRuleRecords($tenantId, $environmentId, $reportingPeriodId, $ruleId, $pageIndex, $pageSize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi->searchStateReportingPeriodRuleRecords: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **ruleId** | **string**|  | |
| **pageIndex** | **int**|  | [optional] |
| **pageSize** | **int**|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1PaginatedRuleRecords**](../Model/EdGraphServicesStateReportingV1PaginatedRuleRecords.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setStateReportingPeriodRuleRecordPostFlag()`

```php
setStateReportingPeriodRuleRecordPostFlag($tenantId, $environmentId, $reportingPeriodId, $ruleId, $recordId, $edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse
```

Toggles the \"ExcludeFromPost\" flag of a Rule's Invalid Record.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsRulesRecordsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$ruleId = 'ruleId_example'; // string | 
$recordId = 'recordId_example'; // string | 
$edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest | 

try {
    $result = $apiInstance->setStateReportingPeriodRuleRecordPostFlag($tenantId, $environmentId, $reportingPeriodId, $ruleId, $recordId, $edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi->setStateReportingPeriodRuleRecordPostFlag: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **ruleId** | **string**|  | |
| **recordId** | **string**|  | |
| **edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest**](../Model/EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest.md)|  | [optional] |

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

## `setStateReportingPeriodRuleRecordPostFlagBulk()`

```php
setStateReportingPeriodRuleRecordPostFlagBulk($tenantId, $environmentId, $reportingPeriodId, $ruleId, $edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest): \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse
```

Toggles the \"ExcludeFromPost\" flag of a Rule's Invalid Records in bulk.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\EnvironmentsReportingPeriodsRulesRecordsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$environmentId = 'environmentId_example'; // string | 
$reportingPeriodId = 'reportingPeriodId_example'; // string | 
$ruleId = 'ruleId_example'; // string | 
$edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest = new \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest(); // \EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest | 

try {
    $result = $apiInstance->setStateReportingPeriodRuleRecordPostFlagBulk($tenantId, $environmentId, $reportingPeriodId, $ruleId, $edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi->setStateReportingPeriodRuleRecordPostFlagBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **environmentId** | **string**|  | |
| **reportingPeriodId** | **string**|  | |
| **ruleId** | **string**|  | |
| **edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest** | [**\EdGraph\PlatformClient\Model\EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest**](../Model/EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest.md)|  | [optional] |

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
