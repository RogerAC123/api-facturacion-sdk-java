# BranchesApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createBranch**](BranchesApi.md#createBranch) | **POST** /api/v1/companies/{id}/branches | Crear establecimiento (sucursal) |
| [**deactivateBranch**](BranchesApi.md#deactivateBranch) | **DELETE** /api/v1/companies/{id}/branches/{branchId} | Desactivar establecimiento (soft-delete) |
| [**listBranches**](BranchesApi.md#listBranches) | **GET** /api/v1/companies/{id}/branches | Listar establecimientos (sucursales) de una empresa |
| [**updateBranch**](BranchesApi.md#updateBranch) | **PUT** /api/v1/companies/{id}/branches/{branchId} | Actualizar establecimiento |


<a id="createBranch"></a>
# **createBranch**
> createBranch(id, createBranchRequest)

Crear establecimiento (sucursal)

El código debe coincidir con el que SUNAT asignó a la sucursal al registrarla en el portal SOL (Mis Trámites &gt; Establecimientos Anexos).

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.BranchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    BranchesApi apiInstance = new BranchesApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    CreateBranchRequest createBranchRequest = new CreateBranchRequest(); // CreateBranchRequest | 
    try {
      apiInstance.createBranch(id, createBranchRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling BranchesApi#createBranch");
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
| **createBranchRequest** | [**CreateBranchRequest**](CreateBranchRequest.md)|  | |

### Return type

null (empty response body)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **429** | Default Response |  -  |

<a id="deactivateBranch"></a>
# **deactivateBranch**
> deactivateBranch(id, branchId)

Desactivar establecimiento (soft-delete)

No se elimina físicamente porque puede haber documentos emitidos desde ahí. Solo se desactiva (isActive&#x3D;false).

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.BranchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    BranchesApi apiInstance = new BranchesApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    UUID branchId = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.deactivateBranch(id, branchId);
    } catch (ApiException e) {
      System.err.println("Exception when calling BranchesApi#deactivateBranch");
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

<a id="listBranches"></a>
# **listBranches**
> listBranches(id)

Listar establecimientos (sucursales) de una empresa

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.BranchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    BranchesApi apiInstance = new BranchesApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.listBranches(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling BranchesApi#listBranches");
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

<a id="updateBranch"></a>
# **updateBranch**
> updateBranch(id, branchId, updateBranchRequest)

Actualizar establecimiento

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.BranchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    BranchesApi apiInstance = new BranchesApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    UUID branchId = UUID.randomUUID(); // UUID | 
    UpdateBranchRequest updateBranchRequest = new UpdateBranchRequest(); // UpdateBranchRequest | 
    try {
      apiInstance.updateBranch(id, branchId, updateBranchRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling BranchesApi#updateBranch");
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
| **updateBranchRequest** | [**UpdateBranchRequest**](UpdateBranchRequest.md)|  | |

### Return type

null (empty response body)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **429** | Default Response |  -  |

