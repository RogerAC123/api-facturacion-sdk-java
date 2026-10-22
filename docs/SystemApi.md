# SystemApi

All URIs are relative to *https://api-facturacion.intifact.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**exportProductoSunat**](SystemApi.md#exportProductoSunat) | **GET** /api/v1/catalogs/producto/export | Descargar el Catálogo 25 completo (52.840 códigos) |
| [**getCatalog**](SystemApi.md#getCatalog) | **GET** /api/v1/catalogs/{key} | Obtener un catálogo por clave |
| [**getProductoSunat**](SystemApi.md#getProductoSunat) | **GET** /api/v1/catalogs/producto/{codigo} | Obtener un Código de Producto SUNAT por código |
| [**healthGet**](SystemApi.md#healthGet) | **GET** /health | Health check del servicio (DB + Redis + SUNAT env) |
| [**internalCertificatesExpiringGet**](SystemApi.md#internalCertificatesExpiringGet) | **GET** /internal/certificates/expiring | List certificates expiring within N days (internal) |
| [**internalWebhooksStatsGet**](SystemApi.md#internalWebhooksStatsGet) | **GET** /internal/webhooks/stats | Webhook delivery statistics (internal) |
| [**listCatalogs**](SystemApi.md#listCatalogs) | **GET** /api/v1/catalogs | Listar catálogos SUNAT (código → descripción) |
| [**searchProductoSunat**](SystemApi.md#searchProductoSunat) | **GET** /api/v1/catalogs/producto/search | Buscar Código de Producto SUNAT (Catálogo 25 / UNSPSC) |


<a id="exportProductoSunat"></a>
# **exportProductoSunat**
> ExportProductoSunat200Response exportProductoSunat()

Descargar el Catálogo 25 completo (52.840 códigos)

Devuelve &#x60;{ success, data: { version, total, items[] } }&#x60; con TODO el catálogo, en el mismo shape que devuelve la búsqueda. Pensado para cachearlo del lado del integrador: manda &#x60;If-None-Match&#x60; con el ETag recibido y la API responde 304 si nada cambió. Se sirve con &#x60;Content-Encoding: gzip&#x60; si el cliente lo acepta (~600 KB vs ~8 MB).

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SystemApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api-facturacion.intifact.com");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    SystemApi apiInstance = new SystemApi(defaultClient);
    try {
      ExportProductoSunat200Response result = apiInstance.exportProductoSunat();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemApi#exportProductoSunat");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ExportProductoSunat200Response**](ExportProductoSunat200Response.md)

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

<a id="getCatalog"></a>
# **getCatalog**
> getCatalog(key)

Obtener un catálogo por clave

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SystemApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api-facturacion.intifact.com");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    SystemApi apiInstance = new SystemApi(defaultClient);
    String key = "key_example"; // String | 
    try {
      apiInstance.getCatalog(key);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemApi#getCatalog");
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
| **key** | **String**|  | |

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

<a id="getProductoSunat"></a>
# **getProductoSunat**
> GetProductoSunat200Response getProductoSunat(codigo)

Obtener un Código de Producto SUNAT por código

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SystemApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api-facturacion.intifact.com");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    SystemApi apiInstance = new SystemApi(defaultClient);
    String codigo = "codigo_example"; // String | 
    try {
      GetProductoSunat200Response result = apiInstance.getProductoSunat(codigo);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemApi#getProductoSunat");
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
| **codigo** | **String**|  | |

### Return type

[**GetProductoSunat200Response**](GetProductoSunat200Response.md)

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

<a id="healthGet"></a>
# **healthGet**
> healthGet()

Health check del servicio (DB + Redis + SUNAT env)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SystemApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api-facturacion.intifact.com");

    SystemApi apiInstance = new SystemApi(defaultClient);
    try {
      apiInstance.healthGet();
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemApi#healthGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

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

<a id="internalCertificatesExpiringGet"></a>
# **internalCertificatesExpiringGet**
> internalCertificatesExpiringGet(days)

List certificates expiring within N days (internal)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SystemApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api-facturacion.intifact.com");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    SystemApi apiInstance = new SystemApi(defaultClient);
    Integer days = 30; // Integer | 
    try {
      apiInstance.internalCertificatesExpiringGet(days);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemApi#internalCertificatesExpiringGet");
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
| **days** | **Integer**|  | [optional] [default to 30] |

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

<a id="internalWebhooksStatsGet"></a>
# **internalWebhooksStatsGet**
> internalWebhooksStatsGet(days)

Webhook delivery statistics (internal)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SystemApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api-facturacion.intifact.com");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    SystemApi apiInstance = new SystemApi(defaultClient);
    Integer days = 7; // Integer | 
    try {
      apiInstance.internalWebhooksStatsGet(days);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemApi#internalWebhooksStatsGet");
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
| **days** | **Integer**|  | [optional] [default to 7] |

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

<a id="listCatalogs"></a>
# **listCatalogs**
> ListCatalogs200Response listCatalogs()

Listar catálogos SUNAT (código → descripción)

Devuelve los catálogos SUNAT más usados y los específicos de guías de remisión (01 tipo doc, 06 doc identidad, 18 modalidad, 20 motivo traslado, 61 doc relacionado, 07 afectación IGV, 25 unidad, etc.).

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SystemApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api-facturacion.intifact.com");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    SystemApi apiInstance = new SystemApi(defaultClient);
    try {
      ListCatalogs200Response result = apiInstance.listCatalogs();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemApi#listCatalogs");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ListCatalogs200Response**](ListCatalogs200Response.md)

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

<a id="searchProductoSunat"></a>
# **searchProductoSunat**
> SearchProductoSunat200Response searchProductoSunat(q, nivel, limit)

Buscar Código de Producto SUNAT (Catálogo 25 / UNSPSC)

Busca por texto libre (sin distinguir tildes ni mayúsculas, todos los términos deben aparecer) o por prefijo de código si &#x60;q&#x60; son dígitos. Devuelve primero las CLASE: SUNAT exige llegar como mínimo a ese nivel y es la respuesta correcta en la mayoría de casos.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SystemApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api-facturacion.intifact.com");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    SystemApi apiInstance = new SystemApi(defaultClient);
    String q = "q_example"; // String | 
    String nivel = "CLASE"; // String | 
    Integer limit = 20; // Integer | 
    try {
      SearchProductoSunat200Response result = apiInstance.searchProductoSunat(q, nivel, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemApi#searchProductoSunat");
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
| **q** | **String**|  | |
| **nivel** | **String**|  | [optional] [enum: CLASE, PRODUCTO] |
| **limit** | **Integer**|  | [optional] [default to 20] |

### Return type

[**SearchProductoSunat200Response**](SearchProductoSunat200Response.md)

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

