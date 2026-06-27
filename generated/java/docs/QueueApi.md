# QueueApi

All URIs are relative to *https://api.kavenio.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createQueueSlotSchedule**](QueueApi.md#createQueueSlotSchedule) | **POST** /v1/queue/slots | Create a queue schedule |
| [**deleteQueueSlotSchedule**](QueueApi.md#deleteQueueSlotSchedule) | **DELETE** /v1/queue/slots | Delete a queue schedule |
| [**getNextQueueSlot**](QueueApi.md#getNextQueueSlot) | **GET** /v1/queue/next-slot | Get next queue slot |
| [**listQueueSlots**](QueueApi.md#listQueueSlots) | **GET** /v1/queue/slots | List queue schedules |
| [**previewQueueSlots**](QueueApi.md#previewQueueSlots) | **GET** /v1/queue/preview | Preview queue slots |
| [**updateQueueSlotSchedule**](QueueApi.md#updateQueueSlotSchedule) | **PUT** /v1/queue/slots | Update a queue schedule |


<a id="createQueueSlotSchedule"></a>
# **createQueueSlotSchedule**
> UpdateQueueSlotSchedule200Response createQueueSlotSchedule(createQueueSlotScheduleRequest)

Create a queue schedule

Creates a reusable posting queue schedule for a profile.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.QueueApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QueueApi apiInstance = new QueueApi(defaultClient);
    CreateQueueSlotScheduleRequest createQueueSlotScheduleRequest = new CreateQueueSlotScheduleRequest(); // CreateQueueSlotScheduleRequest | 
    try {
      UpdateQueueSlotSchedule200Response result = apiInstance.createQueueSlotSchedule(createQueueSlotScheduleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QueueApi#createQueueSlotSchedule");
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
| **createQueueSlotScheduleRequest** | [**CreateQueueSlotScheduleRequest**](CreateQueueSlotScheduleRequest.md)|  | |

### Return type

[**UpdateQueueSlotSchedule200Response**](UpdateQueueSlotSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Queue schedule created. |  -  |
| **401** | Authentication failed. |  -  |
| **409** | Queue schedule conflicts with current state. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Queue creation failed. |  -  |

<a id="deleteQueueSlotSchedule"></a>
# **deleteQueueSlotSchedule**
> DeletePost200Response deleteQueueSlotSchedule(profileId, queueId)

Delete a queue schedule

Deletes a reusable posting queue schedule by profile and queue ID.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.QueueApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QueueApi apiInstance = new QueueApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    String queueId = "queueId_example"; // String | 
    try {
      DeletePost200Response result = apiInstance.deleteQueueSlotSchedule(profileId, queueId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QueueApi#deleteQueueSlotSchedule");
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
| **profileId** | **String**|  | |
| **queueId** | **String**|  | |

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
| **200** | Queue schedule deleted. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Queue schedule not found. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | Queue deletion failed. |  -  |

<a id="getNextQueueSlot"></a>
# **getNextQueueSlot**
> PreviewQueueSlots200Response getNextQueueSlot(profileId, queueId, after)

Get next queue slot

Returns the next scheduled posting slot for a profile queue. The response uses the queue preview shape with at most one slot.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.QueueApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QueueApi apiInstance = new QueueApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    String queueId = "queueId_example"; // String | 
    OffsetDateTime after = OffsetDateTime.now(); // OffsetDateTime | 
    try {
      PreviewQueueSlots200Response result = apiInstance.getNextQueueSlot(profileId, queueId, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QueueApi#getNextQueueSlot");
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
| **profileId** | **String**|  | |
| **queueId** | **String**|  | [optional] |
| **after** | **OffsetDateTime**|  | [optional] |

### Return type

[**PreviewQueueSlots200Response**](PreviewQueueSlots200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Next queue slot returned. |  -  |
| **401** | Authentication failed. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | Next queue slot lookup failed. |  -  |

<a id="listQueueSlots"></a>
# **listQueueSlots**
> ListQueueSlots200Response listQueueSlots(profileId, queueId, all)

List queue schedules

Returns queue schedules for a profile, optionally filtered to one queue.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.QueueApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QueueApi apiInstance = new QueueApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    String queueId = "queueId_example"; // String | 
    String all = "true"; // String | 
    try {
      ListQueueSlots200Response result = apiInstance.listQueueSlots(profileId, queueId, all);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QueueApi#listQueueSlots");
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
| **profileId** | **String**|  | |
| **queueId** | **String**|  | [optional] |
| **all** | **String**|  | [optional] [enum: true] |

### Return type

[**ListQueueSlots200Response**](ListQueueSlots200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Queue schedules returned. |  -  |
| **401** | Authentication failed. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | Queue lookup failed. |  -  |

<a id="previewQueueSlots"></a>
# **previewQueueSlots**
> PreviewQueueSlots200Response previewQueueSlots(profileId, queueId, count, after)

Preview queue slots

Returns upcoming scheduled times for a profile queue without creating posts.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.QueueApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QueueApi apiInstance = new QueueApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    String queueId = "queueId_example"; // String | 
    Integer count = 56; // Integer | 
    OffsetDateTime after = OffsetDateTime.now(); // OffsetDateTime | 
    try {
      PreviewQueueSlots200Response result = apiInstance.previewQueueSlots(profileId, queueId, count, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QueueApi#previewQueueSlots");
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
| **profileId** | **String**|  | |
| **queueId** | **String**|  | [optional] |
| **count** | **Integer**|  | [optional] |
| **after** | **OffsetDateTime**|  | [optional] |

### Return type

[**PreviewQueueSlots200Response**](PreviewQueueSlots200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Queue preview returned. |  -  |
| **401** | Authentication failed. |  -  |
| **422** | Query parameter validation failed. |  -  |
| **500** | Queue preview failed. |  -  |

<a id="updateQueueSlotSchedule"></a>
# **updateQueueSlotSchedule**
> UpdateQueueSlotSchedule200Response updateQueueSlotSchedule(updateQueueSlotScheduleRequest)

Update a queue schedule

Updates a reusable posting queue schedule and returns the resulting schedule.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.QueueApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QueueApi apiInstance = new QueueApi(defaultClient);
    UpdateQueueSlotScheduleRequest updateQueueSlotScheduleRequest = new UpdateQueueSlotScheduleRequest(); // UpdateQueueSlotScheduleRequest | 
    try {
      UpdateQueueSlotSchedule200Response result = apiInstance.updateQueueSlotSchedule(updateQueueSlotScheduleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QueueApi#updateQueueSlotSchedule");
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
| **updateQueueSlotScheduleRequest** | [**UpdateQueueSlotScheduleRequest**](UpdateQueueSlotScheduleRequest.md)|  | |

### Return type

[**UpdateQueueSlotSchedule200Response**](UpdateQueueSlotSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Queue schedule updated. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Queue schedule not found. |  -  |
| **409** | Queue schedule conflicts with current state. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Queue update failed. |  -  |

