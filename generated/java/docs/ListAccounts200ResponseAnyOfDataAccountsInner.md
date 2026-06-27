

# ListAccounts200ResponseAnyOfDataAccountsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**organizationId** | **String** |  |  |
|**profileId** | **String** |  |  |
|**platform** | [**PlatformEnum**](#PlatformEnum) |  |  |
|**providerAccountId** | **String** |  |  |
|**username** | **String** |  |  [optional] |
|**displayName** | **String** |  |  [optional] |
|**profilePicture** | **URI** |  |  [optional] |
|**profileUrl** | **URI** |  |  [optional] |
|**parentAccountId** | **String** |  |  [optional] |
|**enabled** | **Boolean** |  |  |
|**isActive** | **Boolean** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**tokenExpiresAt** | **String** |  |  [optional] |
|**scopes** | **List&lt;String&gt;** |  |  |
|**permissions** | **List&lt;String&gt;** |  |  |
|**metadata** | **Map&lt;String, Object&gt;** |  |  |
|**readiness** | [**ListFacebookPages200ResponseAnyOfDataReadiness**](ListFacebookPages200ResponseAnyOfDataReadiness.md) |  |  [optional] |
|**adAccountsCacheExpiresAt** | **String** |  |  [optional] |
|**lastError** | **String** |  |  [optional] |
|**lastHealthCheckedAt** | **String** |  |  [optional] |
|**createdBy** | **String** |  |  |
|**createdAt** | **String** |  |  |
|**updatedAt** | **String** |  |  |



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
| CONNECTED | &quot;connected&quot; |
| DISCONNECTED | &quot;disconnected&quot; |
| NEEDS_RECONNECT | &quot;needs_reconnect&quot; |
| REVOKED | &quot;revoked&quot; |



