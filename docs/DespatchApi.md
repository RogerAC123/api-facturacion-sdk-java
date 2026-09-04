# DespatchApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiV1DespatchIdCdrGet**](DespatchApi.md#apiV1DespatchIdCdrGet) | **GET** /api/v1/despatch/{id}/cdr | Descargar CDR (constancia de SUNAT) |
| [**apiV1DespatchIdPdfGet**](DespatchApi.md#apiV1DespatchIdPdfGet) | **GET** /api/v1/despatch/{id}/pdf | Obtener PDF de la guía (A4 oficina, ticket 80mm o 58mm POS) |
| [**apiV1DespatchIdXmlGet**](DespatchApi.md#apiV1DespatchIdXmlGet) | **GET** /api/v1/despatch/{id}/xml | Descargar XML firmado de la guía |
| [**apiV1DespatchSendMultiPost**](DespatchApi.md#apiV1DespatchSendMultiPost) | **POST** /api/v1/despatch/send-multi | Enviar múltiples guías de remisión por destino |
| [**apiV1DespatchSendPost**](DespatchApi.md#apiV1DespatchSendPost) | **POST** /api/v1/despatch/send | Enviar guía de remisión (09) via API GRE REST |
| [**apiV1DespatchTransportistaSendPost**](DespatchApi.md#apiV1DespatchTransportistaSendPost) | **POST** /api/v1/despatch-transportista/send | Enviar guía de remisión TRANSPORTISTA (31) via API GRE REST |


<a id="apiV1DespatchIdCdrGet"></a>
# **apiV1DespatchIdCdrGet**
> apiV1DespatchIdCdrGet(id)

Descargar CDR (constancia de SUNAT)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DespatchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    DespatchApi apiInstance = new DespatchApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1DespatchIdCdrGet(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DespatchApi#apiV1DespatchIdCdrGet");
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

<a id="apiV1DespatchIdPdfGet"></a>
# **apiV1DespatchIdPdfGet**
> apiV1DespatchIdPdfGet(id, format)

Obtener PDF de la guía (A4 oficina, ticket 80mm o 58mm POS)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DespatchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    DespatchApi apiInstance = new DespatchApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    String format = "a4"; // String | 
    try {
      apiInstance.apiV1DespatchIdPdfGet(id, format);
    } catch (ApiException e) {
      System.err.println("Exception when calling DespatchApi#apiV1DespatchIdPdfGet");
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

<a id="apiV1DespatchIdXmlGet"></a>
# **apiV1DespatchIdXmlGet**
> apiV1DespatchIdXmlGet(id)

Descargar XML firmado de la guía

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DespatchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    DespatchApi apiInstance = new DespatchApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1DespatchIdXmlGet(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DespatchApi#apiV1DespatchIdXmlGet");
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

<a id="apiV1DespatchSendMultiPost"></a>
# **apiV1DespatchSendMultiPost**
> ApiV1DespatchSendMultiPost202Response apiV1DespatchSendMultiPost(apiV1DespatchSendMultiPostRequest)

Enviar múltiples guías de remisión por destino

Recibe datos comunes de transporte + array de destinos. Genera una guía por cada destino con correlativo auto-asignado. Cada guía se encola independientemente para envío a SUNAT GRE.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DespatchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    DespatchApi apiInstance = new DespatchApi(defaultClient);
    ApiV1DespatchSendMultiPostRequest apiV1DespatchSendMultiPostRequest = new ApiV1DespatchSendMultiPostRequest(); // ApiV1DespatchSendMultiPostRequest | 
    try {
      ApiV1DespatchSendMultiPost202Response result = apiInstance.apiV1DespatchSendMultiPost(apiV1DespatchSendMultiPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DespatchApi#apiV1DespatchSendMultiPost");
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
| **apiV1DespatchSendMultiPostRequest** | [**ApiV1DespatchSendMultiPostRequest**](ApiV1DespatchSendMultiPostRequest.md)|  | |

### Return type

[**ApiV1DespatchSendMultiPost202Response**](ApiV1DespatchSendMultiPost202Response.md)

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

<a id="apiV1DespatchSendPost"></a>
# **apiV1DespatchSendPost**
> ApiV1NoteSendPost202Response apiV1DespatchSendPost(apiV1DespatchSendPostRequest)

Enviar guía de remisión (09) via API GRE REST

Genera XML UBL 2.1, firma y encola. El worker obtiene token OAuth2, envía a SUNAT GRE, guarda ticket y luego hace polling de getStatus. Idempotente por (RUC emisor, tipoDoc, serie, correlativo): reenviar el mismo comprobante NO lo duplica. Si ya fue aceptado devuelve el mismo id y hash sin reenviar nada a SUNAT; si sigue en proceso responde 409 (esperá el resultado, no cambies el correlativo). Solo un RECHAZADO exige un correlativo nuevo.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DespatchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    DespatchApi apiInstance = new DespatchApi(defaultClient);
    ApiV1DespatchSendPostRequest apiV1DespatchSendPostRequest = new ApiV1DespatchSendPostRequest(); // ApiV1DespatchSendPostRequest | 
    try {
      ApiV1NoteSendPost202Response result = apiInstance.apiV1DespatchSendPost(apiV1DespatchSendPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DespatchApi#apiV1DespatchSendPost");
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
| **apiV1DespatchSendPostRequest** | [**ApiV1DespatchSendPostRequest**](ApiV1DespatchSendPostRequest.md)|  | |

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

<a id="apiV1DespatchTransportistaSendPost"></a>
# **apiV1DespatchTransportistaSendPost**
> ApiV1NoteSendPost202Response apiV1DespatchTransportistaSendPost(apiV1DespatchTransportistaSendPostRequest)

Enviar guía de remisión TRANSPORTISTA (31) via API GRE REST

Guía emitida por la empresa de transporte (emisor&#x3D;transportista). Incluye remitente (dueño de los bienes) y destinatario. Genera XML UBL 2.1, firma y encola para envío a SUNAT GRE.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DespatchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    DespatchApi apiInstance = new DespatchApi(defaultClient);
    ApiV1DespatchTransportistaSendPostRequest apiV1DespatchTransportistaSendPostRequest = new ApiV1DespatchTransportistaSendPostRequest(); // ApiV1DespatchTransportistaSendPostRequest | 
    try {
      ApiV1NoteSendPost202Response result = apiInstance.apiV1DespatchTransportistaSendPost(apiV1DespatchTransportistaSendPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DespatchApi#apiV1DespatchTransportistaSendPost");
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
| **apiV1DespatchTransportistaSendPostRequest** | [**ApiV1DespatchTransportistaSendPostRequest**](ApiV1DespatchTransportistaSendPostRequest.md)|  | |

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

