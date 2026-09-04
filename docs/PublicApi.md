# PublicApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiV1PublicConsultarRucTipoDocSerieNumeroGet**](PublicApi.md#apiV1PublicConsultarRucTipoDocSerieNumeroGet) | **GET** /api/v1/public/consultar/{ruc}/{tipoDoc}/{serie}/{numero} | Consultar un comprobante (público, sin auth) |
| [**apiV1PublicConsultarRucTipoDocSerieNumeroPdfGet**](PublicApi.md#apiV1PublicConsultarRucTipoDocSerieNumeroPdfGet) | **GET** /api/v1/public/consultar/{ruc}/{tipoDoc}/{serie}/{numero}/pdf | Descargar PDF del comprobante (público) |
| [**apiV1PublicConsultarRucTipoDocSerieNumeroXmlGet**](PublicApi.md#apiV1PublicConsultarRucTipoDocSerieNumeroXmlGet) | **GET** /api/v1/public/consultar/{ruc}/{tipoDoc}/{serie}/{numero}/xml | Descargar XML firmado (público) |


<a id="apiV1PublicConsultarRucTipoDocSerieNumeroGet"></a>
# **apiV1PublicConsultarRucTipoDocSerieNumeroGet**
> apiV1PublicConsultarRucTipoDocSerieNumeroGet(ruc, tipoDoc, serie, numero, total, fecha, receptor)

Consultar un comprobante (público, sin auth)

Verificación pública de un comprobante emitido. Retorna datos mínimos no sensibles. El parámetro &#x60;total&#x60; es opcional pero recomendado como anti-scraping (debe coincidir con el monto total).

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.PublicApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    PublicApi apiInstance = new PublicApi(defaultClient);
    String ruc = "ruc_example"; // String | 
    String tipoDoc = "tipoDoc_example"; // String | 
    String serie = "serie_example"; // String | 
    String numero = "numero_example"; // String | 
    BigDecimal total = new BigDecimal(78); // BigDecimal | 
    String fecha = "fecha_example"; // String | 
    String receptor = "receptor_example"; // String | 
    try {
      apiInstance.apiV1PublicConsultarRucTipoDocSerieNumeroGet(ruc, tipoDoc, serie, numero, total, fecha, receptor);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicApi#apiV1PublicConsultarRucTipoDocSerieNumeroGet");
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
| **tipoDoc** | **String**|  | |
| **serie** | **String**|  | |
| **numero** | **String**|  | |
| **total** | **BigDecimal**|  | [optional] |
| **fecha** | **String**|  | [optional] |
| **receptor** | **String**|  | [optional] |

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

<a id="apiV1PublicConsultarRucTipoDocSerieNumeroPdfGet"></a>
# **apiV1PublicConsultarRucTipoDocSerieNumeroPdfGet**
> apiV1PublicConsultarRucTipoDocSerieNumeroPdfGet(ruc, tipoDoc, serie, numero)

Descargar PDF del comprobante (público)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.PublicApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    PublicApi apiInstance = new PublicApi(defaultClient);
    String ruc = "ruc_example"; // String | 
    String tipoDoc = "tipoDoc_example"; // String | 
    String serie = "serie_example"; // String | 
    String numero = "numero_example"; // String | 
    try {
      apiInstance.apiV1PublicConsultarRucTipoDocSerieNumeroPdfGet(ruc, tipoDoc, serie, numero);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicApi#apiV1PublicConsultarRucTipoDocSerieNumeroPdfGet");
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
| **tipoDoc** | **String**|  | |
| **serie** | **String**|  | |
| **numero** | **String**|  | |

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

<a id="apiV1PublicConsultarRucTipoDocSerieNumeroXmlGet"></a>
# **apiV1PublicConsultarRucTipoDocSerieNumeroXmlGet**
> apiV1PublicConsultarRucTipoDocSerieNumeroXmlGet(ruc, tipoDoc, serie, numero)

Descargar XML firmado (público)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.PublicApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    PublicApi apiInstance = new PublicApi(defaultClient);
    String ruc = "ruc_example"; // String | 
    String tipoDoc = "tipoDoc_example"; // String | 
    String serie = "serie_example"; // String | 
    String numero = "numero_example"; // String | 
    try {
      apiInstance.apiV1PublicConsultarRucTipoDocSerieNumeroXmlGet(ruc, tipoDoc, serie, numero);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicApi#apiV1PublicConsultarRucTipoDocSerieNumeroXmlGet");
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
| **tipoDoc** | **String**|  | |
| **serie** | **String**|  | |
| **numero** | **String**|  | |

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

