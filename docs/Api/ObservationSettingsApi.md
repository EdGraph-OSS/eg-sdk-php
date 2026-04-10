# EdGraph\PlatformClient\ObservationSettingsApi

All URIs are relative to https://api.dev.edgraph.com/tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addAvailablePersona()**](ObservationSettingsApi.md#addAvailablePersona) | **POST** /tenants/{tenantId}/observations/settings/personas | Adds a persona for a given Tenant |
| [**getApplicationSettings()**](ObservationSettingsApi.md#getApplicationSettings) | **GET** /tenants/{tenantId}/observations/settings/application | Gets the application settings for the tenant |
| [**getPaginatedForms()**](ObservationSettingsApi.md#getPaginatedForms) | **GET** /tenants/{tenantId}/observations/forms | Get Paginated Forms |
| [**getPaginatedPersonas()**](ObservationSettingsApi.md#getPaginatedPersonas) | **GET** /tenants/{tenantId}/observations/settings/personas | Gets available personas |
| [**getPaginatedStaffClassifications()**](ObservationSettingsApi.md#getPaginatedStaffClassifications) | **GET** /tenants/{tenantId}/observations/settings/available-staffclassifications | Get Paginated Available StaffClassifications |
| [**getStaffClassificationsSettings()**](ObservationSettingsApi.md#getStaffClassificationsSettings) | **GET** /tenants/{tenantId}/observations/settings/staffclassifications | Gets the staffClassification settings for the tenant |
| [**setApplicationSettings()**](ObservationSettingsApi.md#setApplicationSettings) | **POST** /tenants/{tenantId}/observations/settings/application | Sets the Application Settings of an Observation for a given Tenant |
| [**setRolePersonasSettings()**](ObservationSettingsApi.md#setRolePersonasSettings) | **POST** /tenants/{tenantId}/observations/settings/rolepersonas | Updates personas assigned to a role configuration of the tenants setting |
| [**verifySysAdminCredentials()**](ObservationSettingsApi.md#verifySysAdminCredentials) | **GET** /tenants/{tenantId}/observations/settings/verify-credentials | Gets the staffClassification settings for the tenant |


## `addAvailablePersona()`

```php
addAvailablePersona($tenantId, $edGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse
```

Adds a persona for a given Tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest | 

try {
    $result = $apiInstance->addAvailablePersona($tenantId, $edGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationSettingsApi->addAvailablePersona: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getApplicationSettings()`

```php
getApplicationSettings($tenantId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse
```

Gets the application settings for the tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->getApplicationSettings($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationSettingsApi->getApplicationSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPaginatedForms()`

```php
getPaginatedForms($tenantId, $pageSize, $pageIndex, $orderBy, $filter): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse
```

Get Paginated Forms

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationSettingsApi(
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
    $result = $apiInstance->getPaginatedForms($tenantId, $pageSize, $pageIndex, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationSettingsApi->getPaginatedForms: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPaginatedPersonas()`

```php
getPaginatedPersonas($tenantId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse
```

Gets available personas

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->getPaginatedPersonas($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationSettingsApi->getPaginatedPersonas: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPaginatedStaffClassifications()`

```php
getPaginatedStaffClassifications($tenantId, $pageIndex, $pageSize, $orderBy, $filter): \EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1GetStaffClassificationsResponse
```

Get Paginated Available StaffClassifications

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationSettingsApi(
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
    $result = $apiInstance->getPaginatedStaffClassifications($tenantId, $pageIndex, $pageSize, $orderBy, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationSettingsApi->getPaginatedStaffClassifications: ', $e->getMessage(), PHP_EOL;
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

[**\EdGraph\PlatformClient\Model\IdentityApiStaffClassificationV1GetStaffClassificationsResponse**](../Model/IdentityApiStaffClassificationV1GetStaffClassificationsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStaffClassificationsSettings()`

```php
getStaffClassificationsSettings($tenantId): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse
```

Gets the staffClassification settings for the tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->getStaffClassificationsSettings($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationSettingsApi->getStaffClassificationsSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setApplicationSettings()`

```php
setApplicationSettings($tenantId, $edGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse
```

Sets the Application Settings of an Observation for a given Tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest | 

try {
    $result = $apiInstance->setApplicationSettings($tenantId, $edGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationSettingsApi->setApplicationSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setRolePersonasSettings()`

```php
setRolePersonasSettings($tenantId, $edGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest): \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse
```

Updates personas assigned to a role configuration of the tenants setting

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 
$edGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest = new \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest(); // \EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest | 

try {
    $result = $apiInstance->setRolePersonasSettings($tenantId, $edGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationSettingsApi->setRolePersonasSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |
| **edGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest.md)|  | [optional] |

### Return type

[**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse**](../Model/EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `verifySysAdminCredentials()`

```php
verifySysAdminCredentials($tenantId): object
```

Gets the staffClassification settings for the tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = EdGraph\PlatformClient\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EdGraph\PlatformClient\Api\ObservationSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenantId = 'tenantId_example'; // string | 

try {
    $result = $apiInstance->verifySysAdminCredentials($tenantId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObservationSettingsApi->verifySysAdminCredentials: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenantId** | **string**|  | |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
