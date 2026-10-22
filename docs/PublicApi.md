# PublicApi

All URIs are relative to *https://api-facturacion.intifact.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**consultarComprobante**](PublicApi.md#consultarComprobante) | **GET** /api/v1/public/consultar/{ruc}/{tipoDoc}/{serie}/{numero} | Consultar un comprobante (público, sin auth) |
| [**consultarComprobantePdf**](PublicApi.md#consultarComprobantePdf) | **GET** /api/v1/public/consultar/{ruc}/{tipoDoc}/{serie}/{numero}/pdf | Descargar PDF del comprobante (público) |
| [**consultarComprobanteXml**](PublicApi.md#consultarComprobanteXml) | **GET** /api/v1/public/consultar/{ruc}/{tipoDoc}/{serie}/{numero}/xml | Descargar XML firmado (público) |


<a id="consultarComprobante"></a>
# **consultarComprobante**
> consultarComprobante(ruc, tipoDoc, serie, numero, total, fecha, receptor)

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
    defaultClient.setBasePath("https://api-facturacion.intifact.com");

    PublicApi apiInstance = new PublicApi(defaultClient);
    String ruc = "ruc_example"; // String | 
    String tipoDoc = "tipoDoc_example"; // String | 
    String serie = "serie_example"; // String | 
    String numero = "numero_example"; // String | 
    BigDecimal total = new BigDecimal(78); // BigDecimal | 
    String fecha = "fecha_example"; // String | 
    String receptor = "receptor_example"; // String | 
    try {
      apiInstance.consultarComprobante(ruc, tipoDoc, serie, numero, total, fecha, receptor);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicApi#consultarComprobante");
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

<a id="consultarComprobantePdf"></a>
# **consultarComprobantePdf**
> consultarComprobantePdf(ruc, tipoDoc, serie, numero, total, fecha, receptor)

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
    defaultClient.setBasePath("https://api-facturacion.intifact.com");

    PublicApi apiInstance = new PublicApi(defaultClient);
    String ruc = "ruc_example"; // String | 
    String tipoDoc = "tipoDoc_example"; // String | 
    String serie = "serie_example"; // String | 
    String numero = "numero_example"; // String | 
    BigDecimal total = new BigDecimal(78); // BigDecimal | 
    String fecha = "fecha_example"; // String | 
    String receptor = "receptor_example"; // String | 
    try {
      apiInstance.consultarComprobantePdf(ruc, tipoDoc, serie, numero, total, fecha, receptor);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicApi#consultarComprobantePdf");
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

<a id="consultarComprobanteXml"></a>
# **consultarComprobanteXml**
> consultarComprobanteXml(ruc, tipoDoc, serie, numero, total, fecha, receptor)

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
    defaultClient.setBasePath("https://api-facturacion.intifact.com");

    PublicApi apiInstance = new PublicApi(defaultClient);
    String ruc = "ruc_example"; // String | 
    String tipoDoc = "tipoDoc_example"; // String | 
    String serie = "serie_example"; // String | 
    String numero = "numero_example"; // String | 
    BigDecimal total = new BigDecimal(78); // BigDecimal | 
    String fecha = "fecha_example"; // String | 
    String receptor = "receptor_example"; // String | 
    try {
      apiInstance.consultarComprobanteXml(ruc, tipoDoc, serie, numero, total, fecha, receptor);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicApi#consultarComprobanteXml");
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

