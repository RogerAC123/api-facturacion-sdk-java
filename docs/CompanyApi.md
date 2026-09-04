# CompanyApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiV1CompaniesClaimPost**](CompanyApi.md#apiV1CompaniesClaimPost) | **POST** /api/v1/companies/claim | Reclamar un RUC registrado por otra cuenta, con su certificado |
| [**apiV1CompaniesGet**](CompanyApi.md#apiV1CompaniesGet) | **GET** /api/v1/companies | Listar empresas emisoras |
| [**apiV1CompaniesIdGet**](CompanyApi.md#apiV1CompaniesIdGet) | **GET** /api/v1/companies/{id} | Detalle de empresa |
| [**apiV1CompaniesIdLogoGet**](CompanyApi.md#apiV1CompaniesIdLogoGet) | **GET** /api/v1/companies/{id}/logo | Obtener logo de la empresa (PNG/JPG) |
| [**apiV1CompaniesIdPut**](CompanyApi.md#apiV1CompaniesIdPut) | **PUT** /api/v1/companies/{id} | Actualizar empresa |
| [**apiV1CompaniesPost**](CompanyApi.md#apiV1CompaniesPost) | **POST** /api/v1/companies | Crear empresa emisora |


<a id="apiV1CompaniesClaimPost"></a>
# **apiV1CompaniesClaimPost**
> apiV1CompaniesClaimPost(apiV1CompaniesClaimPostRequest)

Reclamar un RUC registrado por otra cuenta, con su certificado

Prueba de titularidad &#x3D; certificado digital del RUC. Si la cuenta que lo tiene no acreditó titularidad y no emitió documentos, el RUC pasa a tu cuenta.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    ApiV1CompaniesClaimPostRequest apiV1CompaniesClaimPostRequest = new ApiV1CompaniesClaimPostRequest(); // ApiV1CompaniesClaimPostRequest | 
    try {
      apiInstance.apiV1CompaniesClaimPost(apiV1CompaniesClaimPostRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#apiV1CompaniesClaimPost");
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
| **apiV1CompaniesClaimPostRequest** | [**ApiV1CompaniesClaimPostRequest**](ApiV1CompaniesClaimPostRequest.md)|  | |

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

<a id="apiV1CompaniesGet"></a>
# **apiV1CompaniesGet**
> apiV1CompaniesGet()

Listar empresas emisoras

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    try {
      apiInstance.apiV1CompaniesGet();
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#apiV1CompaniesGet");
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

<a id="apiV1CompaniesIdGet"></a>
# **apiV1CompaniesIdGet**
> apiV1CompaniesIdGet(id)

Detalle de empresa

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1CompaniesIdGet(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#apiV1CompaniesIdGet");
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

<a id="apiV1CompaniesIdLogoGet"></a>
# **apiV1CompaniesIdLogoGet**
> apiV1CompaniesIdLogoGet(id)

Obtener logo de la empresa (PNG/JPG)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1CompaniesIdLogoGet(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#apiV1CompaniesIdLogoGet");
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

<a id="apiV1CompaniesIdPut"></a>
# **apiV1CompaniesIdPut**
> apiV1CompaniesIdPut(id, apiV1CompaniesIdPutRequest)

Actualizar empresa

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    ApiV1CompaniesIdPutRequest apiV1CompaniesIdPutRequest = new ApiV1CompaniesIdPutRequest(); // ApiV1CompaniesIdPutRequest | 
    try {
      apiInstance.apiV1CompaniesIdPut(id, apiV1CompaniesIdPutRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#apiV1CompaniesIdPut");
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
| **apiV1CompaniesIdPutRequest** | [**ApiV1CompaniesIdPutRequest**](ApiV1CompaniesIdPutRequest.md)|  | |

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

<a id="apiV1CompaniesPost"></a>
# **apiV1CompaniesPost**
> apiV1CompaniesPost(apiV1CompaniesPostRequest)

Crear empresa emisora

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    ApiV1CompaniesPostRequest apiV1CompaniesPostRequest = new ApiV1CompaniesPostRequest(); // ApiV1CompaniesPostRequest | 
    try {
      apiInstance.apiV1CompaniesPost(apiV1CompaniesPostRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#apiV1CompaniesPost");
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
| **apiV1CompaniesPostRequest** | [**ApiV1CompaniesPostRequest**](ApiV1CompaniesPostRequest.md)|  | |

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

