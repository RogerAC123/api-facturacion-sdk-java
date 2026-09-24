# InvoiceApi

All URIs are relative to *http://localhost:3099*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**computeInvoice**](InvoiceApi.md#computeInvoice) | **POST** /api/v1/invoice/compute | Calcular importes (IGV, descuentos, totales) sin emitir |
| [**getInvoiceCdr**](InvoiceApi.md#getInvoiceCdr) | **GET** /api/v1/invoice/{id}/cdr | Descargar CDR (constancia de SUNAT) |
| [**getInvoicePdf**](InvoiceApi.md#getInvoicePdf) | **GET** /api/v1/invoice/{id}/pdf | Obtener PDF (A4 oficina, ticket 80mm o ticket 58mm POS) |
| [**getInvoiceXml**](InvoiceApi.md#getInvoiceXml) | **GET** /api/v1/invoice/{id}/xml | Descargar XML firmado |
| [**sendInvoice**](InvoiceApi.md#sendInvoice) | **POST** /api/v1/invoice/send | Enviar factura (01) o boleta (03) a SUNAT |


<a id="computeInvoice"></a>
# **computeInvoice**
> ComputeInvoice200Response computeInvoice(computeInvoiceRequest)

Calcular importes (IGV, descuentos, totales) sin emitir

Motor de cálculo: recibe ítems crudos (cantidad, valorUnitario sin IGV, afectación, descuento) y un descuento global opcional, y devuelve TODOS los importes fiscales calculados (bases, IGV, descuentos, totales, monto en letras). No emite ni persiste nada — úsalo para previsualizar o para alimentar POST /invoice/send.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.InvoiceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    InvoiceApi apiInstance = new InvoiceApi(defaultClient);
    ComputeInvoiceRequest computeInvoiceRequest = new ComputeInvoiceRequest(); // ComputeInvoiceRequest | 
    try {
      ComputeInvoice200Response result = apiInstance.computeInvoice(computeInvoiceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceApi#computeInvoice");
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

<a id="getInvoiceCdr"></a>
# **getInvoiceCdr**
> getInvoiceCdr(id)

Descargar CDR (constancia de SUNAT)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.InvoiceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    InvoiceApi apiInstance = new InvoiceApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.getInvoiceCdr(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceApi#getInvoiceCdr");
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

<a id="getInvoicePdf"></a>
# **getInvoicePdf**
> getInvoicePdf(id, format)

Obtener PDF (A4 oficina, ticket 80mm o ticket 58mm POS)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.InvoiceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    InvoiceApi apiInstance = new InvoiceApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    String format = "a4"; // String | 
    try {
      apiInstance.getInvoicePdf(id, format);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceApi#getInvoicePdf");
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

<a id="getInvoiceXml"></a>
# **getInvoiceXml**
> getInvoiceXml(id)

Descargar XML firmado

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.InvoiceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    InvoiceApi apiInstance = new InvoiceApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.getInvoiceXml(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceApi#getInvoiceXml");
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

<a id="sendInvoice"></a>
# **sendInvoice**
> SendInvoice202Response sendInvoice(sendInvoiceRequest)

Enviar factura (01) o boleta (03) a SUNAT

Genera el XML UBL 2.1, lo firma digitalmente y lo encola para envío asíncrono a SUNAT. Responde 202 inmediatamente. Para conocer el resultado final consultar GET /documents/{id}. Idempotente por (RUC emisor, tipoDoc, serie, correlativo): reenviar el mismo comprobante NO lo duplica. Si ya fue aceptado devuelve el mismo id y hash sin reenviar nada a SUNAT; si sigue en proceso responde 409 (esperá el resultado, no cambies el correlativo). Solo un RECHAZADO exige un correlativo nuevo.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.InvoiceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    InvoiceApi apiInstance = new InvoiceApi(defaultClient);
    SendInvoiceRequest sendInvoiceRequest = new SendInvoiceRequest(); // SendInvoiceRequest | 
    try {
      SendInvoice202Response result = apiInstance.sendInvoice(sendInvoiceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceApi#sendInvoice");
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
| **sendInvoiceRequest** | [**SendInvoiceRequest**](SendInvoiceRequest.md)|  | |

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

