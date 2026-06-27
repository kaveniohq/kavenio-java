# ValidationApi

All URIs are relative to *https://api.kavenio.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**validatePost**](ValidationApi.md#validatePost) | **POST** /v1/tools/validate/post | Validate a post |
| [**validatePostLength**](ValidationApi.md#validatePostLength) | **POST** /v1/tools/validate/post-length | Validate post length |


<a id="validatePost"></a>
# **validatePost**
> ValidatePost200Response validatePost(createPostRequest)

Validate a post

Validates a post payload against platform and scheduling rules without creating a post.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ValidationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ValidationApi apiInstance = new ValidationApi(defaultClient);
    CreatePostRequest createPostRequest = new CreatePostRequest(); // CreatePostRequest | 
    try {
      ValidatePost200Response result = apiInstance.validatePost(createPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationApi#validatePost");
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

[**ValidatePost200Response**](ValidatePost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Post validation result returned. |  -  |
| **401** | Authentication failed. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Post validation failed. |  -  |

<a id="validatePostLength"></a>
# **validatePostLength**
> ValidatePostLength200Response validatePostLength(validatePostLengthRequest)

Validate post length

Returns character counts and per-platform length validity for the supplied text.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ValidationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ValidationApi apiInstance = new ValidationApi(defaultClient);
    ValidatePostLengthRequest validatePostLengthRequest = new ValidatePostLengthRequest(); // ValidatePostLengthRequest | 
    try {
      ValidatePostLength200Response result = apiInstance.validatePostLength(validatePostLengthRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationApi#validatePostLength");
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
| **validatePostLengthRequest** | [**ValidatePostLengthRequest**](ValidatePostLengthRequest.md)|  | |

### Return type

[**ValidatePostLength200Response**](ValidatePostLength200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Post length validation result returned. |  -  |
| **401** | Authentication failed. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Post length validation failed. |  -  |

