# InvoiceApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiV1InvoiceComputePost**](InvoiceApi.md#apiV1InvoiceComputePost) | **POST** /api/v1/invoice/compute | Calcular importes (IGV, descuentos, totales) sin emitir |
| [**apiV1InvoiceIdCdrGet**](InvoiceApi.md#apiV1InvoiceIdCdrGet) | **GET** /api/v1/invoice/{id}/cdr | Descargar CDR (constancia de SUNAT) |
| [**apiV1InvoiceIdPdfGet**](InvoiceApi.md#apiV1InvoiceIdPdfGet) | **GET** /api/v1/invoice/{id}/pdf | Obtener PDF (A4 oficina, ticket 80mm o ticket 58mm POS) |
| [**apiV1InvoiceIdXmlGet**](InvoiceApi.md#apiV1InvoiceIdXmlGet) | **GET** /api/v1/invoice/{id}/xml | Descargar XML firmado |
| [**apiV1InvoiceSendPost**](InvoiceApi.md#apiV1InvoiceSendPost) | **POST** /api/v1/invoice/send | Enviar factura (01) o boleta (03) a SUNAT |


<a id="apiV1InvoiceComputePost"></a>
# **apiV1InvoiceComputePost**
> ApiV1InvoiceComputePost200Response apiV1InvoiceComputePost(apiV1InvoiceComputePostRequest)

Calcular importes (IGV, descuentos, totales) sin emitir

Motor de cálculo: recibe ítems crudos (cantidad, valorUnitario sin IGV, afectación, descuento) y un descuento global opcional, y devuelve TODOS los importes fiscales calculados (bases, IGV, descuentos, totales, monto en letras). No emite ni persiste nada — úsalo para previsualizar o para alimentar POST /invoice/send.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.InvoiceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    InvoiceApi apiInstance = new InvoiceApi(defaultClient);
    ApiV1InvoiceComputePostRequest apiV1InvoiceComputePostRequest = new ApiV1InvoiceComputePostRequest(); // ApiV1InvoiceComputePostRequest | 
    try {
      ApiV1InvoiceComputePost200Response result = apiInstance.apiV1InvoiceComputePost(apiV1InvoiceComputePostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceApi#apiV1InvoiceComputePost");
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
| **apiV1InvoiceComputePostRequest** | [**ApiV1InvoiceComputePostRequest**](ApiV1InvoiceComputePostRequest.md)|  | |

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

<a id="apiV1InvoiceIdCdrGet"></a>
# **apiV1InvoiceIdCdrGet**
> apiV1InvoiceIdCdrGet(id)

Descargar CDR (constancia de SUNAT)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.InvoiceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    InvoiceApi apiInstance = new InvoiceApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1InvoiceIdCdrGet(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceApi#apiV1InvoiceIdCdrGet");
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

<a id="apiV1InvoiceIdPdfGet"></a>
# **apiV1InvoiceIdPdfGet**
> apiV1InvoiceIdPdfGet(id, format)

Obtener PDF (A4 oficina, ticket 80mm o ticket 58mm POS)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.InvoiceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    InvoiceApi apiInstance = new InvoiceApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    String format = "a4"; // String | 
    try {
      apiInstance.apiV1InvoiceIdPdfGet(id, format);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceApi#apiV1InvoiceIdPdfGet");
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
| **format** | **String**|  | [optional] [default to a4] [enum: a4, ticket, ticket80, ticket58] |

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

<a id="apiV1InvoiceIdXmlGet"></a>
# **apiV1InvoiceIdXmlGet**
> apiV1InvoiceIdXmlGet(id)

Descargar XML firmado

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.InvoiceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    InvoiceApi apiInstance = new InvoiceApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1InvoiceIdXmlGet(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceApi#apiV1InvoiceIdXmlGet");
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

<a id="apiV1InvoiceSendPost"></a>
# **apiV1InvoiceSendPost**
> ApiV1InvoiceSendPost202Response apiV1InvoiceSendPost(apiV1InvoiceSendPostRequest)

Enviar factura (01) o boleta (03) a SUNAT

Genera el XML UBL 2.1, lo firma digitalmente y lo encola para envío asíncrono a SUNAT. Responde 202 inmediatamente. Para conocer el resultado final consultar GET /documents/{id}. Idempotente por (RUC emisor, tipoDoc, serie, correlativo): reenviar el mismo comprobante NO lo duplica. Si ya fue aceptado devuelve el mismo id y hash sin reenviar nada a SUNAT; si sigue en proceso responde 409 (esperá el resultado, no cambies el correlativo). Solo un RECHAZADO exige un correlativo nuevo.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.InvoiceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    InvoiceApi apiInstance = new InvoiceApi(defaultClient);
    ApiV1InvoiceSendPostRequest apiV1InvoiceSendPostRequest = new ApiV1InvoiceSendPostRequest(); // ApiV1InvoiceSendPostRequest | 
    try {
      ApiV1InvoiceSendPost202Response result = apiInstance.apiV1InvoiceSendPost(apiV1InvoiceSendPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceApi#apiV1InvoiceSendPost");
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
| **apiV1InvoiceSendPostRequest** | [**ApiV1InvoiceSendPostRequest**](ApiV1InvoiceSendPostRequest.md)|  | |

### Return type

[**ApiV1InvoiceSendPost202Response**](ApiV1InvoiceSendPost202Response.md)

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

