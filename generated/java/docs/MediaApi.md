# MediaApi

All URIs are relative to *https://api.kavenio.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createMediaPresign**](MediaApi.md#createMediaPresign) | **POST** /v1/media/presign | Create a media presign URL |
| [**uploadMediaBatch**](MediaApi.md#uploadMediaBatch) | **POST** /v1/media/upload | Upload media |
| [**validateMedia**](MediaApi.md#validateMedia) | **POST** /v1/tools/validate/media | Validate media |


<a id="createMediaPresign"></a>
# **createMediaPresign**
> CreateMediaPresign200Response createMediaPresign(createMediaPresignRequest)

Create a media presign URL

Creates a short-lived upload URL and public media URL for direct upload workflows.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    CreateMediaPresignRequest createMediaPresignRequest = new CreateMediaPresignRequest(); // CreateMediaPresignRequest | 
    try {
      CreateMediaPresign200Response result = apiInstance.createMediaPresign(createMediaPresignRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#createMediaPresign");
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
| **createMediaPresignRequest** | [**CreateMediaPresignRequest**](CreateMediaPresignRequest.md)|  | |

### Return type

[**CreateMediaPresign200Response**](CreateMediaPresign200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Presign URL created. |  -  |
| **401** | Authentication failed. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Media presign failed. |  -  |

<a id="uploadMediaBatch"></a>
# **uploadMediaBatch**
> UploadMediaBatch200Response uploadMediaBatch(uploadMediaBatchRequest)

Upload media

Uploads one or more base64-encoded media items and returns public URLs.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UploadMediaBatchRequest uploadMediaBatchRequest = new UploadMediaBatchRequest(); // UploadMediaBatchRequest | 
    try {
      UploadMediaBatch200Response result = apiInstance.uploadMediaBatch(uploadMediaBatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#uploadMediaBatch");
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
| **uploadMediaBatchRequest** | [**UploadMediaBatchRequest**](UploadMediaBatchRequest.md)|  | |

### Return type

[**UploadMediaBatch200Response**](UploadMediaBatch200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Media uploaded. |  -  |
| **401** | Authentication failed. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Media upload failed. |  -  |

<a id="validateMedia"></a>
# **validateMedia**
> ValidateMedia200Response validateMedia(validateMediaRequest)

Validate media

Validates a public media URL and returns content type, size, type, and platform limit information when available.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    ValidateMediaRequest validateMediaRequest = new ValidateMediaRequest(); // ValidateMediaRequest | 
    try {
      ValidateMedia200Response result = apiInstance.validateMedia(validateMediaRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#validateMedia");
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
| **validateMediaRequest** | [**ValidateMediaRequest**](ValidateMediaRequest.md)|  | |

### Return type

[**ValidateMedia200Response**](ValidateMedia200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Media validation result returned. |  -  |
| **401** | Authentication failed. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Media validation failed. |  -  |

