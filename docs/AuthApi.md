# AuthApi

All URIs are relative to *http://localhost:3000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiV1AuthLoginPost**](AuthApi.md#apiV1AuthLoginPost) | **POST** /api/v1/auth/login | Login email+password |
| [**apiV1AuthLogoutPost**](AuthApi.md#apiV1AuthLogoutPost) | **POST** /api/v1/auth/logout | Cerrar sesión actual (revoca refresh) |
| [**apiV1AuthMeGet**](AuthApi.md#apiV1AuthMeGet) | **GET** /api/v1/auth/me | Datos del usuario actual |
| [**apiV1AuthRefreshPost**](AuthApi.md#apiV1AuthRefreshPost) | **POST** /api/v1/auth/refresh | Renovar access token con refresh cookie |
| [**apiV1AuthSessionsGet**](AuthApi.md#apiV1AuthSessionsGet) | **GET** /api/v1/auth/sessions | Lista de sesiones activas del usuario |
| [**apiV1AuthSessionsIdDelete**](AuthApi.md#apiV1AuthSessionsIdDelete) | **DELETE** /api/v1/auth/sessions/{id} | Revocar una sesión activa por ID |
| [**apiV1AuthSignupPost**](AuthApi.md#apiV1AuthSignupPost) | **POST** /api/v1/auth/signup | Registro público: crea Tenant + User + sesión |
| [**apiV1AuthVerifyEmailGet**](AuthApi.md#apiV1AuthVerifyEmailGet) | **GET** /api/v1/auth/verify-email | Confirmar email con token (one-time, 24h) |
| [**apiV1AuthVerifyEmailResendPost**](AuthApi.md#apiV1AuthVerifyEmailResendPost) | **POST** /api/v1/auth/verify-email/resend | Re-enviar email de verificación al usuario logueado |


<a id="apiV1AuthLoginPost"></a>
# **apiV1AuthLoginPost**
> apiV1AuthLoginPost(apiV1AuthLoginPostRequest)

Login email+password

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    AuthApi apiInstance = new AuthApi(defaultClient);
    ApiV1AuthLoginPostRequest apiV1AuthLoginPostRequest = new ApiV1AuthLoginPostRequest(); // ApiV1AuthLoginPostRequest | 
    try {
      apiInstance.apiV1AuthLoginPost(apiV1AuthLoginPostRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#apiV1AuthLoginPost");
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
| **apiV1AuthLoginPostRequest** | [**ApiV1AuthLoginPostRequest**](ApiV1AuthLoginPostRequest.md)|  | |

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

<a id="apiV1AuthLogoutPost"></a>
# **apiV1AuthLogoutPost**
> apiV1AuthLogoutPost()

Cerrar sesión actual (revoca refresh)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    AuthApi apiInstance = new AuthApi(defaultClient);
    try {
      apiInstance.apiV1AuthLogoutPost();
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#apiV1AuthLogoutPost");
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

<a id="apiV1AuthMeGet"></a>
# **apiV1AuthMeGet**
> apiV1AuthMeGet()

Datos del usuario actual

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    AuthApi apiInstance = new AuthApi(defaultClient);
    try {
      apiInstance.apiV1AuthMeGet();
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#apiV1AuthMeGet");
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

<a id="apiV1AuthRefreshPost"></a>
# **apiV1AuthRefreshPost**
> apiV1AuthRefreshPost()

Renovar access token con refresh cookie

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    AuthApi apiInstance = new AuthApi(defaultClient);
    try {
      apiInstance.apiV1AuthRefreshPost();
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#apiV1AuthRefreshPost");
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

<a id="apiV1AuthSessionsGet"></a>
# **apiV1AuthSessionsGet**
> apiV1AuthSessionsGet()

Lista de sesiones activas del usuario

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    AuthApi apiInstance = new AuthApi(defaultClient);
    try {
      apiInstance.apiV1AuthSessionsGet();
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#apiV1AuthSessionsGet");
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

<a id="apiV1AuthSessionsIdDelete"></a>
# **apiV1AuthSessionsIdDelete**
> apiV1AuthSessionsIdDelete(id)

Revocar una sesión activa por ID

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    AuthApi apiInstance = new AuthApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.apiV1AuthSessionsIdDelete(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#apiV1AuthSessionsIdDelete");
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

<a id="apiV1AuthSignupPost"></a>
# **apiV1AuthSignupPost**
> apiV1AuthSignupPost(apiV1AuthSignupPostRequest)

Registro público: crea Tenant + User + sesión

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    AuthApi apiInstance = new AuthApi(defaultClient);
    ApiV1AuthSignupPostRequest apiV1AuthSignupPostRequest = new ApiV1AuthSignupPostRequest(); // ApiV1AuthSignupPostRequest | 
    try {
      apiInstance.apiV1AuthSignupPost(apiV1AuthSignupPostRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#apiV1AuthSignupPost");
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
| **apiV1AuthSignupPostRequest** | [**ApiV1AuthSignupPostRequest**](ApiV1AuthSignupPostRequest.md)|  | |

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

<a id="apiV1AuthVerifyEmailGet"></a>
# **apiV1AuthVerifyEmailGet**
> apiV1AuthVerifyEmailGet(token)

Confirmar email con token (one-time, 24h)

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    AuthApi apiInstance = new AuthApi(defaultClient);
    String token = "token_example"; // String | 
    try {
      apiInstance.apiV1AuthVerifyEmailGet(token);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#apiV1AuthVerifyEmailGet");
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
| **token** | **String**|  | |

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

<a id="apiV1AuthVerifyEmailResendPost"></a>
# **apiV1AuthVerifyEmailResendPost**
> apiV1AuthVerifyEmailResendPost()

Re-enviar email de verificación al usuario logueado

### Example
```java
// Import classes:
import com.intifact.sdk.client.ApiClient;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.client.Configuration;
import com.intifact.sdk.client.models.*;
import com.intifact.sdk.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000");

    AuthApi apiInstance = new AuthApi(defaultClient);
    try {
      apiInstance.apiV1AuthVerifyEmailResendPost();
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#apiV1AuthVerifyEmailResendPost");
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

