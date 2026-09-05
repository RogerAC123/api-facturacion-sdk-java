# DespatchApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getDespatchCdr**](DespatchApi.md#getDespatchCdr) | **GET** /api/v1/despatch/{id}/cdr | Descargar CDR (constancia de SUNAT) |
| [**getDespatchPdf**](DespatchApi.md#getDespatchPdf) | **GET** /api/v1/despatch/{id}/pdf | Obtener PDF de la guía (A4 oficina, ticket 80mm o 58mm POS) |
| [**getDespatchXml**](DespatchApi.md#getDespatchXml) | **GET** /api/v1/despatch/{id}/xml | Descargar XML firmado de la guía |
| [**sendDespatch**](DespatchApi.md#sendDespatch) | **POST** /api/v1/despatch/send | Enviar guía de remisión (09) via API GRE REST |
| [**sendDespatchMulti**](DespatchApi.md#sendDespatchMulti) | **POST** /api/v1/despatch/send-multi | Enviar múltiples guías de remisión por destino |
| [**sendDespatchTransportista**](DespatchApi.md#sendDespatchTransportista) | **POST** /api/v1/despatch-transportista/send | Enviar guía de remisión TRANSPORTISTA (31) via API GRE REST |


<a id="getDespatchCdr"></a>
# **getDespatchCdr**
> getDespatchCdr(id)

Descargar CDR (constancia de SUNAT)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DespatchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    DespatchApi apiInstance = new DespatchApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.getDespatchCdr(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DespatchApi#getDespatchCdr");
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

<a id="getDespatchPdf"></a>
# **getDespatchPdf**
> getDespatchPdf(id, format)

Obtener PDF de la guía (A4 oficina, ticket 80mm o 58mm POS)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DespatchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    DespatchApi apiInstance = new DespatchApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    String format = "a4"; // String | 
    try {
      apiInstance.getDespatchPdf(id, format);
    } catch (ApiException e) {
      System.err.println("Exception when calling DespatchApi#getDespatchPdf");
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

<a id="getDespatchXml"></a>
# **getDespatchXml**
> getDespatchXml(id)

Descargar XML firmado de la guía

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DespatchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    DespatchApi apiInstance = new DespatchApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.getDespatchXml(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DespatchApi#getDespatchXml");
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

<a id="sendDespatch"></a>
# **sendDespatch**
> SendInvoice202Response sendDespatch(sendDespatchRequest)

Enviar guía de remisión (09) via API GRE REST

Genera XML UBL 2.1, firma y encola. El worker obtiene token OAuth2, envía a SUNAT GRE, guarda ticket y luego hace polling de getStatus. Idempotente por (RUC emisor, tipoDoc, serie, correlativo): reenviar el mismo comprobante NO lo duplica. Si ya fue aceptado devuelve el mismo id y hash sin reenviar nada a SUNAT; si sigue en proceso responde 409 (esperá el resultado, no cambies el correlativo). Solo un RECHAZADO exige un correlativo nuevo.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DespatchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    DespatchApi apiInstance = new DespatchApi(defaultClient);
    SendDespatchRequest sendDespatchRequest = new SendDespatchRequest(); // SendDespatchRequest | 
    try {
      SendInvoice202Response result = apiInstance.sendDespatch(sendDespatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DespatchApi#sendDespatch");
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
| **sendDespatchRequest** | [**SendDespatchRequest**](SendDespatchRequest.md)|  | |

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

<a id="sendDespatchMulti"></a>
# **sendDespatchMulti**
> SendDespatchMulti202Response sendDespatchMulti(sendDespatchMultiRequest)

Enviar múltiples guías de remisión por destino

Recibe datos comunes de transporte + array de destinos. Genera una guía por cada destino con correlativo auto-asignado. Cada guía se encola independientemente para envío a SUNAT GRE.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DespatchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    DespatchApi apiInstance = new DespatchApi(defaultClient);
    SendDespatchMultiRequest sendDespatchMultiRequest = new SendDespatchMultiRequest(); // SendDespatchMultiRequest | 
    try {
      SendDespatchMulti202Response result = apiInstance.sendDespatchMulti(sendDespatchMultiRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DespatchApi#sendDespatchMulti");
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
| **sendDespatchMultiRequest** | [**SendDespatchMultiRequest**](SendDespatchMultiRequest.md)|  | |

### Return type

[**SendDespatchMulti202Response**](SendDespatchMulti202Response.md)

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

<a id="sendDespatchTransportista"></a>
# **sendDespatchTransportista**
> SendInvoice202Response sendDespatchTransportista(sendDespatchTransportistaRequest)

Enviar guía de remisión TRANSPORTISTA (31) via API GRE REST

Guía emitida por la empresa de transporte (emisor&#x3D;transportista). Incluye remitente (dueño de los bienes) y destinatario. Genera XML UBL 2.1, firma y encola para envío a SUNAT GRE.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DespatchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    DespatchApi apiInstance = new DespatchApi(defaultClient);
    SendDespatchTransportistaRequest sendDespatchTransportistaRequest = new SendDespatchTransportistaRequest(); // SendDespatchTransportistaRequest | 
    try {
      SendInvoice202Response result = apiInstance.sendDespatchTransportista(sendDespatchTransportistaRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DespatchApi#sendDespatchTransportista");
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
| **sendDespatchTransportistaRequest** | [**SendDespatchTransportistaRequest**](SendDespatchTransportistaRequest.md)|  | |

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

