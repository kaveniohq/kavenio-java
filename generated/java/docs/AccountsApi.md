# AccountsApi

All URIs are relative to *https://api.kavenio.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**checkAccountHealth**](AccountsApi.md#checkAccountHealth) | **POST** /v1/accounts/{accountId}/health | Check account health |
| [**disconnectAccount**](AccountsApi.md#disconnectAccount) | **POST** /v1/accounts/{accountId}/disconnect | Disconnect an account |
| [**getAccount**](AccountsApi.md#getAccount) | **GET** /v1/accounts/{accountId} | Get a connected account |
| [**listAccounts**](AccountsApi.md#listAccounts) | **GET** /v1/accounts | List connected accounts |
| [**moveAccount**](AccountsApi.md#moveAccount) | **POST** /v1/accounts/{accountId}/move | Move a connected account |
| [**refreshTikTokCreatorInfo**](AccountsApi.md#refreshTikTokCreatorInfo) | **POST** /v1/accounts/{accountId}/tiktok/creator-info | Refresh TikTok creator info |
| [**replaceAccount**](AccountsApi.md#replaceAccount) | **PUT** /v1/accounts/{accountId} | Replace account fields |
| [**updateAccount**](AccountsApi.md#updateAccount) | **PATCH** /v1/accounts/{accountId} | Update a connected account |


<a id="checkAccountHealth"></a>
# **checkAccountHealth**
> CheckAccountHealth200Response checkAccountHealth(accountId)

Check account health

Refreshes account health and readiness information for a connected account.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.AccountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountsApi apiInstance = new AccountsApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    try {
      CheckAccountHealth200Response result = apiInstance.checkAccountHealth(accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#checkAccountHealth");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **accountId** | **String**|  | |

### Return type

[**CheckAccountHealth200Response**](CheckAccountHealth200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account health returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **422** | Path parameter validation failed. |  -  |
| **500** | Account health check failed. |  -  |

<a id="disconnectAccount"></a>
# **disconnectAccount**
> DisconnectAccount200Response disconnectAccount(accountId)

Disconnect an account

Disconnects a connected account and returns the resulting account state.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.AccountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountsApi apiInstance = new AccountsApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    try {
      DisconnectAccount200Response result = apiInstance.disconnectAccount(accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#disconnectAccount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **accountId** | **String**|  | |

### Return type

[**DisconnectAccount200Response**](DisconnectAccount200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connected account disconnected. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **409** | Connected account cannot be disconnected. |  -  |
| **422** | Path parameter validation failed. |  -  |
| **500** | Connected account disconnect failed. |  -  |

<a id="getAccount"></a>
# **getAccount**
> GetAccount200Response getAccount(accountId)

Get a connected account

Returns one connected account by ID.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.AccountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountsApi apiInstance = new AccountsApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    try {
      GetAccount200Response result = apiInstance.getAccount(accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#getAccount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **accountId** | **String**|  | |

### Return type

[**GetAccount200Response**](GetAccount200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connected account returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **422** | Path parameter validation failed. |  -  |
| **500** | Connected account lookup failed. |  -  |

<a id="listAccounts"></a>
# **listAccounts**
> ListAccounts200Response listAccounts(profileId, platform, status, limit, cursor)

List connected accounts

Returns connected social accounts for the authenticated organization.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.AccountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountsApi apiInstance = new AccountsApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    String platform = "twitter"; // String | 
    String status = "connected"; // String | 
    Integer limit = 56; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      ListAccounts200Response result = apiInstance.listAccounts(profileId, platform, status, limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#listAccounts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **profileId** | **String**|  | [optional] |
| **platform** | **String**|  | [optional] [enum: twitter, facebook, instagram, linkedin, tiktok, youtube, threads, reddit, pinterest, bluesky, mastodon, googlebusiness, telegram, snapchat, discord, whatsapp, metaads, googleads, tiktokads, linkedinads, pinterestads, xads] |
| **status** | **String**|  | [optional] [enum: connected, disconnected, needs_reconnect, revoked] |
| **limit** | **Integer**|  | [optional] |
| **cursor** | **String**|  | [optional] |

### Return type

[**ListAccounts200Response**](ListAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connected accounts returned. |  -  |
| **401** | Authentication failed. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | Connected account lookup failed. |  -  |

<a id="moveAccount"></a>
# **moveAccount**
> GetAccount200Response moveAccount(accountId, moveAccountRequest)

Move a connected account

Moves a connected account to another profile.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.AccountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountsApi apiInstance = new AccountsApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    MoveAccountRequest moveAccountRequest = new MoveAccountRequest(); // MoveAccountRequest | 
    try {
      GetAccount200Response result = apiInstance.moveAccount(accountId, moveAccountRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#moveAccount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **accountId** | **String**|  | |
| **moveAccountRequest** | [**MoveAccountRequest**](MoveAccountRequest.md)|  | |

### Return type

[**GetAccount200Response**](GetAccount200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connected account moved. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account or profile not found. |  -  |
| **409** | Connected account cannot be moved. |  -  |
| **422** | Request validation failed. |  -  |
| **500** | Connected account move failed. |  -  |

<a id="refreshTikTokCreatorInfo"></a>
# **refreshTikTokCreatorInfo**
> RefreshTikTokCreatorInfo200Response refreshTikTokCreatorInfo(accountId)

Refresh TikTok creator info

Refreshes TikTok creator information and posting readiness for a connected account.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.AccountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountsApi apiInstance = new AccountsApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    try {
      RefreshTikTokCreatorInfo200Response result = apiInstance.refreshTikTokCreatorInfo(accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#refreshTikTokCreatorInfo");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **accountId** | **String**|  | |

### Return type

[**RefreshTikTokCreatorInfo200Response**](RefreshTikTokCreatorInfo200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | TikTok creator information returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **422** | Path parameter validation failed. |  -  |
| **500** | TikTok creator information refresh failed. |  -  |

<a id="replaceAccount"></a>
# **replaceAccount**
> GetAccount200Response replaceAccount(accountId, replaceAccountRequest)

Replace account fields

Updates editable connected account fields. Public metadata updates must not include provider credential fields.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.AccountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountsApi apiInstance = new AccountsApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    ReplaceAccountRequest replaceAccountRequest = new ReplaceAccountRequest(); // ReplaceAccountRequest | 
    try {
      GetAccount200Response result = apiInstance.replaceAccount(accountId, replaceAccountRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#replaceAccount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **accountId** | **String**|  | |
| **replaceAccountRequest** | [**ReplaceAccountRequest**](ReplaceAccountRequest.md)|  | |

### Return type

[**GetAccount200Response**](GetAccount200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connected account updated. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **409** | Connected account cannot be updated. |  -  |
| **422** | Request validation failed. |  -  |
| **500** | Connected account update failed. |  -  |

<a id="updateAccount"></a>
# **updateAccount**
> GetAccount200Response updateAccount(accountId, replaceAccountRequest)

Update a connected account

Partially updates editable connected account fields. Public metadata updates must not include provider credential fields.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.AccountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountsApi apiInstance = new AccountsApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    ReplaceAccountRequest replaceAccountRequest = new ReplaceAccountRequest(); // ReplaceAccountRequest | 
    try {
      GetAccount200Response result = apiInstance.updateAccount(accountId, replaceAccountRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#updateAccount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **accountId** | **String**|  | |
| **replaceAccountRequest** | [**ReplaceAccountRequest**](ReplaceAccountRequest.md)|  | |

### Return type

[**GetAccount200Response**](GetAccount200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connected account updated. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **409** | Connected account cannot be updated. |  -  |
| **422** | Request validation failed. |  -  |
| **500** | Connected account update failed. |  -  |

