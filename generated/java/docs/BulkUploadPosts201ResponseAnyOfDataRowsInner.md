

# BulkUploadPosts201ResponseAnyOfDataRowsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**rowNumber** | **Integer** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**post** | [**CreatePost201ResponseAnyOfData**](CreatePost201ResponseAnyOfData.md) |  |  [optional] |
|**error** | [**ListProfiles401ResponseError**](ListProfiles401ResponseError.md) |  |  [optional] |
|**warnings** | [**List&lt;BulkUploadPosts201ResponseAnyOfDataRowsInnerWarningsInner&gt;**](BulkUploadPosts201ResponseAnyOfDataRowsInnerWarningsInner.md) |  |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| CREATED | &quot;created&quot; |
| FAILED | &quot;failed&quot; |



