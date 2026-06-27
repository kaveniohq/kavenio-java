

# ListPosts200ResponseAnyOfDataPostsInnerTargetsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**postId** | **String** |  |  |
|**platform** | [**PlatformEnum**](#PlatformEnum) |  |  |
|**accountId** | **String** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**customContent** | **String** |  |  [optional] |
|**customMedia** | [**List&lt;ListPosts200ResponseAnyOfDataPostsInnerMediaItemsInner&gt;**](ListPosts200ResponseAnyOfDataPostsInnerMediaItemsInner.md) |  |  [optional] |
|**scheduledFor** | **OffsetDateTime** |  |  [optional] |
|**platformSpecificData** | [**ListPosts200ResponseAnyOfDataPostsInnerTargetsInnerPlatformSpecificData**](ListPosts200ResponseAnyOfDataPostsInnerTargetsInnerPlatformSpecificData.md) |  |  [optional] |
|**platformPostId** | **String** |  |  [optional] |
|**nativeUrl** | **URI** |  |  [optional] |
|**error** | **String** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  |
|**updatedAt** | **OffsetDateTime** |  |  |



## Enum: PlatformEnum

| Name | Value |
|---- | -----|
| TWITTER | &quot;twitter&quot; |
| PINTEREST | &quot;pinterest&quot; |
| LINKEDIN | &quot;linkedin&quot; |
| BLUESKY | &quot;bluesky&quot; |
| MASTODON | &quot;mastodon&quot; |
| REDDIT | &quot;reddit&quot; |
| TELEGRAM | &quot;telegram&quot; |
| YOUTUBE | &quot;youtube&quot; |
| FACEBOOK | &quot;facebook&quot; |
| INSTAGRAM | &quot;instagram&quot; |
| THREADS | &quot;threads&quot; |
| TIKTOK | &quot;tiktok&quot; |
| GOOGLEBUSINESS | &quot;googlebusiness&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| DRAFT | &quot;draft&quot; |
| SCHEDULED | &quot;scheduled&quot; |
| PUBLISHING | &quot;publishing&quot; |
| PUBLISHED | &quot;published&quot; |
| UNPUBLISHED | &quot;unpublished&quot; |
| FAILED | &quot;failed&quot; |
| PARTIAL | &quot;partial&quot; |
| CANCELLED | &quot;cancelled&quot; |



