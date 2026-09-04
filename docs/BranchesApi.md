# BranchesApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiV1CompaniesIdBranchesBranchIdDelete**](BranchesApi.md#apiV1CompaniesIdBranchesBranchIdDelete) | **DELETE** /api/v1/companies/{id}/branches/{branchId} | Desactivar establecimiento (soft-delete) |
| [**apiV1CompaniesIdBranchesBranchIdPut**](BranchesApi.md#apiV1CompaniesIdBranchesBranchIdPut) | **PUT** /api/v1/companies/{id}/branches/{branchId} | Actualizar establecimiento |
| [**apiV1CompaniesIdBranchesGet**](BranchesApi.md#apiV1CompaniesIdBranchesGet) | **GET** /api/v1/companies/{id}/branches | Listar establecimientos (sucursales) de una empresa |
| [**apiV1CompaniesIdBranchesPost**](BranchesApi.md#apiV1CompaniesIdBranchesPost) | **POST** /api/v1/companies/{id}/branches | Crear establecimiento (sucursal) |


<a id="apiV1CompaniesIdBranchesBranchIdDelete"></a>
# **apiV1CompaniesIdBranchesBranchIdDelete**
> apiV1CompaniesIdBranchesBranchIdDelete(id, branchId)

Desactivar establecimiento (soft-delete)

No se elimina físicamente porque puede haber documentos emitidos desde ahí. Solo se desactiva (isActive&#x3D;false).

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.BranchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    BranchesApi apiInstance = new BranchesApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    UUID branchId = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1CompaniesIdBranchesBranchIdDelete(id, branchId);
    } catch (ApiException e) {
      System.err.println("Exception when calling BranchesApi#apiV1CompaniesIdBranchesBranchIdDelete");
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
| **branchId** | **UUID**|  | |

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

<a id="apiV1CompaniesIdBranchesBranchIdPut"></a>
# **apiV1CompaniesIdBranchesBranchIdPut**
> apiV1CompaniesIdBranchesBranchIdPut(id, branchId, apiV1CompaniesIdBranchesBranchIdPutRequest)

Actualizar establecimiento

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.BranchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    BranchesApi apiInstance = new BranchesApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    UUID branchId = UUID.randomUUID(); // UUID | 
    ApiV1CompaniesIdBranchesBranchIdPutRequest apiV1CompaniesIdBranchesBranchIdPutRequest = new ApiV1CompaniesIdBranchesBranchIdPutRequest(); // ApiV1CompaniesIdBranchesBranchIdPutRequest | 
    try {
      apiInstance.apiV1CompaniesIdBranchesBranchIdPut(id, branchId, apiV1CompaniesIdBranchesBranchIdPutRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling BranchesApi#apiV1CompaniesIdBranchesBranchIdPut");
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
| **branchId** | **UUID**|  | |
| **apiV1CompaniesIdBranchesBranchIdPutRequest** | [**ApiV1CompaniesIdBranchesBranchIdPutRequest**](ApiV1CompaniesIdBranchesBranchIdPutRequest.md)|  | |

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

<a id="apiV1CompaniesIdBranchesGet"></a>
# **apiV1CompaniesIdBranchesGet**
> apiV1CompaniesIdBranchesGet(id)

Listar establecimientos (sucursales) de una empresa

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.BranchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    BranchesApi apiInstance = new BranchesApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1CompaniesIdBranchesGet(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling BranchesApi#apiV1CompaniesIdBranchesGet");
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

<a id="apiV1CompaniesIdBranchesPost"></a>
# **apiV1CompaniesIdBranchesPost**
> apiV1CompaniesIdBranchesPost(id, apiV1CompaniesIdBranchesPostRequest)

Crear establecimiento (sucursal)

El código debe coincidir con el que SUNAT asignó a la sucursal al registrarla en el portal SOL (Mis Trámites &gt; Establecimientos Anexos).

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.BranchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    BranchesApi apiInstance = new BranchesApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    ApiV1CompaniesIdBranchesPostRequest apiV1CompaniesIdBranchesPostRequest = new ApiV1CompaniesIdBranchesPostRequest(); // ApiV1CompaniesIdBranchesPostRequest | 
    try {
      apiInstance.apiV1CompaniesIdBranchesPost(id, apiV1CompaniesIdBranchesPostRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling BranchesApi#apiV1CompaniesIdBranchesPost");
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
| **apiV1CompaniesIdBranchesPostRequest** | [**ApiV1CompaniesIdBranchesPostRequest**](ApiV1CompaniesIdBranchesPostRequest.md)|  | |

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

