

# CreatePost201ResponseAnyOfData


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**organizationId** | **String** |  |  |
|**profileId** | **String** |  |  [optional] |
|**createdBy** | **String** |  |  |
|**title** | **String** |  |  [optional] |
|**content** | **String** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**scheduledFor** | **OffsetDateTime** |  |  [optional] |
|**publishedAt** | **OffsetDateTime** |  |  [optional] |
|**timezone** | **String** |  |  [optional] |
|**mediaItems** | [**List&lt;ListPosts200ResponseAnyOfDataPostsInnerMediaItemsInner&gt;**](ListPosts200ResponseAnyOfDataPostsInnerMediaItemsInner.md) |  |  |
|**tags** | **List&lt;String&gt;** |  |  |
|**hashtags** | **List&lt;String&gt;** |  |  |
|**mentions** | **List&lt;String&gt;** |  |  |
|**metadata** | **Map&lt;String, Object&gt;** |  |  |
|**crosspostingEnabled** | **Boolean** |  |  |
|**queuedFromProfile** | **String** |  |  [optional] |
|**queueId** | **String** |  |  [optional] |
|**recycling** | **CreatePostRequestRecycling** |  |  [optional] |
|**targets** | [**List&lt;ListPosts200ResponseAnyOfDataPostsInnerTargetsInner&gt;**](ListPosts200ResponseAnyOfDataPostsInnerTargetsInner.md) |  |  |
|**createdAt** | **OffsetDateTime** |  |  |
|**updatedAt** | **OffsetDateTime** |  |  |



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



