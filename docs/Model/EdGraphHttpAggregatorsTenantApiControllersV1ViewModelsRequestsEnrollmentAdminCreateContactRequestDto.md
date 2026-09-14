# EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tenantId** | **string** | Must match the tenant in the route. | [optional]
**contactId** | **string** | The contact&#39;s identifier in the source system. Distinct from the record id, which the service  assigns and returns in the response. | [optional]
**firstName** | **string** | Required. Never overridable - only email and phone are. | [optional]
**lastName** | **string** | Required. Never overridable - only email and phone are. | [optional]
**email** | **string** | The SIS-sourced email. Correcting it later is an override and goes through the  &#x60;email-override&#x60; route instead - see EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.UpdateContactRequestDto. | [optional]
**phone** | **string** | The SIS-sourced phone, on the same terms as Email. | [optional]
**students** | [**\EdGraph\PlatformClient\Model\EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminContactStudentRequestDto[]**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminContactStudentRequestDto.md) | The students to link the contact to. Optional; omit or send an empty list for a contact with no  links yet. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
