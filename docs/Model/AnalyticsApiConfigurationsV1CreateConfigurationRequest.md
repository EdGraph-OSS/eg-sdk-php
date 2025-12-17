# # AnalyticsApiConfigurationsV1CreateConfigurationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional]
**tenantId** | **string** |  | [optional]
**sqlConnectionString** | **string** |  | [optional]
**status** | **string** |  | [optional]
**useEdGraphPowerBi** | **bool** |  | [optional]
**isGlobalConfiguration** | **bool** |  | [optional]
**isDefaultTenantConfiguration** | **bool** |  | [optional]
**azureAd** | [**\EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsAzureAd**](AnalyticsApiConfigurationsV1AnalyticsAzureAd.md) |  | [optional]
**powerBi** | [**\EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsPowerBi**](AnalyticsApiConfigurationsV1AnalyticsPowerBi.md) |  | [optional]
**selectedEdFiConnectionId** | **string** |  | [optional]
**triggerOptions** | [**\EdGraph\PlatformClient\Model\AnalyticsApiConfigurationsV1AnalyticsTriggerOption[]**](AnalyticsApiConfigurationsV1AnalyticsTriggerOption.md) |  | [optional] [readonly]
**schoolYears** | **string[]** |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
