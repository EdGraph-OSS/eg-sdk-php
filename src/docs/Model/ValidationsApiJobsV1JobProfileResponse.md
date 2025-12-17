# # ValidationsApiJobsV1JobProfileResponse

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
**dataRefreshType** | [**\EdGraph\PlatformClient\Model\ValidationsApiJobsV1DataRefreshType**](ValidationsApiJobsV1DataRefreshType.md) |  | [optional]
**dataRefreshSpecificDate** | **string** |  | [optional]
**maxApiFailure** | **int** |  | [optional]
**maxApiRetry** | **int** |  | [optional]
**jobCompleteCallbackUrl** | **string** |  | [optional]
**jobMetadata** | [**\EdGraph\PlatformClient\Model\ValidationsApiJobsV1JobMetadata[]**](ValidationsApiJobsV1JobMetadata.md) |  | [optional] [readonly]
**schedule** | [**\EdGraph\PlatformClient\Model\ValidationsApiJobsV1Schedule**](ValidationsApiJobsV1Schedule.md) |  | [optional]
**notificationEmails** | **string[]** |  | [optional] [readonly]
**jobStatus** | [**\EdGraph\PlatformClient\Model\ValidationsApiJobsV1JobStatus**](ValidationsApiJobsV1JobStatus.md) |  | [optional]
**jobExecutionId** | **string** |  | [optional]
**jobExecutionStatus** | [**\EdGraph\PlatformClient\Model\ValidationsApiJobsV1JobExecutionStatus**](ValidationsApiJobsV1JobExecutionStatus.md) |  | [optional]
**jobExecutionStartDateTime** | **string** |  | [optional]
**jobExecutionEndDateTime** | **string** |  | [optional]
**metrics** | [**\EdGraph\PlatformClient\Model\ValidationsApiJobsV1Metric[]**](ValidationsApiJobsV1Metric.md) |  | [optional] [readonly]
**childJobs** | [**\EdGraph\PlatformClient\Model\ValidationsApiJobsV1ChildJob[]**](ValidationsApiJobsV1ChildJob.md) |  | [optional] [readonly]
**createdBy** | **string** |  | [optional]
**createdDateTime** | **string** |  | [optional]
**lastModifiedBy** | **string** |  | [optional]
**lastModifiedDateTime** | **string** |  | [optional]
**collectionId** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
