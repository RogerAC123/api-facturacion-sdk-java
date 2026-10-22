# QueuesApi

All URIs are relative to *https://api-facturacion.intifact.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getQueueStats**](QueuesApi.md#getQueueStats) | **GET** /api/v1/queues/stats | Estado de las colas BullMQ |


<a id="getQueueStats"></a>
# **getQueueStats**
> GetQueueStats200Response getQueueStats()

Estado de las colas BullMQ

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.QueuesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api-facturacion.intifact.com");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    QueuesApi apiInstance = new QueuesApi(defaultClient);
    try {
      GetQueueStats200Response result = apiInstance.getQueueStats();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QueuesApi#getQueueStats");
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

[**GetQueueStats200Response**](GetQueueStats200Response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **429** | Default Response |  -  |

