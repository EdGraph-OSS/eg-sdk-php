# IdentityApiUserV2UserProfileResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userId** | **string** |  | [optional]
**userName** | **string** |  | [optional]
**email** | **string** |  | [optional]
**firstName** | **string** |  | [optional]
**lastName** | **string** |  | [optional]
**phoneNumber** | **string** |  | [optional]
**lockoutEnabled** | **bool** |  | [optional]
**tenantCount** | **int** |  | [optional]
**createdDateTime** | **string** |  | [optional]
**lastModifiedDateTime** | **string** |  | [optional]
**extensions** | [**\EdGraph\PlatformClient\Model\IdentityApiUserV2UserExtension[]**](IdentityApiUserV2UserExtension.md) |  | [optional] [readonly]
**logins** | [**\EdGraph\PlatformClient\Model\IdentityApiUserV2UserLogin[]**](IdentityApiUserV2UserLogin.md) |  | [optional] [readonly]
**source** | **string** |  | [optional]
**lastLoginDateTime** | **string** |  | [optional]
**mfaCompleted** | **bool** |  | [optional]
**platformRole** | **string** |  | [optional]
**tenantStatus** | **string** |  | [optional]
**tenantAdmin** | **bool** |  | [optional]
**status** | **string** | The user&#39;s status across all their tenants: Active if any membership is active, Inactive if every  membership is inactive, Unknown if they have no memberships. Unlike tenantStatus this does not  depend on a tenantId being supplied on the request. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
