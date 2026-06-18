# EdfiAdminApiEdfiAdminV1InstanceListModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Details | [optional]
**instanceName** | **string** |  | [optional]
**useCustomId** | **bool** |  | [optional]
**customId** | **string** |  | [optional]
**description** | **string** |  | [optional]
**connectionName** | **string** |  | [optional]
**selectedConnectionId** | **string** | Connection | [optional]
**selectedConnection** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1EdFiConnectionListModel**](EdfiAdminApiEdfiAdminV1EdFiConnectionListModel.md) |  | [optional]
**databases** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceDatabases**](EdfiAdminApiEdfiAdminV1InstanceDatabases.md) |  | [optional]
**tenantId** | **string** | Metadata | [optional]
**createdBy** | **string** |  | [optional]
**createdDateTime** | **string** |  | [optional]
**isDeleted** | **bool** |  | [optional]
**lastModifiedBy** | **string** |  | [optional]
**lastModifiedDateTime** | **string** |  | [optional]
**apiAuthUrl** | **string** | URLs | [optional]
**apiResourcesUrls** | **string[]** |  | [optional] [readonly]
**apiCompositesUrls** | **string[]** |  | [optional] [readonly]
**selectedConnectionType** | **string** | Connection | [optional]
**isDefault** | **bool** | IsDefault | [optional]
**provider** | **string** | Provider | [optional]
**onboarding** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1Onboarding**](EdfiAdminApiEdfiAdminV1Onboarding.md) |  | [optional]
**applications** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponse[]**](EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponse.md) | Applications | [optional] [readonly]
**relatedInstances** | [**\EdGraph\PlatformClient\Model\EdfiAdminApiEdfiAdminV1RelatedInstance[]**](EdfiAdminApiEdfiAdminV1RelatedInstance.md) |  | [optional] [readonly]
**enableAdminApi** | **bool** | Enable Admin API | [optional]
**state** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
