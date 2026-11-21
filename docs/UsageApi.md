# UsageApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getUsage**](UsageApi.md#getUsage) | **GET** /api/v1/usage | Consumo del tenant actual (docs emitidos / límite del plan) |


<a id="getUsage"></a>
# **getUsage**
> getUsage()

Consumo del tenant actual (docs emitidos / límite del plan)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.UsageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    UsageApi apiInstance = new UsageApi(defaultClient);
    try {
      apiInstance.getUsage();
    } catch (ApiException e) {
      System.err.println("Exception when calling UsageApi#getUsage");
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

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **429** | Default Response |  -  |

