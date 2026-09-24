# SummaryApi

All URIs are relative to *http://localhost:3099*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**cancelBoleta**](SummaryApi.md#cancelBoleta) | **POST** /api/v1/boleta/cancel | Anular boleta via resumen diario (estado&#x3D;3) |
| [**cancelInvoice**](SummaryApi.md#cancelInvoice) | **POST** /api/v1/invoice/cancel | Anular factura via comunicación de baja |
| [**getTicketStatus**](SummaryApi.md#getTicketStatus) | **GET** /api/v1/ticket/{ticket}/status | Consultar estado de ticket asíncrono (SOAP o GRE) |
| [**sendSummary**](SummaryApi.md#sendSummary) | **POST** /api/v1/summary/send | Enviar resumen diario de boletas (RC) |
| [**sendVoided**](SummaryApi.md#sendVoided) | **POST** /api/v1/voided/send | Enviar comunicación de baja (RA) |


<a id="cancelBoleta"></a>
# **cancelBoleta**
> SendSummary202Response cancelBoleta(cancelBoletaRequest)

Anular boleta via resumen diario (estado&#x3D;3)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SummaryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    SummaryApi apiInstance = new SummaryApi(defaultClient);
    CancelBoletaRequest cancelBoletaRequest = new CancelBoletaRequest(); // CancelBoletaRequest | 
    try {
      SendSummary202Response result = apiInstance.cancelBoleta(cancelBoletaRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SummaryApi#cancelBoleta");
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
| **cancelBoletaRequest** | [**CancelBoletaRequest**](CancelBoletaRequest.md)|  | |

### Return type

[**SendSummary202Response**](SendSummary202Response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Default Response |  -  |
| **400** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **429** | Default Response |  -  |

<a id="cancelInvoice"></a>
# **cancelInvoice**
> SendSummary202Response cancelInvoice(cancelInvoiceRequest)

Anular factura via comunicación de baja

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SummaryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    SummaryApi apiInstance = new SummaryApi(defaultClient);
    CancelInvoiceRequest cancelInvoiceRequest = new CancelInvoiceRequest(); // CancelInvoiceRequest | 
    try {
      SendSummary202Response result = apiInstance.cancelInvoice(cancelInvoiceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SummaryApi#cancelInvoice");
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
| **cancelInvoiceRequest** | [**CancelInvoiceRequest**](CancelInvoiceRequest.md)|  | |

### Return type

[**SendSummary202Response**](SendSummary202Response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Default Response |  -  |
| **400** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **429** | Default Response |  -  |

<a id="getTicketStatus"></a>
# **getTicketStatus**
> GetTicketStatus200Response getTicketStatus(ruc, ticket)

Consultar estado de ticket asíncrono (SOAP o GRE)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SummaryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    SummaryApi apiInstance = new SummaryApi(defaultClient);
    String ruc = "ruc_example"; // String | 
    String ticket = "ticket_example"; // String | 
    try {
      GetTicketStatus200Response result = apiInstance.getTicketStatus(ruc, ticket);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SummaryApi#getTicketStatus");
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

[**GetTicketStatus200Response**](GetTicketStatus200Response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **202** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **429** | Default Response |  -  |

<a id="sendSummary"></a>
# **sendSummary**
> SendSummary202Response sendSummary(sendSummaryRequest)

Enviar resumen diario de boletas (RC)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SummaryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    SummaryApi apiInstance = new SummaryApi(defaultClient);
    SendSummaryRequest sendSummaryRequest = new SendSummaryRequest(); // SendSummaryRequest | 
    try {
      SendSummary202Response result = apiInstance.sendSummary(sendSummaryRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SummaryApi#sendSummary");
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
| **sendSummaryRequest** | [**SendSummaryRequest**](SendSummaryRequest.md)|  | |

### Return type

[**SendSummary202Response**](SendSummary202Response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Default Response |  -  |
| **400** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **429** | Default Response |  -  |

<a id="sendVoided"></a>
# **sendVoided**
> SendSummary202Response sendVoided(sendVoidedRequest)

Enviar comunicación de baja (RA)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SummaryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    SummaryApi apiInstance = new SummaryApi(defaultClient);
    SendVoidedRequest sendVoidedRequest = new SendVoidedRequest(); // SendVoidedRequest | 
    try {
      SendSummary202Response result = apiInstance.sendVoided(sendVoidedRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SummaryApi#sendVoided");
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
| **sendVoidedRequest** | [**SendVoidedRequest**](SendVoidedRequest.md)|  | |

### Return type

[**SendSummary202Response**](SendSummary202Response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Default Response |  -  |
| **400** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **429** | Default Response |  -  |

