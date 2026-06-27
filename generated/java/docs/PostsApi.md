# PostsApi

All URIs are relative to *https://api.kavenio.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**bulkUploadPosts**](PostsApi.md#bulkUploadPosts) | **POST** /v1/posts/bulk-upload | Bulk upload posts |
| [**createPost**](PostsApi.md#createPost) | **POST** /v1/posts | Create a post |
| [**deletePost**](PostsApi.md#deletePost) | **DELETE** /v1/posts/{postId} | Delete a post |
| [**editPublishedPost**](PostsApi.md#editPublishedPost) | **POST** /v1/posts/{postId}/edit | Edit a published post |
| [**getPost**](PostsApi.md#getPost) | **GET** /v1/posts/{postId} | Get a post |
| [**listPosts**](PostsApi.md#listPosts) | **GET** /v1/posts | List posts |
| [**replacePost**](PostsApi.md#replacePost) | **PUT** /v1/posts/{postId} | Replace post fields |
| [**retryPost**](PostsApi.md#retryPost) | **POST** /v1/posts/{postId}/retry | Retry post publishing |
| [**unpublishPost**](PostsApi.md#unpublishPost) | **POST** /v1/posts/{postId}/unpublish | Unpublish a post |
| [**updatePost**](PostsApi.md#updatePost) | **PATCH** /v1/posts/{postId} | Update a post |


<a id="bulkUploadPosts"></a>
# **bulkUploadPosts**
> BulkUploadPosts201Response bulkUploadPosts(bulkUploadPostsRequest)

Bulk upload posts

Creates posts from CSV content and returns per-row creation or validation results.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    BulkUploadPostsRequest bulkUploadPostsRequest = new BulkUploadPostsRequest(); // BulkUploadPostsRequest | 
    try {
      BulkUploadPosts201Response result = apiInstance.bulkUploadPosts(bulkUploadPostsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#bulkUploadPosts");
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
| **bulkUploadPostsRequest** | [**BulkUploadPostsRequest**](BulkUploadPostsRequest.md)|  | |

### Return type

[**BulkUploadPosts201Response**](BulkUploadPosts201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Bulk upload processed. |  -  |
| **401** | Authentication failed. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Bulk upload failed. |  -  |

<a id="createPost"></a>
# **createPost**
> CreatePost201Response createPost(createPostRequest)

Create a post

Creates a draft, scheduled post, queue-backed post, or immediate publish request depending on the payload fields.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    CreatePostRequest createPostRequest = new CreatePostRequest(); // CreatePostRequest | 
    try {
      CreatePost201Response result = apiInstance.createPost(createPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#createPost");
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
| **createPostRequest** | [**CreatePostRequest**](CreatePostRequest.md)|  | |

### Return type

[**CreatePost201Response**](CreatePost201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Post created. |  -  |
| **401** | Authentication failed. |  -  |
| **409** | Post request conflicts with current state. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Post creation failed. |  -  |

<a id="deletePost"></a>
# **deletePost**
> DeletePost200Response deletePost(postId)

Delete a post

Deletes a post by ID and returns the deletion count.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    String postId = "postId_example"; // String | 
    try {
      DeletePost200Response result = apiInstance.deletePost(postId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#deletePost");
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
| **postId** | **String**|  | |

### Return type

[**DeletePost200Response**](DeletePost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Post deleted. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Post not found. |  -  |
| **409** | Post cannot be deleted in its current state. |  -  |
| **422** | Path parameter validation failed. |  -  |
| **500** | Post deletion failed. |  -  |

<a id="editPublishedPost"></a>
# **editPublishedPost**
> CreatePost201Response editPublishedPost(postId, editPublishedPostRequest)

Edit a published post

Applies supported lifecycle edits to published platform targets and returns the resulting post state.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    String postId = "postId_example"; // String | 
    EditPublishedPostRequest editPublishedPostRequest = new EditPublishedPostRequest(); // EditPublishedPostRequest | 
    try {
      CreatePost201Response result = apiInstance.editPublishedPost(postId, editPublishedPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#editPublishedPost");
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
| **postId** | **String**|  | |
| **editPublishedPostRequest** | [**EditPublishedPostRequest**](EditPublishedPostRequest.md)|  | |

### Return type

[**CreatePost201Response**](CreatePost201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Published post edit processed. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Post not found. |  -  |
| **409** | Post cannot be edited in its current state. |  -  |
| **422** | Request validation failed. |  -  |
| **500** | Published post edit failed. |  -  |

<a id="getPost"></a>
# **getPost**
> CreatePost201Response getPost(postId)

Get a post

Returns a post by ID, including platform target state.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    String postId = "postId_example"; // String | 
    try {
      CreatePost201Response result = apiInstance.getPost(postId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#getPost");
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
| **postId** | **String**|  | |

### Return type

[**CreatePost201Response**](CreatePost201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Post returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Post not found. |  -  |
| **422** | Path parameter validation failed. |  -  |
| **500** | Post lookup failed. |  -  |

<a id="listPosts"></a>
# **listPosts**
> ListPosts200Response listPosts(profileId, accountId, platform, status, search, fromDate, toDate, page, limit)

List posts

Returns posts for the authenticated organization, optionally filtered by profile, account, platform, status, search text, or date range.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    String accountId = "accountId_example"; // String | 
    String platform = "twitter"; // String | 
    String status = "draft"; // String | 
    String search = "search_example"; // String | 
    OffsetDateTime fromDate = OffsetDateTime.now(); // OffsetDateTime | 
    OffsetDateTime toDate = OffsetDateTime.now(); // OffsetDateTime | 
    Integer page = 56; // Integer | 
    Integer limit = 56; // Integer | 
    try {
      ListPosts200Response result = apiInstance.listPosts(profileId, accountId, platform, status, search, fromDate, toDate, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#listPosts");
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
| **accountId** | **String**|  | [optional] |
| **platform** | **String**|  | [optional] [enum: twitter, pinterest, linkedin, bluesky, mastodon, reddit, telegram, youtube, facebook, instagram, threads, tiktok, googlebusiness] |
| **status** | **String**|  | [optional] [enum: draft, scheduled, publishing, published, unpublished, failed, partial, cancelled] |
| **search** | **String**|  | [optional] |
| **fromDate** | **OffsetDateTime**|  | [optional] |
| **toDate** | **OffsetDateTime**|  | [optional] |
| **page** | **Integer**|  | [optional] |
| **limit** | **Integer**|  | [optional] |

### Return type

[**ListPosts200Response**](ListPosts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Posts returned. |  -  |
| **401** | Authentication failed. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | Post lookup failed. |  -  |

<a id="replacePost"></a>
# **replacePost**
> CreatePost201Response replacePost(postId, replacePostRequest)

Replace post fields

Updates editable fields on an existing post and returns the resulting post state.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    String postId = "postId_example"; // String | 
    ReplacePostRequest replacePostRequest = new ReplacePostRequest(); // ReplacePostRequest | 
    try {
      CreatePost201Response result = apiInstance.replacePost(postId, replacePostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#replacePost");
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
| **postId** | **String**|  | |
| **replacePostRequest** | [**ReplacePostRequest**](ReplacePostRequest.md)|  | |

### Return type

[**CreatePost201Response**](CreatePost201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Post updated. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Post not found. |  -  |
| **409** | Post cannot be updated in its current state. |  -  |
| **422** | Request validation failed. |  -  |
| **500** | Post update failed. |  -  |

<a id="retryPost"></a>
# **retryPost**
> CreatePost201Response retryPost(postId, retryPostRequest)

Retry post publishing

Retries failed platform targets for a post, optionally limited to specific target IDs.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    String postId = "postId_example"; // String | 
    RetryPostRequest retryPostRequest = new RetryPostRequest(); // RetryPostRequest | 
    try {
      CreatePost201Response result = apiInstance.retryPost(postId, retryPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#retryPost");
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
| **postId** | **String**|  | |
| **retryPostRequest** | [**RetryPostRequest**](RetryPostRequest.md)|  | |

### Return type

[**CreatePost201Response**](CreatePost201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Post retry started. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Post not found. |  -  |
| **409** | Post cannot be retried in its current state. |  -  |
| **422** | Request validation failed. |  -  |
| **500** | Post retry failed. |  -  |

<a id="unpublishPost"></a>
# **unpublishPost**
> CreatePost201Response unpublishPost(postId, unpublishPostRequest)

Unpublish a post

Starts unpublishing for published platform targets, optionally limited to specific target IDs.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    String postId = "postId_example"; // String | 
    UnpublishPostRequest unpublishPostRequest = new UnpublishPostRequest(); // UnpublishPostRequest | 
    try {
      CreatePost201Response result = apiInstance.unpublishPost(postId, unpublishPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#unpublishPost");
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
| **postId** | **String**|  | |
| **unpublishPostRequest** | [**UnpublishPostRequest**](UnpublishPostRequest.md)|  | |

### Return type

[**CreatePost201Response**](CreatePost201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Post unpublish started. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Post not found. |  -  |
| **409** | Post cannot be unpublished in its current state. |  -  |
| **422** | Request validation failed. |  -  |
| **500** | Post unpublish failed. |  -  |

<a id="updatePost"></a>
# **updatePost**
> CreatePost201Response updatePost(postId, replacePostRequest)

Update a post

Partially updates editable fields on an existing post and returns the resulting post state.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    String postId = "postId_example"; // String | 
    ReplacePostRequest replacePostRequest = new ReplacePostRequest(); // ReplacePostRequest | 
    try {
      CreatePost201Response result = apiInstance.updatePost(postId, replacePostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#updatePost");
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
| **postId** | **String**|  | |
| **replacePostRequest** | [**ReplacePostRequest**](ReplacePostRequest.md)|  | |

### Return type

[**CreatePost201Response**](CreatePost201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Post updated. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Post not found. |  -  |
| **409** | Post cannot be updated in its current state. |  -  |
| **422** | Request validation failed. |  -  |
| **500** | Post update failed. |  -  |

