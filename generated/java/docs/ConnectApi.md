# ConnectApi

All URIs are relative to *https://api.kavenio.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**beginConnect**](ConnectApi.md#beginConnect) | **POST** /v1/connect/begin | Begin OAuth connect |
| [**completeConnect**](ConnectApi.md#completeConnect) | **POST** /v1/connect/complete | Complete OAuth connect |
| [**completeHostedConnectCallback**](ConnectApi.md#completeHostedConnectCallback) | **GET** /v1/connect/callback | Complete hosted OAuth callback |
| [**completeTokenConnect**](ConnectApi.md#completeTokenConnect) | **POST** /v1/connect/token | Complete token connect |
| [**connectBlueskyCredentials**](ConnectApi.md#connectBlueskyCredentials) | **POST** /v1/connect/bluesky/credentials | Connect Bluesky credentials |
| [**connectTelegramCredentials**](ConnectApi.md#connectTelegramCredentials) | **POST** /v1/connect/telegram/credentials | Connect Telegram credentials |
| [**listConnectProviders**](ConnectApi.md#listConnectProviders) | **GET** /v1/connect/providers | List connect providers |
| [**listFacebookPages**](ConnectApi.md#listFacebookPages) | **GET** /v1/connect/facebook/pages | List Facebook Pages |
| [**listGoogleBusinessConnectLocations**](ConnectApi.md#listGoogleBusinessConnectLocations) | **GET** /v1/connect/googlebusiness/locations | List Google Business connect locations |
| [**listInstagramAccounts**](ConnectApi.md#listInstagramAccounts) | **GET** /v1/connect/instagram/accounts | List Instagram accounts |
| [**listLinkedInOrganizations**](ConnectApi.md#listLinkedInOrganizations) | **GET** /v1/connect/linkedin/organizations | List LinkedIn organizations |
| [**listPinterestBoards**](ConnectApi.md#listPinterestBoards) | **GET** /v1/connect/pinterest/boards | List Pinterest boards |
| [**listRedditFlairs**](ConnectApi.md#listRedditFlairs) | **GET** /v1/connect/reddit/flairs | List Reddit flairs |
| [**listRedditSubreddits**](ConnectApi.md#listRedditSubreddits) | **GET** /v1/connect/reddit/subreddits | List Reddit subreddits |
| [**listYouTubeChannels**](ConnectApi.md#listYouTubeChannels) | **GET** /v1/connect/youtube/channels | List YouTube channels |
| [**listYouTubePlaylists**](ConnectApi.md#listYouTubePlaylists) | **GET** /v1/connect/youtube/playlists | List YouTube playlists |
| [**selectFacebookPage**](ConnectApi.md#selectFacebookPage) | **POST** /v1/connect/facebook/select-page | Select Facebook Page |
| [**selectGoogleBusinessLocation**](ConnectApi.md#selectGoogleBusinessLocation) | **POST** /v1/connect/googlebusiness/select-location | Select Google Business location |
| [**selectInstagramAccount**](ConnectApi.md#selectInstagramAccount) | **POST** /v1/connect/instagram/select-account | Select Instagram account |
| [**selectLinkedInOrganization**](ConnectApi.md#selectLinkedInOrganization) | **POST** /v1/connect/linkedin/select-organization | Select LinkedIn organization |
| [**selectPinterestBoard**](ConnectApi.md#selectPinterestBoard) | **POST** /v1/connect/pinterest/select-board | Select Pinterest board |
| [**selectYouTubeChannel**](ConnectApi.md#selectYouTubeChannel) | **POST** /v1/connect/youtube/select-channel | Select YouTube channel |


<a id="beginConnect"></a>
# **beginConnect**
> BeginConnect200Response beginConnect(beginConnectRequest)

Begin OAuth connect

Creates an OAuth connect session and returns the provider authorization URL.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    BeginConnectRequest beginConnectRequest = new BeginConnectRequest(); // BeginConnectRequest | 
    try {
      BeginConnect200Response result = apiInstance.beginConnect(beginConnectRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#beginConnect");
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
| **beginConnectRequest** | [**BeginConnectRequest**](BeginConnectRequest.md)|  | |

### Return type

[**BeginConnect200Response**](BeginConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connect session created. |  -  |
| **401** | Authentication failed. |  -  |
| **409** | Provider cannot be connected in the current state. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Connect session creation failed. |  -  |

<a id="completeConnect"></a>
# **completeConnect**
> CompleteConnect200Response completeConnect(completeConnectRequest)

Complete OAuth connect

Completes an OAuth connect session using the provider authorization code.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    CompleteConnectRequest completeConnectRequest = new CompleteConnectRequest(); // CompleteConnectRequest | 
    try {
      CompleteConnect200Response result = apiInstance.completeConnect(completeConnectRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#completeConnect");
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
| **completeConnectRequest** | [**CompleteConnectRequest**](CompleteConnectRequest.md)|  | |

### Return type

[**CompleteConnect200Response**](CompleteConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connect session completed. |  -  |
| **401** | Authentication failed. |  -  |
| **409** | Connect session cannot be completed. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Connect completion failed. |  -  |

<a id="completeHostedConnectCallback"></a>
# **completeHostedConnectCallback**
> completeHostedConnectCallback(state, code, error)

Complete hosted OAuth callback

Handles provider OAuth redirects for hosted connect flows and redirects back to the Kavenio app with the connection result.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    String state = "state_example"; // String | 
    String code = "code_example"; // String | 
    String error = "error_example"; // String | 
    try {
      apiInstance.completeHostedConnectCallback(state, code, error);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#completeHostedConnectCallback");
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
| **state** | **String**|  | [optional] |
| **code** | **String**|  | [optional] |
| **error** | **String**|  | [optional] |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **302** | Redirects to the configured Kavenio app completion URL with connection status query parameters. |  -  |
| **500** | Hosted connect callback failed. |  -  |

<a id="completeTokenConnect"></a>
# **completeTokenConnect**
> CompleteConnect200Response completeTokenConnect(completeTokenConnectRequest)

Complete token connect

Connects a provider that requires user-supplied token credentials. Raw tokens are accepted only in the request and are never returned.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    CompleteTokenConnectRequest completeTokenConnectRequest = new CompleteTokenConnectRequest(); // CompleteTokenConnectRequest | 
    try {
      CompleteConnect200Response result = apiInstance.completeTokenConnect(completeTokenConnectRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#completeTokenConnect");
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
| **completeTokenConnectRequest** | [**CompleteTokenConnectRequest**](CompleteTokenConnectRequest.md)|  | |

### Return type

[**CompleteConnect200Response**](CompleteConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Token connect completed. |  -  |
| **401** | Authentication failed. |  -  |
| **409** | Provider cannot be connected in the current state. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Token connect failed. |  -  |

<a id="connectBlueskyCredentials"></a>
# **connectBlueskyCredentials**
> CompleteConnect200Response connectBlueskyCredentials(connectBlueskyCredentialsRequest)

Connect Bluesky credentials

Connects a Bluesky account using an identifier and app password. The app password is accepted only in the request and is never returned.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    ConnectBlueskyCredentialsRequest connectBlueskyCredentialsRequest = new ConnectBlueskyCredentialsRequest(); // ConnectBlueskyCredentialsRequest | 
    try {
      CompleteConnect200Response result = apiInstance.connectBlueskyCredentials(connectBlueskyCredentialsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#connectBlueskyCredentials");
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
| **connectBlueskyCredentialsRequest** | [**ConnectBlueskyCredentialsRequest**](ConnectBlueskyCredentialsRequest.md)|  | |

### Return type

[**CompleteConnect200Response**](CompleteConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Bluesky account connected. |  -  |
| **401** | Authentication failed. |  -  |
| **409** | Bluesky account cannot be connected. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Bluesky credential connect failed. |  -  |

<a id="connectTelegramCredentials"></a>
# **connectTelegramCredentials**
> CompleteConnect200Response connectTelegramCredentials(connectTelegramCredentialsRequest)

Connect Telegram credentials

Connects a Telegram bot or chat using supplied credentials. The bot token is accepted only in the request and is never returned.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    ConnectTelegramCredentialsRequest connectTelegramCredentialsRequest = new ConnectTelegramCredentialsRequest(); // ConnectTelegramCredentialsRequest | 
    try {
      CompleteConnect200Response result = apiInstance.connectTelegramCredentials(connectTelegramCredentialsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#connectTelegramCredentials");
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
| **connectTelegramCredentialsRequest** | [**ConnectTelegramCredentialsRequest**](ConnectTelegramCredentialsRequest.md)|  | |

### Return type

[**CompleteConnect200Response**](CompleteConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Telegram account connected. |  -  |
| **401** | Authentication failed. |  -  |
| **409** | Telegram account cannot be connected. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Telegram credential connect failed. |  -  |

<a id="listConnectProviders"></a>
# **listConnectProviders**
> ListConnectProviders200Response listConnectProviders()

List connect providers

Returns social and ads providers available to the authenticated user.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    try {
      ListConnectProviders200Response result = apiInstance.listConnectProviders();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#listConnectProviders");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ListConnectProviders200Response**](ListConnectProviders200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connect providers returned. |  -  |
| **401** | Authentication failed. |  -  |
| **500** | Connect provider lookup failed. |  -  |

<a id="listFacebookPages"></a>
# **listFacebookPages**
> ListFacebookPages200Response listFacebookPages(accountId)

List Facebook Pages

Returns Facebook Pages available from a connected Facebook account.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    try {
      ListFacebookPages200Response result = apiInstance.listFacebookPages(accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#listFacebookPages");
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

[**ListFacebookPages200Response**](ListFacebookPages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Facebook Pages returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | Facebook Page lookup failed. |  -  |

<a id="listGoogleBusinessConnectLocations"></a>
# **listGoogleBusinessConnectLocations**
> ListGoogleBusinessConnectLocations200Response listGoogleBusinessConnectLocations(accountId, pageSize, pageToken, search, filter)

List Google Business connect locations

Returns Google Business locations available during account connection.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    Integer pageSize = 56; // Integer | 
    String pageToken = "pageToken_example"; // String | 
    String search = "search_example"; // String | 
    String filter = "filter_example"; // String | 
    try {
      ListGoogleBusinessConnectLocations200Response result = apiInstance.listGoogleBusinessConnectLocations(accountId, pageSize, pageToken, search, filter);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#listGoogleBusinessConnectLocations");
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
| **pageSize** | **Integer**|  | [optional] |
| **pageToken** | **String**|  | [optional] |
| **search** | **String**|  | [optional] |
| **filter** | **String**|  | [optional] |

### Return type

[**ListGoogleBusinessConnectLocations200Response**](ListGoogleBusinessConnectLocations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Google Business locations returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | Google Business location lookup failed. |  -  |

<a id="listInstagramAccounts"></a>
# **listInstagramAccounts**
> ListInstagramAccounts200Response listInstagramAccounts(accountId)

List Instagram accounts

Returns Instagram business or creator accounts available from a connected account.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    try {
      ListInstagramAccounts200Response result = apiInstance.listInstagramAccounts(accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#listInstagramAccounts");
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

[**ListInstagramAccounts200Response**](ListInstagramAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Instagram accounts returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | Instagram account lookup failed. |  -  |

<a id="listLinkedInOrganizations"></a>
# **listLinkedInOrganizations**
> ListLinkedInOrganizations200Response listLinkedInOrganizations(accountId)

List LinkedIn organizations

Returns LinkedIn organizations available from a connected LinkedIn account.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    try {
      ListLinkedInOrganizations200Response result = apiInstance.listLinkedInOrganizations(accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#listLinkedInOrganizations");
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

[**ListLinkedInOrganizations200Response**](ListLinkedInOrganizations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | LinkedIn organizations returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | LinkedIn organization lookup failed. |  -  |

<a id="listPinterestBoards"></a>
# **listPinterestBoards**
> ListPinterestBoards200Response listPinterestBoards(accountId)

List Pinterest boards

Returns Pinterest boards available from a connected Pinterest account.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    try {
      ListPinterestBoards200Response result = apiInstance.listPinterestBoards(accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#listPinterestBoards");
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

[**ListPinterestBoards200Response**](ListPinterestBoards200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pinterest boards returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | Pinterest board lookup failed. |  -  |

<a id="listRedditFlairs"></a>
# **listRedditFlairs**
> ListRedditFlairs200Response listRedditFlairs(accountId, subreddit)

List Reddit flairs

Returns post flair choices for a connected Reddit account and subreddit.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    String subreddit = "subreddit_example"; // String | 
    try {
      ListRedditFlairs200Response result = apiInstance.listRedditFlairs(accountId, subreddit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#listRedditFlairs");
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
| **subreddit** | **String**|  | |

### Return type

[**ListRedditFlairs200Response**](ListRedditFlairs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reddit flairs returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account or subreddit not found. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | Reddit flair lookup failed. |  -  |

<a id="listRedditSubreddits"></a>
# **listRedditSubreddits**
> ListRedditSubreddits200Response listRedditSubreddits(accountId)

List Reddit subreddits

Returns Reddit subreddits available from a connected Reddit account.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    try {
      ListRedditSubreddits200Response result = apiInstance.listRedditSubreddits(accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#listRedditSubreddits");
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

[**ListRedditSubreddits200Response**](ListRedditSubreddits200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reddit subreddits returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | Reddit subreddit lookup failed. |  -  |

<a id="listYouTubeChannels"></a>
# **listYouTubeChannels**
> ListYouTubeChannels200Response listYouTubeChannels(accountId)

List YouTube channels

Returns YouTube channels available from a connected YouTube account.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    try {
      ListYouTubeChannels200Response result = apiInstance.listYouTubeChannels(accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#listYouTubeChannels");
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

[**ListYouTubeChannels200Response**](ListYouTubeChannels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | YouTube channels returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | YouTube channel lookup failed. |  -  |

<a id="listYouTubePlaylists"></a>
# **listYouTubePlaylists**
> ListYouTubePlaylists200Response listYouTubePlaylists(accountId)

List YouTube playlists

Returns YouTube playlists available from a connected YouTube account.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    try {
      ListYouTubePlaylists200Response result = apiInstance.listYouTubePlaylists(accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#listYouTubePlaylists");
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

[**ListYouTubePlaylists200Response**](ListYouTubePlaylists200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | YouTube playlists returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account not found. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | YouTube playlist lookup failed. |  -  |

<a id="selectFacebookPage"></a>
# **selectFacebookPage**
> CompleteConnect200Response selectFacebookPage(selectFacebookPageRequest)

Select Facebook Page

Selects a Facebook Page destination and attaches it to a profile.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    SelectFacebookPageRequest selectFacebookPageRequest = new SelectFacebookPageRequest(); // SelectFacebookPageRequest | 
    try {
      CompleteConnect200Response result = apiInstance.selectFacebookPage(selectFacebookPageRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#selectFacebookPage");
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
| **selectFacebookPageRequest** | [**SelectFacebookPageRequest**](SelectFacebookPageRequest.md)|  | |

### Return type

[**CompleteConnect200Response**](CompleteConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Facebook Page selected. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account or Page not found. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Facebook Page selection failed. |  -  |

<a id="selectGoogleBusinessLocation"></a>
# **selectGoogleBusinessLocation**
> CompleteConnect200Response selectGoogleBusinessLocation(selectGoogleBusinessLocationRequest)

Select Google Business location

Selects a Google Business location destination and attaches it to a profile.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    SelectGoogleBusinessLocationRequest selectGoogleBusinessLocationRequest = new SelectGoogleBusinessLocationRequest(); // SelectGoogleBusinessLocationRequest | 
    try {
      CompleteConnect200Response result = apiInstance.selectGoogleBusinessLocation(selectGoogleBusinessLocationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#selectGoogleBusinessLocation");
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
| **selectGoogleBusinessLocationRequest** | [**SelectGoogleBusinessLocationRequest**](SelectGoogleBusinessLocationRequest.md)|  | |

### Return type

[**CompleteConnect200Response**](CompleteConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Google Business location selected. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account or location not found. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Google Business location selection failed. |  -  |

<a id="selectInstagramAccount"></a>
# **selectInstagramAccount**
> CompleteConnect200Response selectInstagramAccount(selectInstagramAccountRequest)

Select Instagram account

Selects an Instagram account destination and attaches it to a profile.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    SelectInstagramAccountRequest selectInstagramAccountRequest = new SelectInstagramAccountRequest(); // SelectInstagramAccountRequest | 
    try {
      CompleteConnect200Response result = apiInstance.selectInstagramAccount(selectInstagramAccountRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#selectInstagramAccount");
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
| **selectInstagramAccountRequest** | [**SelectInstagramAccountRequest**](SelectInstagramAccountRequest.md)|  | |

### Return type

[**CompleteConnect200Response**](CompleteConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Instagram account selected. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account or Instagram account not found. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Instagram account selection failed. |  -  |

<a id="selectLinkedInOrganization"></a>
# **selectLinkedInOrganization**
> CompleteConnect200Response selectLinkedInOrganization(selectLinkedInOrganizationRequest)

Select LinkedIn organization

Selects a LinkedIn organization destination and attaches it to a profile.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    SelectLinkedInOrganizationRequest selectLinkedInOrganizationRequest = new SelectLinkedInOrganizationRequest(); // SelectLinkedInOrganizationRequest | 
    try {
      CompleteConnect200Response result = apiInstance.selectLinkedInOrganization(selectLinkedInOrganizationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#selectLinkedInOrganization");
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
| **selectLinkedInOrganizationRequest** | [**SelectLinkedInOrganizationRequest**](SelectLinkedInOrganizationRequest.md)|  | |

### Return type

[**CompleteConnect200Response**](CompleteConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | LinkedIn organization selected. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account or organization not found. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | LinkedIn organization selection failed. |  -  |

<a id="selectPinterestBoard"></a>
# **selectPinterestBoard**
> CompleteConnect200Response selectPinterestBoard(selectPinterestBoardRequest)

Select Pinterest board

Selects a Pinterest board destination and attaches it to a profile.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    SelectPinterestBoardRequest selectPinterestBoardRequest = new SelectPinterestBoardRequest(); // SelectPinterestBoardRequest | 
    try {
      CompleteConnect200Response result = apiInstance.selectPinterestBoard(selectPinterestBoardRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#selectPinterestBoard");
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
| **selectPinterestBoardRequest** | [**SelectPinterestBoardRequest**](SelectPinterestBoardRequest.md)|  | |

### Return type

[**CompleteConnect200Response**](CompleteConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pinterest board selected. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account or board not found. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Pinterest board selection failed. |  -  |

<a id="selectYouTubeChannel"></a>
# **selectYouTubeChannel**
> CompleteConnect200Response selectYouTubeChannel(selectYouTubeChannelRequest)

Select YouTube channel

Selects a YouTube channel destination and attaches it to a profile.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    SelectYouTubeChannelRequest selectYouTubeChannelRequest = new SelectYouTubeChannelRequest(); // SelectYouTubeChannelRequest | 
    try {
      CompleteConnect200Response result = apiInstance.selectYouTubeChannel(selectYouTubeChannelRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#selectYouTubeChannel");
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
| **selectYouTubeChannelRequest** | [**SelectYouTubeChannelRequest**](SelectYouTubeChannelRequest.md)|  | |

### Return type

[**CompleteConnect200Response**](CompleteConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | YouTube channel selected. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Connected account or channel not found. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | YouTube channel selection failed. |  -  |

