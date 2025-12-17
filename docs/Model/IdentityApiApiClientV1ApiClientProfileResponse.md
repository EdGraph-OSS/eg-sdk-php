# # IdentityApiApiClientV1ApiClientProfileResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tenantId** | **string** |  | [optional]
**clientId** | **string** |  | [optional]
**clientName** | **string** |  | [optional]
**description** | **string** |  | [optional]
**clientUri** | **string** |  | [optional]
**logoUri** | **string** |  | [optional]
**enabled** | **bool** |  | [optional]
**accessTokenType** | [**\EdGraph\PlatformClient\Model\IdentityApiApiClientV1AccessTokenType**](IdentityApiApiClientV1AccessTokenType.md) |  | [optional]
**tokenUsage** | [**\EdGraph\PlatformClient\Model\IdentityApiApiClientV1TokenUsage**](IdentityApiApiClientV1TokenUsage.md) |  | [optional]
**refreshTokenExpiration** | [**\EdGraph\PlatformClient\Model\IdentityApiApiClientV1TokenExpiration**](IdentityApiApiClientV1TokenExpiration.md) |  | [optional]
**enableLocalLogin** | **bool** |  | [optional]
**allowOfflineAccess** | **bool** |  | [optional]
**allowAccessTokensViaBrowser** | **bool** |  | [optional]
**updateAccessTokenClaimsOnRefresh** | **bool** |  | [optional]
**alwaysIncludeUserClaimsInIdToken** | **bool** |  | [optional]
**identityTokenLifetime** | **int** |  | [optional]
**accessTokenLifetime** | **int** |  | [optional]
**authorizationCodeLifetime** | **int** |  | [optional]
**absoluteRefreshTokenLifetime** | **int** |  | [optional]
**slidingRefreshTokenLifetime** | **int** |  | [optional]
**requireClientSecret** | **bool** |  | [optional]
**requireConsent** | **bool** |  | [optional]
**allowedScopes** | **string[]** |  | [optional] [readonly]
**allowedCorsOrigins** | **string[]** |  | [optional] [readonly]
**allowedGrantTypes** | **string[]** |  | [optional] [readonly]
**identityProviderRestrictions** | **string[]** |  | [optional] [readonly]
**redirectUris** | **string[]** |  | [optional] [readonly]
**postLogoutRedirectUris** | **string[]** |  | [optional] [readonly]
**claims** | [**\EdGraph\PlatformClient\Model\IdentityApiApiClientV1Claim[]**](IdentityApiApiClientV1Claim.md) |  | [optional] [readonly]
**requirePkce** | **bool** |  | [optional]
**createdBy** | **string** |  | [optional]
**createdDateTime** | **string** |  | [optional]
**lastModifiedBy** | **string** |  | [optional]
**lastModifiedDateTime** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
