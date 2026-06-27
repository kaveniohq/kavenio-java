# ProfilesApi

All URIs are relative to *https://api.kavenio.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createProfile**](ProfilesApi.md#createProfile) | **POST** /v1/profiles | Create a profile |
| [**deleteProfile**](ProfilesApi.md#deleteProfile) | **DELETE** /v1/profiles/{profileId} | Delete a profile |
| [**getProfile**](ProfilesApi.md#getProfile) | **GET** /v1/profiles/{profileId} | Get a profile |
| [**listProfiles**](ProfilesApi.md#listProfiles) | **GET** /v1/profiles | List profiles |
| [**replaceProfile**](ProfilesApi.md#replaceProfile) | **PUT** /v1/profiles/{profileId} | Replace profile fields |
| [**updateProfile**](ProfilesApi.md#updateProfile) | **PATCH** /v1/profiles/{profileId} | Update a profile |


<a id="createProfile"></a>
# **createProfile**
> CreateProfile201Response createProfile(createProfileRequest)

Create a profile

Creates a customer-owned profile grouping.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProfilesApi apiInstance = new ProfilesApi(defaultClient);
    CreateProfileRequest createProfileRequest = new CreateProfileRequest(); // CreateProfileRequest | 
    try {
      CreateProfile201Response result = apiInstance.createProfile(createProfileRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProfilesApi#createProfile");
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
| **createProfileRequest** | [**CreateProfileRequest**](CreateProfileRequest.md)|  | |

### Return type

[**CreateProfile201Response**](CreateProfile201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Profile created. |  -  |
| **401** | Authentication failed. |  -  |
| **409** | A profile with this name already exists. |  -  |
| **422** | Request body validation failed. |  -  |
| **500** | Profile creation failed. |  -  |

<a id="deleteProfile"></a>
# **deleteProfile**
> DeleteProfile200Response deleteProfile(profileId)

Delete a profile

Deletes a customer-owned profile grouping.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProfilesApi apiInstance = new ProfilesApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    try {
      DeleteProfile200Response result = apiInstance.deleteProfile(profileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProfilesApi#deleteProfile");
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

### Return type

[**DeleteProfile200Response**](DeleteProfile200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Profile deleted. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Profile not found. |  -  |
| **409** | Profile cannot be deleted in its current state. |  -  |
| **422** | Path parameter validation failed. |  -  |
| **500** | Profile deletion failed. |  -  |

<a id="getProfile"></a>
# **getProfile**
> CreateProfile201Response getProfile(profileId)

Get a profile

Returns one profile by ID.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProfilesApi apiInstance = new ProfilesApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    try {
      CreateProfile201Response result = apiInstance.getProfile(profileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProfilesApi#getProfile");
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

### Return type

[**CreateProfile201Response**](CreateProfile201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Profile returned. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Profile not found. |  -  |
| **422** | Path parameter validation failed. |  -  |
| **500** | Profile lookup failed. |  -  |

<a id="listProfiles"></a>
# **listProfiles**
> ListProfiles200Response listProfiles()

List profiles

Returns the profiles available to the authenticated organization.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProfilesApi apiInstance = new ProfilesApi(defaultClient);
    try {
      ListProfiles200Response result = apiInstance.listProfiles();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProfilesApi#listProfiles");
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

[**ListProfiles200Response**](ListProfiles200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Profiles returned. |  -  |
| **401** | Authentication failed. |  -  |
| **500** | Profile lookup failed. |  -  |

<a id="replaceProfile"></a>
# **replaceProfile**
> CreateProfile201Response replaceProfile(profileId, replaceProfileRequest)

Replace profile fields

Updates profile fields for an existing customer-owned grouping.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProfilesApi apiInstance = new ProfilesApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    ReplaceProfileRequest replaceProfileRequest = new ReplaceProfileRequest(); // ReplaceProfileRequest | 
    try {
      CreateProfile201Response result = apiInstance.replaceProfile(profileId, replaceProfileRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProfilesApi#replaceProfile");
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
| **replaceProfileRequest** | [**ReplaceProfileRequest**](ReplaceProfileRequest.md)|  | |

### Return type

[**CreateProfile201Response**](CreateProfile201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Profile updated. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Profile not found. |  -  |
| **409** | A profile with this name already exists. |  -  |
| **422** | Request validation failed. |  -  |
| **500** | Profile update failed. |  -  |

<a id="updateProfile"></a>
# **updateProfile**
> CreateProfile201Response updateProfile(profileId, replaceProfileRequest)

Update a profile

Partially updates profile fields for an existing customer-owned grouping.

### Example
```java
// Import classes:
import com.kavenio.sdk.ApiClient;
import com.kavenio.sdk.ApiException;
import com.kavenio.sdk.Configuration;
import com.kavenio.sdk.auth.*;
import com.kavenio.sdk.models.*;
import com.kavenio.sdk.api.ProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.kavenio.com");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ProfilesApi apiInstance = new ProfilesApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    ReplaceProfileRequest replaceProfileRequest = new ReplaceProfileRequest(); // ReplaceProfileRequest | 
    try {
      CreateProfile201Response result = apiInstance.updateProfile(profileId, replaceProfileRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProfilesApi#updateProfile");
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
| **replaceProfileRequest** | [**ReplaceProfileRequest**](ReplaceProfileRequest.md)|  | |

### Return type

[**CreateProfile201Response**](CreateProfile201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Profile updated. |  -  |
| **401** | Authentication failed. |  -  |
| **404** | Profile not found. |  -  |
| **409** | A profile with this name already exists. |  -  |
| **422** | Request validation failed. |  -  |
| **500** | Profile update failed. |  -  |

