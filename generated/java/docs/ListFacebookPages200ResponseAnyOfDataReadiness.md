

# ListFacebookPages200ResponseAnyOfDataReadiness


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**platform** | [**PlatformEnum**](#PlatformEnum) |  |  |
|**ready** | **Boolean** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**checkedAt** | **String** |  |  [optional] |
|**reconnectRecommended** | **Boolean** |  |  [optional] |
|**selectedDestinationId** | **String** |  |  [optional] |
|**selectedDestinationName** | **String** |  |  [optional] |
|**missingScopes** | **List&lt;String&gt;** |  |  [optional] |
|**missingPermissions** | **List&lt;String&gt;** |  |  [optional] |
|**missingDestinations** | **List&lt;String&gt;** |  |  [optional] |
|**issues** | [**List&lt;ListFacebookPages200ResponseAnyOfDataReadinessIssuesInner&gt;**](ListFacebookPages200ResponseAnyOfDataReadinessIssuesInner.md) |  |  [optional] |
|**capabilities** | [**List&lt;ListFacebookPages200ResponseAnyOfDataReadinessCapabilitiesInner&gt;**](ListFacebookPages200ResponseAnyOfDataReadinessCapabilitiesInner.md) |  |  [optional] |



## Enum: PlatformEnum

| Name | Value |
|---- | -----|
| TWITTER | &quot;twitter&quot; |
| FACEBOOK | &quot;facebook&quot; |
| INSTAGRAM | &quot;instagram&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| TIKTOK | &quot;tiktok&quot; |
| YOUTUBE | &quot;youtube&quot; |
| THREADS | &quot;threads&quot; |
| REDDIT | &quot;reddit&quot; |
| PINTEREST | &quot;pinterest&quot; |
| BLUESKY | &quot;bluesky&quot; |
| MASTODON | &quot;mastodon&quot; |
| GOOGLEBUSINESS | &quot;googlebusiness&quot; |
| TELEGRAM | &quot;telegram&quot; |
| SNAPCHAT | &quot;snapchat&quot; |
| DISCORD | &quot;discord&quot; |
| WHATSAPP | &quot;whatsapp&quot; |
| METAADS | &quot;metaads&quot; |
| GOOGLEADS | &quot;googleads&quot; |
| TIKTOKADS | &quot;tiktokads&quot; |
| LINKEDINADS | &quot;linkedinads&quot; |
| PINTERESTADS | &quot;pinterestads&quot; |
| XADS | &quot;xads&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| READY | &quot;ready&quot; |
| NEEDS_SETUP | &quot;needs_setup&quot; |
| NEEDS_RECONNECT | &quot;needs_reconnect&quot; |
| BLOCKED | &quot;blocked&quot; |
| UNSUPPORTED | &quot;unsupported&quot; |
| UNKNOWN | &quot;unknown&quot; |



