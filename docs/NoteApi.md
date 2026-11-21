# NoteApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**computeNote**](NoteApi.md#computeNote) | **POST** /api/v1/note/compute | Calcular importes (IGV, descuentos, totales) sin emitir |
| [**getNoteCdr**](NoteApi.md#getNoteCdr) | **GET** /api/v1/note/{id}/cdr | Descargar CDR (constancia de SUNAT) |
| [**getNotePdf**](NoteApi.md#getNotePdf) | **GET** /api/v1/note/{id}/pdf | Obtener PDF de la nota |
| [**getNoteXml**](NoteApi.md#getNoteXml) | **GET** /api/v1/note/{id}/xml | Descargar XML firmado |
| [**sendNote**](NoteApi.md#sendNote) | **POST** /api/v1/note/send | Enviar nota de crédito (07) o débito (08) a SUNAT |


<a id="computeNote"></a>
# **computeNote**
> ComputeInvoice200Response computeNote(computeInvoiceRequest)

Calcular importes (IGV, descuentos, totales) sin emitir

Motor de cálculo para notas: recibe ítems crudos (cantidad, valorUnitario sin IGV, afectación, descuento) y un descuento global opcional, y devuelve TODOS los importes fiscales calculados. No emite ni persiste nada — úsalo para previsualizar o para alimentar POST /note/send (agrega tú el documento afectado y el motivo).

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.NoteApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    NoteApi apiInstance = new NoteApi(defaultClient);
    ComputeInvoiceRequest computeInvoiceRequest = new ComputeInvoiceRequest(); // ComputeInvoiceRequest | 
    try {
      ComputeInvoice200Response result = apiInstance.computeNote(computeInvoiceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NoteApi#computeNote");
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
| **computeInvoiceRequest** | [**ComputeInvoiceRequest**](ComputeInvoiceRequest.md)|  | |

### Return type

[**ComputeInvoice200Response**](ComputeInvoice200Response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **429** | Default Response |  -  |

<a id="getNoteCdr"></a>
# **getNoteCdr**
> getNoteCdr(id)

Descargar CDR (constancia de SUNAT)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.NoteApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    NoteApi apiInstance = new NoteApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.getNoteCdr(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling NoteApi#getNoteCdr");
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

<a id="getNotePdf"></a>
# **getNotePdf**
> getNotePdf(id)

Obtener PDF de la nota

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.NoteApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    NoteApi apiInstance = new NoteApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.getNotePdf(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling NoteApi#getNotePdf");
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

<a id="getNoteXml"></a>
# **getNoteXml**
> getNoteXml(id)

Descargar XML firmado

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.NoteApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    NoteApi apiInstance = new NoteApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.getNoteXml(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling NoteApi#getNoteXml");
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

<a id="sendNote"></a>
# **sendNote**
> SendInvoice202Response sendNote(sendNoteRequest)

Enviar nota de crédito (07) o débito (08) a SUNAT

Genera XML UBL 2.1, firma y encola. Responde 202. Consultar GET /documents/{id} para el resultado final. Idempotente por (RUC emisor, tipoDoc, serie, correlativo): reenviar el mismo comprobante NO lo duplica. Si ya fue aceptado devuelve el mismo id y hash sin reenviar nada a SUNAT; si sigue en proceso responde 409 (esperá el resultado, no cambies el correlativo). Solo un RECHAZADO exige un correlativo nuevo.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.NoteApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    NoteApi apiInstance = new NoteApi(defaultClient);
    SendNoteRequest sendNoteRequest = new SendNoteRequest(); // SendNoteRequest | 
    try {
      SendInvoice202Response result = apiInstance.sendNote(sendNoteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NoteApi#sendNote");
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
| **sendNoteRequest** | [**SendNoteRequest**](SendNoteRequest.md)|  | |

### Return type

[**SendInvoice202Response**](SendInvoice202Response.md)

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
| **409** | Default Response |  -  |
| **429** | Default Response |  -  |

