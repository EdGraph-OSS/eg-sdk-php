# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**eventId** | **string** |  | [optional]
**detail** | **string** | Which detail this entry is about: &#x60;email&#x60; or &#x60;phone&#x60;. | [optional]
**action** | **string** | &#x60;set&#x60; or &#x60;removed&#x60;. A removal returns the detail to its SIS value. | [optional]
**previousValue** | **string** | The value this entry superseded, if any. Superseded values are kept, never deleted. | [optional]
**newValue** | **string** |  | [optional]
**sisValue** | **string** |  | [optional]
**overriddenBy** | **string** |  | [optional]
**overriddenAt** | **\DateTime** |  | [optional]
**actingStudentId** | **string** | The student whose screen the change was made from, when one was recorded. | [optional]
**studentIds** | **string[]** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
