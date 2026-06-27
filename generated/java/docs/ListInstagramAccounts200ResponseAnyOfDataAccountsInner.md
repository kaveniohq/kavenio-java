

# ListInstagramAccounts200ResponseAnyOfDataAccountsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**username** | **String** |  |  |
|**displayName** | **String** |  |  [optional] |
|**accountType** | [**AccountTypeEnum**](#AccountTypeEnum) |  |  |
|**connectedFacebookPageId** | **String** |  |  [optional] |
|**connectedFacebookPageName** | **String** |  |  [optional] |
|**profilePictureUrl** | **URI** |  |  [optional] |
|**selected** | **Boolean** |  |  [optional] |
|**canPublish** | **Boolean** |  |  [optional] |
|**missingPermissions** | **List&lt;String&gt;** |  |  [optional] |



## Enum: AccountTypeEnum

| Name | Value |
|---- | -----|
| BUSINESS | &quot;business&quot; |
| CREATOR | &quot;creator&quot; |



