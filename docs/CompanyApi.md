# CompanyApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteCompanyLogo**](CompanyApi.md#deleteCompanyLogo) | **DELETE** /api/v1/companies/{id}/logo | Eliminar logo de la empresa |
| [**getCompany**](CompanyApi.md#getCompany) | **GET** /api/v1/companies/{id} | Detalle de empresa |
| [**getCompanyLogo**](CompanyApi.md#getCompanyLogo) | **GET** /api/v1/companies/{id}/logo | Obtener logo de la empresa (PNG/JPG) |
| [**listCompanies**](CompanyApi.md#listCompanies) | **GET** /api/v1/companies | Listar empresas emisoras |
| [**registerCompany**](CompanyApi.md#registerCompany) | **POST** /api/v1/companies/register | Dar de alta una empresa con su certificado digital |
| [**updateCompany**](CompanyApi.md#updateCompany) | **PUT** /api/v1/companies/{id} | Actualizar empresa |
| [**uploadCompanyCertificate**](CompanyApi.md#uploadCompanyCertificate) | **POST** /api/v1/companies/{id}/certificate | Subir certificado digital (.p12/.pfx en base64) |
| [**uploadCompanyLogo**](CompanyApi.md#uploadCompanyLogo) | **POST** /api/v1/companies/{id}/logo | Subir logo de la empresa (PNG/JPG, max 200KB) |


<a id="deleteCompanyLogo"></a>
# **deleteCompanyLogo**
> deleteCompanyLogo(id)

Eliminar logo de la empresa

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.deleteCompanyLogo(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#deleteCompanyLogo");
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

<a id="getCompany"></a>
# **getCompany**
> getCompany(id)

Detalle de empresa

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.getCompany(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#getCompany");
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

<a id="getCompanyLogo"></a>
# **getCompanyLogo**
> getCompanyLogo(id)

Obtener logo de la empresa (PNG/JPG)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.getCompanyLogo(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#getCompanyLogo");
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

<a id="listCompanies"></a>
# **listCompanies**
> listCompanies()

Listar empresas emisoras

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    try {
      apiInstance.listCompanies();
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#listCompanies");
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

<a id="registerCompany"></a>
# **registerCompany**
> registerCompany(registerCompanyRequest)

Dar de alta una empresa con su certificado digital

Requiere una API key live de cuenta en un plan pago (autogestión incluida). El certificado (.p12/.pfx en base64) tiene que declarar el mismo RUC; si no, no se crea nada.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    RegisterCompanyRequest registerCompanyRequest = new RegisterCompanyRequest(); // RegisterCompanyRequest | 
    try {
      apiInstance.registerCompany(registerCompanyRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#registerCompany");
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
| **registerCompanyRequest** | [**RegisterCompanyRequest**](RegisterCompanyRequest.md)|  | |

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

<a id="updateCompany"></a>
# **updateCompany**
> updateCompany(id, updateCompanyRequest)

Actualizar empresa

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    UpdateCompanyRequest updateCompanyRequest = new UpdateCompanyRequest(); // UpdateCompanyRequest | 
    try {
      apiInstance.updateCompany(id, updateCompanyRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#updateCompany");
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
| **updateCompanyRequest** | [**UpdateCompanyRequest**](UpdateCompanyRequest.md)|  | |

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

<a id="uploadCompanyCertificate"></a>
# **uploadCompanyCertificate**
> uploadCompanyCertificate(id, uploadCompanyCertificateRequest)

Subir certificado digital (.p12/.pfx en base64)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    UploadCompanyCertificateRequest uploadCompanyCertificateRequest = new UploadCompanyCertificateRequest(); // UploadCompanyCertificateRequest | 
    try {
      apiInstance.uploadCompanyCertificate(id, uploadCompanyCertificateRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#uploadCompanyCertificate");
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
| **uploadCompanyCertificateRequest** | [**UploadCompanyCertificateRequest**](UploadCompanyCertificateRequest.md)|  | |

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

<a id="uploadCompanyLogo"></a>
# **uploadCompanyLogo**
> uploadCompanyLogo(id)

Subir logo de la empresa (PNG/JPG, max 200KB)

El logo aparecerá en los PDFs (A4 y ticket). Reemplaza el anterior.

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.auth.*;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.CompanyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");
    
    // Configure HTTP bearer authorization: apiKey
    HttpBearerAuth apiKey = (HttpBearerAuth) defaultClient.getAuthentication("apiKey");
    apiKey.setBearerToken("BEARER TOKEN");

    CompanyApi apiInstance = new CompanyApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.uploadCompanyLogo(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompanyApi#uploadCompanyLogo");
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

