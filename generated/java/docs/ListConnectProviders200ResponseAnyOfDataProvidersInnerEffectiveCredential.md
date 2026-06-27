

# ListConnectProviders200ResponseAnyOfDataProvidersInnerEffectiveCredential


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**source** | [**SourceEnum**](#SourceEnum) |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**credentialId** | **String** |  |  [optional] |
|**credentialFamily** | [**CredentialFamilyEnum**](#CredentialFamilyEnum) |  |  [optional] |
|**credentialVersion** | **Integer** |  |  [optional] |
|**lastTestedAt** | **String** |  |  [optional] |
|**message** | **String** |  |  [optional] |



## Enum: SourceEnum

| Name | Value |
|---- | -----|
| SYSTEM | &quot;system&quot; |
| ORGANIZATION | &quot;organization&quot; |
| NONE | &quot;none&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| MISSING | &quot;missing&quot; |
| NOT_REQUIRED | &quot;not_required&quot; |
| UNTESTED | &quot;untested&quot; |
| VERIFIED | &quot;verified&quot; |
| INVALID | &quot;invalid&quot; |
| DISABLED | &quot;disabled&quot; |
| NEEDS_OAUTH_TEST | &quot;needs_oauth_test&quot; |
| TEST_FAILED | &quot;test_failed&quot; |



## Enum: CredentialFamilyEnum

| Name | Value |
|---- | -----|
| X | &quot;x&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| PINTEREST | &quot;pinterest&quot; |
| REDDIT | &quot;reddit&quot; |
| META | &quot;meta&quot; |
| THREADS | &quot;threads&quot; |
| TIKTOK | &quot;tiktok&quot; |
| GOOGLE_ADS | &quot;google_ads&quot; |
| GOOGLE_BUSINESS | &quot;google_business&quot; |
| YOUTUBE | &quot;youtube&quot; |
| X_ADS | &quot;x_ads&quot; |
| BLUESKY | &quot;bluesky&quot; |
| MASTODON | &quot;mastodon&quot; |
| TELEGRAM | &quot;telegram&quot; |



