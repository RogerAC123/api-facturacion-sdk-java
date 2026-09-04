# QueuesApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiV1QueuesStatsGet**](QueuesApi.md#apiV1QueuesStatsGet) | **GET** /api/v1/queues/stats | Estado de las colas BullMQ |


<a id="apiV1QueuesStatsGet"></a>
# **apiV1QueuesStatsGet**
> ApiV1QueuesStatsGet200Response apiV1QueuesStatsGet()

Estado de las colas BullMQ

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.QueuesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    QueuesApi apiInstance = new QueuesApi(defaultClient);
    try {
      ApiV1QueuesStatsGet200Response result = apiInstance.apiV1QueuesStatsGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QueuesApi#apiV1QueuesStatsGet");
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

[**ApiV1QueuesStatsGet200Response**](ApiV1QueuesStatsGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **403** | Default Response |  -  |

