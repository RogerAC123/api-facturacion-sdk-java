# WebhooksApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiV1WebhooksGet**](WebhooksApi.md#apiV1WebhooksGet) | **GET** /api/v1/webhooks | Listar webhooks (filtra por RUC opcional) |
| [**apiV1WebhooksIdDelete**](WebhooksApi.md#apiV1WebhooksIdDelete) | **DELETE** /api/v1/webhooks/{id} | Eliminar webhook (también elimina su historial de deliveries) |
| [**apiV1WebhooksIdDeliveriesDeliveryIdRedeliverPost**](WebhooksApi.md#apiV1WebhooksIdDeliveriesDeliveryIdRedeliverPost) | **POST** /api/v1/webhooks/{id}/deliveries/{deliveryId}/redeliver | Reintentar manualmente una entrega |
| [**apiV1WebhooksIdDeliveriesGet**](WebhooksApi.md#apiV1WebhooksIdDeliveriesGet) | **GET** /api/v1/webhooks/{id}/deliveries | Log de entregas del webhook |
| [**apiV1WebhooksIdGet**](WebhooksApi.md#apiV1WebhooksIdGet) | **GET** /api/v1/webhooks/{id} | Detalle de webhook (sin secret) |
| [**apiV1WebhooksIdPut**](WebhooksApi.md#apiV1WebhooksIdPut) | **PUT** /api/v1/webhooks/{id} | Actualizar webhook (url, eventos, activación) |
| [**apiV1WebhooksIdRotateSecretPost**](WebhooksApi.md#apiV1WebhooksIdRotateSecretPost) | **POST** /api/v1/webhooks/{id}/rotate-secret | Rotar el secret de firma (devuelto UNA sola vez) |
| [**apiV1WebhooksIdTestPost**](WebhooksApi.md#apiV1WebhooksIdTestPost) | **POST** /api/v1/webhooks/{id}/test | Enviar un evento de prueba (webhook.test) |
| [**apiV1WebhooksPost**](WebhooksApi.md#apiV1WebhooksPost) | **POST** /api/v1/webhooks | Crear endpoint webhook |


<a id="apiV1WebhooksGet"></a>
# **apiV1WebhooksGet**
> apiV1WebhooksGet(ruc)

Listar webhooks (filtra por RUC opcional)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    String ruc = "ruc_example"; // String | 
    try {
      apiInstance.apiV1WebhooksGet(ruc);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#apiV1WebhooksGet");
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

<a id="apiV1WebhooksIdDelete"></a>
# **apiV1WebhooksIdDelete**
> apiV1WebhooksIdDelete(id)

Eliminar webhook (también elimina su historial de deliveries)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1WebhooksIdDelete(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#apiV1WebhooksIdDelete");
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

<a id="apiV1WebhooksIdDeliveriesDeliveryIdRedeliverPost"></a>
# **apiV1WebhooksIdDeliveriesDeliveryIdRedeliverPost**
> apiV1WebhooksIdDeliveriesDeliveryIdRedeliverPost(id, deliveryId)

Reintentar manualmente una entrega

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    UUID deliveryId = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1WebhooksIdDeliveriesDeliveryIdRedeliverPost(id, deliveryId);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#apiV1WebhooksIdDeliveriesDeliveryIdRedeliverPost");
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
| **deliveryId** | **UUID**|  | |

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

<a id="apiV1WebhooksIdDeliveriesGet"></a>
# **apiV1WebhooksIdDeliveriesGet**
> apiV1WebhooksIdDeliveriesGet(id, limit, success)

Log de entregas del webhook

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    Integer limit = 50; // Integer | 
    String success = "true"; // String | 
    try {
      apiInstance.apiV1WebhooksIdDeliveriesGet(id, limit, success);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#apiV1WebhooksIdDeliveriesGet");
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
| **limit** | **Integer**|  | [optional] [default to 50] |
| **success** | **String**|  | [optional] [enum: true, false] |

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

<a id="apiV1WebhooksIdGet"></a>
# **apiV1WebhooksIdGet**
> apiV1WebhooksIdGet(id)

Detalle de webhook (sin secret)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1WebhooksIdGet(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#apiV1WebhooksIdGet");
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

<a id="apiV1WebhooksIdPut"></a>
# **apiV1WebhooksIdPut**
> apiV1WebhooksIdPut(id, apiV1WebhooksIdPutRequest)

Actualizar webhook (url, eventos, activación)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    ApiV1WebhooksIdPutRequest apiV1WebhooksIdPutRequest = new ApiV1WebhooksIdPutRequest(); // ApiV1WebhooksIdPutRequest | 
    try {
      apiInstance.apiV1WebhooksIdPut(id, apiV1WebhooksIdPutRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#apiV1WebhooksIdPut");
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
| **apiV1WebhooksIdPutRequest** | [**ApiV1WebhooksIdPutRequest**](ApiV1WebhooksIdPutRequest.md)|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

<a id="apiV1WebhooksIdRotateSecretPost"></a>
# **apiV1WebhooksIdRotateSecretPost**
> apiV1WebhooksIdRotateSecretPost(id)

Rotar el secret de firma (devuelto UNA sola vez)

Genera un nuevo secret HMAC y lo devuelve una única vez. Las firmas de entregas posteriores usarán el nuevo secret; actualiza tu receptor antes de rotar.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1WebhooksIdRotateSecretPost(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#apiV1WebhooksIdRotateSecretPost");
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

<a id="apiV1WebhooksIdTestPost"></a>
# **apiV1WebhooksIdTestPost**
> apiV1WebhooksIdTestPost(id)

Enviar un evento de prueba (webhook.test)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1WebhooksIdTestPost(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#apiV1WebhooksIdTestPost");
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

<a id="apiV1WebhooksPost"></a>
# **apiV1WebhooksPost**
> apiV1WebhooksPost(apiV1WebhooksPostRequest)

Crear endpoint webhook

Registra una URL que recibirá POSTs cuando ocurran los eventos suscritos. Sin &#x60;empresaRuc&#x60; el webhook cubre TODAS las empresas de tu cuenta (un solo secret; el &#x60;empresaRuc&#x60; viaja en cada payload). La respuesta incluye el &#x60;secret&#x60; (mostrado UNA sola vez) — guárdalo para verificar las firmas HMAC-SHA256.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    ApiV1WebhooksPostRequest apiV1WebhooksPostRequest = new ApiV1WebhooksPostRequest(); // ApiV1WebhooksPostRequest | 
    try {
      apiInstance.apiV1WebhooksPost(apiV1WebhooksPostRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#apiV1WebhooksPost");
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
| **apiV1WebhooksPostRequest** | [**ApiV1WebhooksPostRequest**](ApiV1WebhooksPostRequest.md)|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

