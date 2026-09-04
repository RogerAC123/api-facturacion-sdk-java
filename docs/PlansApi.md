# PlansApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiV1PlansGet**](PlansApi.md#apiV1PlansGet) | **GET** /api/v1/plans | Listar planes (solo master) |
| [**apiV1PlansIdDelete**](PlansApi.md#apiV1PlansIdDelete) | **DELETE** /api/v1/plans/{id} | Desactivar plan (soft-delete) |
| [**apiV1PlansIdPut**](PlansApi.md#apiV1PlansIdPut) | **PUT** /api/v1/plans/{id} | Actualizar plan (precio, docs, nombre, estado) |
| [**apiV1PlansPost**](PlansApi.md#apiV1PlansPost) | **POST** /api/v1/plans | Crear plan |


<a id="apiV1PlansGet"></a>
# **apiV1PlansGet**
> apiV1PlansGet()

Listar planes (solo master)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.PlansApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    PlansApi apiInstance = new PlansApi(defaultClient);
    try {
      apiInstance.apiV1PlansGet();
    } catch (ApiException e) {
      System.err.println("Exception when calling PlansApi#apiV1PlansGet");
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

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

<a id="apiV1PlansIdDelete"></a>
# **apiV1PlansIdDelete**
> apiV1PlansIdDelete(id)

Desactivar plan (soft-delete)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.PlansApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    PlansApi apiInstance = new PlansApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1PlansIdDelete(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling PlansApi#apiV1PlansIdDelete");
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
| **id** | **UUID**|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

<a id="apiV1PlansIdPut"></a>
# **apiV1PlansIdPut**
> apiV1PlansIdPut(id, apiV1PlansIdPutRequest)

Actualizar plan (precio, docs, nombre, estado)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.PlansApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    PlansApi apiInstance = new PlansApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    ApiV1PlansIdPutRequest apiV1PlansIdPutRequest = new ApiV1PlansIdPutRequest(); // ApiV1PlansIdPutRequest | 
    try {
      apiInstance.apiV1PlansIdPut(id, apiV1PlansIdPutRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling PlansApi#apiV1PlansIdPut");
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
| **id** | **UUID**|  | |
| **apiV1PlansIdPutRequest** | [**ApiV1PlansIdPutRequest**](ApiV1PlansIdPutRequest.md)|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

<a id="apiV1PlansPost"></a>
# **apiV1PlansPost**
> apiV1PlansPost(apiV1PlansPostRequest)

Crear plan

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.PlansApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    PlansApi apiInstance = new PlansApi(defaultClient);
    ApiV1PlansPostRequest apiV1PlansPostRequest = new ApiV1PlansPostRequest(); // ApiV1PlansPostRequest | 
    try {
      apiInstance.apiV1PlansPost(apiV1PlansPostRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling PlansApi#apiV1PlansPost");
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
| **apiV1PlansPostRequest** | [**ApiV1PlansPostRequest**](ApiV1PlansPostRequest.md)|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

