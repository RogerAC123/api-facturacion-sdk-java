# NoteApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiV1NoteComputePost**](NoteApi.md#apiV1NoteComputePost) | **POST** /api/v1/note/compute | Calcular importes (IGV, descuentos, totales) sin emitir |
| [**apiV1NoteIdCdrGet**](NoteApi.md#apiV1NoteIdCdrGet) | **GET** /api/v1/note/{id}/cdr | Descargar CDR (constancia de SUNAT) |
| [**apiV1NoteIdPdfGet**](NoteApi.md#apiV1NoteIdPdfGet) | **GET** /api/v1/note/{id}/pdf | Obtener PDF de la nota |
| [**apiV1NoteIdXmlGet**](NoteApi.md#apiV1NoteIdXmlGet) | **GET** /api/v1/note/{id}/xml | Descargar XML firmado |
| [**apiV1NoteSendPost**](NoteApi.md#apiV1NoteSendPost) | **POST** /api/v1/note/send | Enviar nota de crédito (07) o débito (08) a SUNAT |


<a id="apiV1NoteComputePost"></a>
# **apiV1NoteComputePost**
> ApiV1InvoiceComputePost200Response apiV1NoteComputePost(apiV1NoteComputePostRequest)

Calcular importes (IGV, descuentos, totales) sin emitir

Motor de cálculo para notas: recibe ítems crudos (cantidad, valorUnitario sin IGV, afectación, descuento) y un descuento global opcional, y devuelve TODOS los importes fiscales calculados. No emite ni persiste nada — úsalo para previsualizar o para alimentar POST /note/send (agrega tú el documento afectado y el motivo).

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.NoteApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    NoteApi apiInstance = new NoteApi(defaultClient);
    ApiV1NoteComputePostRequest apiV1NoteComputePostRequest = new ApiV1NoteComputePostRequest(); // ApiV1NoteComputePostRequest | 
    try {
      ApiV1InvoiceComputePost200Response result = apiInstance.apiV1NoteComputePost(apiV1NoteComputePostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NoteApi#apiV1NoteComputePost");
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
| **apiV1NoteComputePostRequest** | [**ApiV1NoteComputePostRequest**](ApiV1NoteComputePostRequest.md)|  | |

### Return type

[**ApiV1InvoiceComputePost200Response**](ApiV1InvoiceComputePost200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

<a id="apiV1NoteIdCdrGet"></a>
# **apiV1NoteIdCdrGet**
> apiV1NoteIdCdrGet(id)

Descargar CDR (constancia de SUNAT)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.NoteApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    NoteApi apiInstance = new NoteApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1NoteIdCdrGet(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling NoteApi#apiV1NoteIdCdrGet");
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

<a id="apiV1NoteIdPdfGet"></a>
# **apiV1NoteIdPdfGet**
> apiV1NoteIdPdfGet(id)

Obtener PDF de la nota

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.NoteApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    NoteApi apiInstance = new NoteApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1NoteIdPdfGet(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling NoteApi#apiV1NoteIdPdfGet");
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

<a id="apiV1NoteIdXmlGet"></a>
# **apiV1NoteIdXmlGet**
> apiV1NoteIdXmlGet(id)

Descargar XML firmado

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.NoteApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    NoteApi apiInstance = new NoteApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1NoteIdXmlGet(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling NoteApi#apiV1NoteIdXmlGet");
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

<a id="apiV1NoteSendPost"></a>
# **apiV1NoteSendPost**
> ApiV1NoteSendPost202Response apiV1NoteSendPost(apiV1NoteSendPostRequest)

Enviar nota de crédito (07) o débito (08) a SUNAT

Genera XML UBL 2.1, firma y encola. Responde 202. Consultar GET /documents/{id} para el resultado final. Idempotente por (RUC emisor, tipoDoc, serie, correlativo): reenviar el mismo comprobante NO lo duplica. Si ya fue aceptado devuelve el mismo id y hash sin reenviar nada a SUNAT; si sigue en proceso responde 409 (esperá el resultado, no cambies el correlativo). Solo un RECHAZADO exige un correlativo nuevo.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.NoteApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    NoteApi apiInstance = new NoteApi(defaultClient);
    ApiV1NoteSendPostRequest apiV1NoteSendPostRequest = new ApiV1NoteSendPostRequest(); // ApiV1NoteSendPostRequest | 
    try {
      ApiV1NoteSendPost202Response result = apiInstance.apiV1NoteSendPost(apiV1NoteSendPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NoteApi#apiV1NoteSendPost");
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
| **apiV1NoteSendPostRequest** | [**ApiV1NoteSendPostRequest**](ApiV1NoteSendPostRequest.md)|  | |

### Return type

[**ApiV1NoteSendPost202Response**](ApiV1NoteSendPost202Response.md)

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
| **409** | Default Response |  -  |

