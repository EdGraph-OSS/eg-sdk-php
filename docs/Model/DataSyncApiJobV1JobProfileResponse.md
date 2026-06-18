# DataSyncApiJobV1JobProfileResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tenantId** | **string** |  | [optional]
**jobId** | **string** |  | [optional]
**name** | **string** |  | [optional]
**jobTypeId** | **string** |  | [optional]
**jobTypeName** | **string** |  | [optional]
**sourceConnectionId** | **string** |  | [optional]
**destinationConnectionId** | **string** |  | [optional]
**profileId** | **string** |  | [optional]
**profileName** | **string** |  | [optional]
**applicationId** | **string** |  | [optional]
**jobPoints** | **int** |  | [optional]
**dataRefreshType** | [**\EdGraph\PlatformClient\Model\DataSyncApiJobV1DataRefreshType**](DataSyncApiJobV1DataRefreshType.md) |  | [optional]
**dataRefreshSpecificDate** | **string** |  | [optional]
**maxApiFailure** | **int** |  | [optional]
**maxApiRetry** | **int** |  | [optional]
**jobCompleteCallbackUrl** | **string** |  | [optional]
**jobMetadata** | [**\EdGraph\PlatformClient\Model\DataSyncApiJobV1JobMetadata[]**](DataSyncApiJobV1JobMetadata.md) |  | [optional] [readonly]
**schedule** | [**\EdGraph\PlatformClient\Model\DataSyncApiJobV1Schedule**](DataSyncApiJobV1Schedule.md) |  | [optional]
**notificationEmails** | **string[]** |  | [optional] [readonly]
**jobStatus** | [**\EdGraph\PlatformClient\Model\DataSyncApiJobV1JobStatus**](DataSyncApiJobV1JobStatus.md) |  | [optional]
**jobExecutionId** | **string** |  | [optional]
**jobExecutionStatus** | [**\EdGraph\PlatformClient\Model\DataSyncApiJobV1JobExecutionStatus**](DataSyncApiJobV1JobExecutionStatus.md) |  | [optional]
**jobExecutionStartDateTime** | **string** |  | [optional]
**jobExecutionEndDateTime** | **string** |  | [optional]
**metrics** | [**\EdGraph\PlatformClient\Model\DataSyncApiJobV1Metric[]**](DataSyncApiJobV1Metric.md) |  | [optional] [readonly]
**childJobs** | [**\EdGraph\PlatformClient\Model\DataSyncApiJobV1ChildJob[]**](DataSyncApiJobV1ChildJob.md) |  | [optional] [readonly]
**createdBy** | **string** |  | [optional]
**createdDateTime** | **string** |  | [optional]
**lastModifiedBy** | **string** |  | [optional]
**lastModifiedDateTime** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
