# SystemApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiV1CatalogsGet**](SystemApi.md#apiV1CatalogsGet) | **GET** /api/v1/catalogs | Listar catálogos SUNAT (código → descripción) |
| [**apiV1CatalogsKeyGet**](SystemApi.md#apiV1CatalogsKeyGet) | **GET** /api/v1/catalogs/{key} | Obtener un catálogo por clave |
| [**healthGet**](SystemApi.md#healthGet) | **GET** /health | Health check del servicio (DB + Redis + SUNAT env) |
| [**internalCertificatesExpiringGet**](SystemApi.md#internalCertificatesExpiringGet) | **GET** /internal/certificates/expiring | List certificates expiring within N days (internal) |
| [**internalWebhooksStatsGet**](SystemApi.md#internalWebhooksStatsGet) | **GET** /internal/webhooks/stats | Webhook delivery statistics (internal) |


<a id="apiV1CatalogsGet"></a>
# **apiV1CatalogsGet**
> ApiV1CatalogsGet200Response apiV1CatalogsGet()

Listar catálogos SUNAT (código → descripción)

Devuelve los catálogos SUNAT más usados y los específicos de guías de remisión (01 tipo doc, 06 doc identidad, 18 modalidad, 20 motivo traslado, 61 doc relacionado, 07 afectación IGV, 25 unidad, etc.).

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
    defaultClient.setBasePath("http://localhost:3000");

    SystemApi apiInstance = new SystemApi(defaultClient);
    try {
      ApiV1CatalogsGet200Response result = apiInstance.apiV1CatalogsGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemApi#apiV1CatalogsGet");
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

[**ApiV1CatalogsGet200Response**](ApiV1CatalogsGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

<a id="apiV1CatalogsKeyGet"></a>
# **apiV1CatalogsKeyGet**
> apiV1CatalogsKeyGet(key)

Obtener un catálogo por clave

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
    defaultClient.setBasePath("http://localhost:3000");

    SystemApi apiInstance = new SystemApi(defaultClient);
    String key = "key_example"; // String | 
    try {
      apiInstance.apiV1CatalogsKeyGet(key);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemApi#apiV1CatalogsKeyGet");
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

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

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
    defaultClient.setBasePath("http://localhost:3000");

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
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SystemApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

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

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

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
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.SystemApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

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

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

