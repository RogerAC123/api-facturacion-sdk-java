# SummaryApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiV1BoletaCancelPost**](SummaryApi.md#apiV1BoletaCancelPost) | **POST** /api/v1/boleta/cancel | Anular boleta via resumen diario (estado&#x3D;3) |
| [**apiV1InvoiceCancelPost**](SummaryApi.md#apiV1InvoiceCancelPost) | **POST** /api/v1/invoice/cancel | Anular factura via comunicación de baja |
| [**apiV1SummarySendPost**](SummaryApi.md#apiV1SummarySendPost) | **POST** /api/v1/summary/send | Enviar resumen diario de boletas (RC) |
| [**apiV1TicketTicketStatusGet**](SummaryApi.md#apiV1TicketTicketStatusGet) | **GET** /api/v1/ticket/{ticket}/status | Consultar estado de ticket asíncrono (SOAP o GRE) |
| [**apiV1VoidedSendPost**](SummaryApi.md#apiV1VoidedSendPost) | **POST** /api/v1/voided/send | Enviar comunicación de baja (RA) |


<a id="apiV1BoletaCancelPost"></a>
# **apiV1BoletaCancelPost**
> ApiV1SummarySendPost202Response apiV1BoletaCancelPost(apiV1BoletaCancelPostRequest)

Anular boleta via resumen diario (estado&#x3D;3)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SummaryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    SummaryApi apiInstance = new SummaryApi(defaultClient);
    ApiV1BoletaCancelPostRequest apiV1BoletaCancelPostRequest = new ApiV1BoletaCancelPostRequest(); // ApiV1BoletaCancelPostRequest | 
    try {
      ApiV1SummarySendPost202Response result = apiInstance.apiV1BoletaCancelPost(apiV1BoletaCancelPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SummaryApi#apiV1BoletaCancelPost");
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
| **apiV1BoletaCancelPostRequest** | [**ApiV1BoletaCancelPostRequest**](ApiV1BoletaCancelPostRequest.md)|  | |

### Return type

[**ApiV1SummarySendPost202Response**](ApiV1SummarySendPost202Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Default Response |  -  |
| **400** | Default Response |  -  |

<a id="apiV1InvoiceCancelPost"></a>
# **apiV1InvoiceCancelPost**
> ApiV1SummarySendPost202Response apiV1InvoiceCancelPost(apiV1InvoiceCancelPostRequest)

Anular factura via comunicación de baja

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SummaryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    SummaryApi apiInstance = new SummaryApi(defaultClient);
    ApiV1InvoiceCancelPostRequest apiV1InvoiceCancelPostRequest = new ApiV1InvoiceCancelPostRequest(); // ApiV1InvoiceCancelPostRequest | 
    try {
      ApiV1SummarySendPost202Response result = apiInstance.apiV1InvoiceCancelPost(apiV1InvoiceCancelPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SummaryApi#apiV1InvoiceCancelPost");
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
| **apiV1InvoiceCancelPostRequest** | [**ApiV1InvoiceCancelPostRequest**](ApiV1InvoiceCancelPostRequest.md)|  | |

### Return type

[**ApiV1SummarySendPost202Response**](ApiV1SummarySendPost202Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Default Response |  -  |
| **400** | Default Response |  -  |

<a id="apiV1SummarySendPost"></a>
# **apiV1SummarySendPost**
> ApiV1SummarySendPost202Response apiV1SummarySendPost(apiV1SummarySendPostRequest)

Enviar resumen diario de boletas (RC)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SummaryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    SummaryApi apiInstance = new SummaryApi(defaultClient);
    ApiV1SummarySendPostRequest apiV1SummarySendPostRequest = new ApiV1SummarySendPostRequest(); // ApiV1SummarySendPostRequest | 
    try {
      ApiV1SummarySendPost202Response result = apiInstance.apiV1SummarySendPost(apiV1SummarySendPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SummaryApi#apiV1SummarySendPost");
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
| **apiV1SummarySendPostRequest** | [**ApiV1SummarySendPostRequest**](ApiV1SummarySendPostRequest.md)|  | |

### Return type

[**ApiV1SummarySendPost202Response**](ApiV1SummarySendPost202Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Default Response |  -  |
| **400** | Default Response |  -  |

<a id="apiV1TicketTicketStatusGet"></a>
# **apiV1TicketTicketStatusGet**
> ApiV1TicketTicketStatusGet200Response apiV1TicketTicketStatusGet(ruc, ticket)

Consultar estado de ticket asíncrono (SOAP o GRE)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SummaryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    SummaryApi apiInstance = new SummaryApi(defaultClient);
    String ruc = "ruc_example"; // String | 
    String ticket = "ticket_example"; // String | 
    try {
      ApiV1TicketTicketStatusGet200Response result = apiInstance.apiV1TicketTicketStatusGet(ruc, ticket);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SummaryApi#apiV1TicketTicketStatusGet");
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
| **ruc** | **String**|  | |
| **ticket** | **String**|  | |

### Return type

[**ApiV1TicketTicketStatusGet200Response**](ApiV1TicketTicketStatusGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **202** | Default Response |  -  |

<a id="apiV1VoidedSendPost"></a>
# **apiV1VoidedSendPost**
> ApiV1SummarySendPost202Response apiV1VoidedSendPost(apiV1VoidedSendPostRequest)

Enviar comunicación de baja (RA)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SummaryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    SummaryApi apiInstance = new SummaryApi(defaultClient);
    ApiV1VoidedSendPostRequest apiV1VoidedSendPostRequest = new ApiV1VoidedSendPostRequest(); // ApiV1VoidedSendPostRequest | 
    try {
      ApiV1SummarySendPost202Response result = apiInstance.apiV1VoidedSendPost(apiV1VoidedSendPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SummaryApi#apiV1VoidedSendPost");
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
| **apiV1VoidedSendPostRequest** | [**ApiV1VoidedSendPostRequest**](ApiV1VoidedSendPostRequest.md)|  | |

### Return type

[**ApiV1SummarySendPost202Response**](ApiV1SummarySendPost202Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Default Response |  -  |
| **400** | Default Response |  -  |

