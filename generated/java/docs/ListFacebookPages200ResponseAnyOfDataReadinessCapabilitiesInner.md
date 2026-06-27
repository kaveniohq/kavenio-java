

# ListFacebookPages200ResponseAnyOfDataReadinessCapabilitiesInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**key** | [**KeyEnum**](#KeyEnum) |  |  |
|**supported** | **Boolean** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**reason** | **String** |  |  [optional] |
|**requiredScopes** | **List&lt;String&gt;** |  |  [optional] |
|**requiredPermissions** | **List&lt;String&gt;** |  |  [optional] |



## Enum: KeyEnum

| Name | Value |
|---- | -----|
| PUBLISH | &quot;publish&quot; |
| SCHEDULE | &quot;schedule&quot; |
| MEDIA_UPLOAD | &quot;media_upload&quot; |
| VIDEO_UPLOAD | &quot;video_upload&quot; |
| PHOTO_UPLOAD | &quot;photo_upload&quot; |
| FIRST_COMMENT | &quot;first_comment&quot; |
| PLAYLIST | &quot;playlist&quot; |
| PAGE_SELECTION | &quot;page_selection&quot; |
| ACCOUNT_SELECTION | &quot;account_selection&quot; |
| CREATOR_INFO | &quot;creator_info&quot; |
| LOCATION_SELECTION | &quot;location_selection&quot; |
| LOCATION_MANAGEMENT | &quot;location_management&quot; |
| REVIEWS | &quot;reviews&quot; |
| ANALYTICS | &quot;analytics&quot; |
| VERIFICATION | &quot;verification&quot; |
| PLACE_ACTIONS | &quot;place_actions&quot; |
| LIFECYCLE_EDIT | &quot;lifecycle_edit&quot; |
| LIFECYCLE_UNPUBLISH | &quot;lifecycle_unpublish&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| READY | &quot;ready&quot; |
| NEEDS_SETUP | &quot;needs_setup&quot; |
| NEEDS_RECONNECT | &quot;needs_reconnect&quot; |
| BLOCKED | &quot;blocked&quot; |
| UNSUPPORTED | &quot;unsupported&quot; |
| UNKNOWN | &quot;unknown&quot; |



