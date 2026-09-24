# DocumentsApi

All URIs are relative to *http://localhost:3099*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**consultarCdr**](DocumentsApi.md#consultarCdr) | **POST** /api/v1/cdr/consultar | Consultar el CDR de un comprobante en SUNAT por referencia |
| [**getDocument**](DocumentsApi.md#getDocument) | **GET** /api/v1/documents/{id} | Detalle completo de un documento |
| [**getNextCorrelativo**](DocumentsApi.md#getNextCorrelativo) | **GET** /api/v1/documents/next-correlativo | Obtener el siguiente correlativo disponible para una serie |
| [**listDocuments**](DocumentsApi.md#listDocuments) | **GET** /api/v1/documents | Listar documentos con filtros y paginación |
| [**reconcileDocument**](DocumentsApi.md#reconcileDocument) | **POST** /api/v1/documents/{id}/recover | Reconciliar un documento con SUNAT (consulta de CDR, solo master) |
| [**retryDocument**](DocumentsApi.md#retryDocument) | **POST** /api/v1/documents/{id}/retry | Re-encolar un documento fallido |


<a id="consultarCdr"></a>
# **consultarCdr**
> ConsultarCdr200Response consultarCdr(consultarCdrRequest)

Consultar el CDR de un comprobante en SUNAT por referencia

Recupera el CDR oficial (billConsultService / getStatusCdr) de un comprobante 01/03/07/08 por RUC+serie+número, aunque no exista en esta BD. Útil para recuperar el histórico emitido por otro PSE. Solo en producción; usa la Clave SOL de la empresa (debe existir y estar en scope de la API key).

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    ConsultarCdrRequest consultarCdrRequest = new ConsultarCdrRequest(); // ConsultarCdrRequest | 
    try {
      ConsultarCdr200Response result = apiInstance.consultarCdr(consultarCdrRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#consultarCdr");
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
| **consultarCdrRequest** | [**ConsultarCdrRequest**](ConsultarCdrRequest.md)|  | |

### Return type

[**ConsultarCdr200Response**](ConsultarCdr200Response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |
| **429** | Default Response |  -  |

<a id="getDocument"></a>
# **getDocument**
> getDocument(id)

Detalle completo de un documento

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.getDocument(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#getDocument");
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

<a id="getNextCorrelativo"></a>
# **getNextCorrelativo**
> GetNextCorrelativo200Response getNextCorrelativo(companyRuc, tipoDoc, serie)

Obtener el siguiente correlativo disponible para una serie

Busca el correlativo más alto existente para la combinación empresa+tipoDoc+serie y retorna el siguiente. Útil para auto-numeración.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    String companyRuc = "companyRuc_example"; // String | 
    String tipoDoc = "tipoDoc_example"; // String | 
    String serie = "serie_example"; // String | 
    try {
      GetNextCorrelativo200Response result = apiInstance.getNextCorrelativo(companyRuc, tipoDoc, serie);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#getNextCorrelativo");
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
| **companyRuc** | **String**|  | |
| **tipoDoc** | **String**|  | |
| **serie** | **String**|  | |

### Return type

[**GetNextCorrelativo200Response**](GetNextCorrelativo200Response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |
| **429** | Default Response |  -  |

<a id="listDocuments"></a>
# **listDocuments**
> ListDocuments200Response listDocuments(ruc, tenantId, tipoDoc, serie, correlativo, estado, env, fechaDesde, fechaHasta, clienteNumDoc, page, limit)

Listar documentos con filtros y paginación

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    String ruc = "ruc_example"; // String | 
    UUID tenantId = UUID.randomUUID(); // UUID | 
    String tipoDoc = "tipoDoc_example"; // String | 
    String serie = "serie_example"; // String | 
    String correlativo = "correlativo_example"; // String | 
    String estado = "estado_example"; // String | 
    String env = "live"; // String | 
    String fechaDesde = "fechaDesde_example"; // String | 
    String fechaHasta = "fechaHasta_example"; // String | 
    String clienteNumDoc = "clienteNumDoc_example"; // String | 
    Integer page = 1; // Integer | 
    Integer limit = 20; // Integer | 
    try {
      ListDocuments200Response result = apiInstance.listDocuments(ruc, tenantId, tipoDoc, serie, correlativo, estado, env, fechaDesde, fechaHasta, clienteNumDoc, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#listDocuments");
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
| **ruc** | **String**|  | [optional] |
| **tenantId** | **UUID**|  | [optional] |
| **tipoDoc** | **String**|  | [optional] |
| **serie** | **String**|  | [optional] |
| **correlativo** | **String**|  | [optional] |
| **estado** | **String**|  | [optional] |
| **env** | **String**|  | [optional] [enum: live, test] |
| **fechaDesde** | **String**|  | [optional] |
| **fechaHasta** | **String**|  | [optional] |
| **clienteNumDoc** | **String**|  | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **limit** | **Integer**|  | [optional] [default to 20] |

### Return type

[**ListDocuments200Response**](ListDocuments200Response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **429** | Default Response |  -  |

<a id="reconcileDocument"></a>
# **reconcileDocument**
> ReconcileDocument200Response reconcileDocument(id)

Reconciliar un documento con SUNAT (consulta de CDR, solo master)

Consulta el estado REAL en SUNAT (getStatusCdr / billConsultService) SIN reenviar y corrige la BD. Útil cuando un documento quedó desincronizado (ej. una boleta ACEPTADA figurando RECHAZADO/COLA_FALLIDA/ENCOLADO). Solo comprobantes 01/03/07/08, solo en producción. Restringido al master API key.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      ReconcileDocument200Response result = apiInstance.reconcileDocument(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#reconcileDocument");
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

[**ReconcileDocument200Response**](ReconcileDocument200Response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |
| **429** | Default Response |  -  |

<a id="retryDocument"></a>
# **retryDocument**
> RetryDocument202Response retryDocument(id)

Re-encolar un documento fallido

Útil cuando un documento quedó en estado COLA_FALLIDA tras agotar los reintentos automáticos.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3099");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      RetryDocument202Response result = apiInstance.retryDocument(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#retryDocument");
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

[**RetryDocument202Response**](RetryDocument202Response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Default Response |  -  |
| **400** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **429** | Default Response |  -  |

