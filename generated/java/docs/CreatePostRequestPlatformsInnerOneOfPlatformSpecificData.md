

# CreatePostRequestPlatformsInnerOneOfPlatformSpecificData


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**replyToTweetId** | **String** |  |  [optional] |
|**quoteTweetId** | **String** |  |  [optional] |
|**mediaIds** | **List&lt;String&gt;** |  |  [optional] |
|**replySettings** | [**ReplySettingsEnum**](#ReplySettingsEnum) |  |  [optional] |
|**threadItems** | [**List&lt;CreatePostRequestPlatformsInnerOneOfPlatformSpecificDataThreadItemsInner&gt;**](CreatePostRequestPlatformsInnerOneOfPlatformSpecificDataThreadItemsInner.md) |  |  [optional] |
|**poll** | [**CreatePostRequestPlatformsInnerOneOfPlatformSpecificDataPoll**](CreatePostRequestPlatformsInnerOneOfPlatformSpecificDataPoll.md) |  |  [optional] |
|**longVideo** | **Boolean** |  |  [optional] |
|**paidPartnership** | **Boolean** |  |  [optional] |
|**madeWithAi** | **Boolean** |  |  [optional] |
|**firstComment** | **String** |  |  [optional] |
|**sensitiveMedia** | [**ListPosts200ResponseAnyOfDataPostsInnerTargetsInnerPlatformSpecificDataAnyOfSensitiveMedia**](ListPosts200ResponseAnyOfDataPostsInnerTargetsInnerPlatformSpecificDataAnyOfSensitiveMedia.md) |  |  [optional] |



## Enum: ReplySettingsEnum

| Name | Value |
|---- | -----|
| FOLLOWING | &quot;following&quot; |
| MENTIONED_USERS | &quot;mentionedUsers&quot; |
| SUBSCRIBERS | &quot;subscribers&quot; |
| VERIFIED | &quot;verified&quot; |



