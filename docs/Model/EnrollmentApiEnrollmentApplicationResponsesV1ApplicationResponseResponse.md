# EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional]
**tenantId** | **string** |  | [optional]
**applicationPathway** | [**\EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentApplicationResponsesV1ApplicationPathwayMessage**](EnrollmentApiEnrollmentApplicationResponsesV1ApplicationPathwayMessage.md) |  | [optional]
**currentScreenCode** | **string** |  | [optional]
**progress** | **string** | Decimal progress (0-100, 2dp) carried as an invariant-culture string,  mirroring the legacy enrollmentresults.proto completedProgress convention. | [optional]
**studentId** | **string** |  | [optional]
**languageCode** | **string** |  | [optional]
**contacts** | [**\EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseContactMessage[]**](EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseContactMessage.md) |  | [optional] [readonly]
**screens** | [**\EdGraph\PlatformClient\Model\EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseScreenMessage[]**](EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseScreenMessage.md) |  | [optional] [readonly]
**createdBy** | **string** |  | [optional]
**createdDateTime** | **string** |  | [optional]
**lastModifiedBy** | **string** |  | [optional]
**lastModifiedDateTime** | **string** |  | [optional]
**deletedBy** | **string** |  | [optional]
**deletedDateTime** | **string** |  | [optional]
**isDeleted** | **bool** |  | [optional]
**status** | **string** |  | [optional]
**studentFirstName** | **string** |  | [optional]
**studentLastName** | **string** |  | [optional]
**studentLocalId** | **string** |  | [optional]
**nextSchoolCode** | **string** |  | [optional]
**nextSchoolName** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
