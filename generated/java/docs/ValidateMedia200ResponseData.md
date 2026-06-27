

# ValidateMedia200ResponseData


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**valid** | **Boolean** |  |  |
|**url** | **URI** |  |  |
|**error** | **String** |  |  [optional] |
|**contentType** | **String** |  |  [optional] |
|**size** | **Integer** |  |  [optional] |
|**sizeFormatted** | **String** |  |  [optional] |
|**type** | [**TypeEnum**](#TypeEnum) |  |  |
|**platformLimits** | [**Map&lt;String, ValidateMedia200ResponseDataPlatformLimitsValue&gt;**](ValidateMedia200ResponseDataPlatformLimitsValue.md) |  |  [optional] |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| IMAGE | &quot;image&quot; |
| VIDEO | &quot;video&quot; |
| DOCUMENT | &quot;document&quot; |
| UNKNOWN | &quot;unknown&quot; |



