

# ListPosts200ResponseAnyOfDataPostsInnerTargetsInnerPlatformSpecificDataAnyOf7


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**pageId** | **String** |  |  [optional] |
|**contentType** | [**ContentTypeEnum**](#ContentTypeEnum) |  |  [optional] |
|**firstComment** | **String** |  |  [optional] |
|**title** | **String** |  |  [optional] |
|**reelTitle** | **String** |  |  [optional] |
|**link** | **URI** |  |  [optional] |
|**carouselLink** | **URI** |  |  [optional] |
|**carouselCards** | [**List&lt;ListPosts200ResponseAnyOfDataPostsInnerTargetsInnerPlatformSpecificDataAnyOf7CarouselCardsInner&gt;**](ListPosts200ResponseAnyOfDataPostsInnerTargetsInnerPlatformSpecificDataAnyOf7CarouselCardsInner.md) |  |  [optional] |
|**unpublishedContentType** | [**UnpublishedContentTypeEnum**](#UnpublishedContentTypeEnum) |  |  [optional] |
|**draft** | **Boolean** |  |  [optional] |
|**scheduledPublishTime** | **OffsetDateTime** |  |  [optional] |
|**geoRestriction** | [**ListPosts200ResponseAnyOfDataPostsInnerTargetsInnerPlatformSpecificDataAnyOf7GeoRestriction**](ListPosts200ResponseAnyOfDataPostsInnerTargetsInnerPlatformSpecificDataAnyOf7GeoRestriction.md) |  |  [optional] |
|**geoRestrictions** | [**ListPosts200ResponseAnyOfDataPostsInnerTargetsInnerPlatformSpecificDataAnyOf7GeoRestriction**](ListPosts200ResponseAnyOfDataPostsInnerTargetsInnerPlatformSpecificDataAnyOf7GeoRestriction.md) |  |  [optional] |
|**multiPageTargets** | **List&lt;String&gt;** |  |  [optional] |



## Enum: ContentTypeEnum

| Name | Value |
|---- | -----|
| FEED | &quot;feed&quot; |
| STORY | &quot;story&quot; |
| REEL | &quot;reel&quot; |
| VIDEO | &quot;video&quot; |



## Enum: UnpublishedContentTypeEnum

| Name | Value |
|---- | -----|
| DRAFT | &quot;draft&quot; |
| SCHEDULED | &quot;scheduled&quot; |



