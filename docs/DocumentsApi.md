# DocumentsApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiV1CdrConsultarPost**](DocumentsApi.md#apiV1CdrConsultarPost) | **POST** /api/v1/cdr/consultar | Consultar el CDR de un comprobante en SUNAT por referencia |
| [**apiV1DocumentsGet**](DocumentsApi.md#apiV1DocumentsGet) | **GET** /api/v1/documents | Listar documentos con filtros y paginación |
| [**apiV1DocumentsIdGet**](DocumentsApi.md#apiV1DocumentsIdGet) | **GET** /api/v1/documents/{id} | Detalle completo de un documento |
| [**apiV1DocumentsIdRecoverPost**](DocumentsApi.md#apiV1DocumentsIdRecoverPost) | **POST** /api/v1/documents/{id}/recover | Reconciliar un documento con SUNAT (consulta de CDR, solo master) |
| [**apiV1DocumentsIdRetryPost**](DocumentsApi.md#apiV1DocumentsIdRetryPost) | **POST** /api/v1/documents/{id}/retry | Re-encolar un documento fallido |
| [**apiV1DocumentsNextCorrelativoGet**](DocumentsApi.md#apiV1DocumentsNextCorrelativoGet) | **GET** /api/v1/documents/next-correlativo | Obtener el siguiente correlativo disponible para una serie |


<a id="apiV1CdrConsultarPost"></a>
# **apiV1CdrConsultarPost**
> ApiV1CdrConsultarPost200Response apiV1CdrConsultarPost(apiV1CdrConsultarPostRequest)

Consultar el CDR de un comprobante en SUNAT por referencia

Recupera el CDR oficial (billConsultService / getStatusCdr) de un comprobante 01/03/07/08 por RUC+serie+número, aunque no exista en esta BD. Útil para recuperar el histórico emitido por otro PSE. Solo en producción; usa la Clave SOL de la empresa (debe existir y estar en scope de la API key).

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    ApiV1CdrConsultarPostRequest apiV1CdrConsultarPostRequest = new ApiV1CdrConsultarPostRequest(); // ApiV1CdrConsultarPostRequest | 
    try {
      ApiV1CdrConsultarPost200Response result = apiInstance.apiV1CdrConsultarPost(apiV1CdrConsultarPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#apiV1CdrConsultarPost");
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
| **apiV1CdrConsultarPostRequest** | [**ApiV1CdrConsultarPostRequest**](ApiV1CdrConsultarPostRequest.md)|  | |

### Return type

[**ApiV1CdrConsultarPost200Response**](ApiV1CdrConsultarPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **404** | Default Response |  -  |

<a id="apiV1DocumentsGet"></a>
# **apiV1DocumentsGet**
> ApiV1DocumentsGet200Response apiV1DocumentsGet(ruc, tipoDoc, serie, estado, env, fechaDesde, fechaHasta, clienteNumDoc, page, limit)

Listar documentos con filtros y paginación

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    String ruc = "ruc_example"; // String | 
    String tipoDoc = "tipoDoc_example"; // String | 
    String serie = "serie_example"; // String | 
    String estado = "estado_example"; // String | 
    String env = "live"; // String | 
    String fechaDesde = "fechaDesde_example"; // String | 
    String fechaHasta = "fechaHasta_example"; // String | 
    String clienteNumDoc = "clienteNumDoc_example"; // String | 
    Integer page = 1; // Integer | 
    Integer limit = 20; // Integer | 
    try {
      ApiV1DocumentsGet200Response result = apiInstance.apiV1DocumentsGet(ruc, tipoDoc, serie, estado, env, fechaDesde, fechaHasta, clienteNumDoc, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#apiV1DocumentsGet");
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
| **tipoDoc** | **String**|  | [optional] |
| **serie** | **String**|  | [optional] |
| **estado** | **String**|  | [optional] |
| **env** | **String**|  | [optional] [enum: live, test] |
| **fechaDesde** | **String**|  | [optional] |
| **fechaHasta** | **String**|  | [optional] |
| **clienteNumDoc** | **String**|  | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **limit** | **Integer**|  | [optional] [default to 20] |

### Return type

[**ApiV1DocumentsGet200Response**](ApiV1DocumentsGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

<a id="apiV1DocumentsIdGet"></a>
# **apiV1DocumentsIdGet**
> apiV1DocumentsIdGet(id)

Detalle completo de un documento

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1DocumentsIdGet(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#apiV1DocumentsIdGet");
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

<a id="apiV1DocumentsIdRecoverPost"></a>
# **apiV1DocumentsIdRecoverPost**
> ApiV1DocumentsIdRecoverPost200Response apiV1DocumentsIdRecoverPost(id)

Reconciliar un documento con SUNAT (consulta de CDR, solo master)

Consulta el estado REAL en SUNAT (getStatusCdr / billConsultService) SIN reenviar y corrige la BD. Útil cuando un documento quedó desincronizado (ej. una boleta ACEPTADA figurando RECHAZADO/COLA_FALLIDA/ENCOLADO). Solo comprobantes 01/03/07/08, solo en producción. Restringido al master API key.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      ApiV1DocumentsIdRecoverPost200Response result = apiInstance.apiV1DocumentsIdRecoverPost(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#apiV1DocumentsIdRecoverPost");
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

[**ApiV1DocumentsIdRecoverPost200Response**](ApiV1DocumentsIdRecoverPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

<a id="apiV1DocumentsIdRetryPost"></a>
# **apiV1DocumentsIdRetryPost**
> ApiV1DocumentsIdRetryPost202Response apiV1DocumentsIdRetryPost(id)

Re-encolar un documento fallido

Útil cuando un documento quedó en estado COLA_FALLIDA tras agotar los reintentos automáticos.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      ApiV1DocumentsIdRetryPost202Response result = apiInstance.apiV1DocumentsIdRetryPost(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#apiV1DocumentsIdRetryPost");
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

[**ApiV1DocumentsIdRetryPost202Response**](ApiV1DocumentsIdRetryPost202Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Default Response |  -  |
| **400** | Default Response |  -  |

<a id="apiV1DocumentsNextCorrelativoGet"></a>
# **apiV1DocumentsNextCorrelativoGet**
> ApiV1DocumentsNextCorrelativoGet200Response apiV1DocumentsNextCorrelativoGet(companyRuc, tipoDoc, serie)

Obtener el siguiente correlativo disponible para una serie

Busca el correlativo más alto existente para la combinación empresa+tipoDoc+serie y retorna el siguiente. Útil para auto-numeración.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    String companyRuc = "companyRuc_example"; // String | 
    String tipoDoc = "tipoDoc_example"; // String | 
    String serie = "serie_example"; // String | 
    try {
      ApiV1DocumentsNextCorrelativoGet200Response result = apiInstance.apiV1DocumentsNextCorrelativoGet(companyRuc, tipoDoc, serie);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#apiV1DocumentsNextCorrelativoGet");
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

[**ApiV1DocumentsNextCorrelativoGet200Response**](ApiV1DocumentsNextCorrelativoGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **404** | Default Response |  -  |

