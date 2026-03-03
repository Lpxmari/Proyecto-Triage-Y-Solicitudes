# DefaultApi

All URIs are relative to *http://localhost:8080/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**asignarFuncionario**](DefaultApi.md#asignarFuncionario) | **PUT** /solicitudes/{id}/funcionario | Asignar funcionario encargado |
| [**asignarPrioridad**](DefaultApi.md#asignarPrioridad) | **PUT** /solicitudes/{id}/priorizar | Asignar prioridad y Triage |
| [**consultarHistorial**](DefaultApi.md#consultarHistorial) | **GET** /solicitudes/{id}/historial | Ver historial de cambios de la solicitud |
| [**consultarSolicitudes**](DefaultApi.md#consultarSolicitudes) | **GET** /solicitudes | Consultar solicitudes (Funcionario) |
| [**login**](DefaultApi.md#login) | **POST** /auth/login | Autenticación de usuario |
| [**registrarSolicitud**](DefaultApi.md#registrarSolicitud) | **POST** /solicitudes | Registrar nueva solicitud (Estudiante) |


<a id="asignarFuncionario"></a>
# **asignarFuncionario**
> asignarFuncionario(id, asignarFuncionarioRequest)

Asignar funcionario encargado

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String id = "id_example"; // String | 
    AsignarFuncionarioRequest asignarFuncionarioRequest = new AsignarFuncionarioRequest(); // AsignarFuncionarioRequest | 
    try {
      apiInstance.asignarFuncionario(id, asignarFuncionarioRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#asignarFuncionario");
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
| **id** | **String**|  | |
| **asignarFuncionarioRequest** | [**AsignarFuncionarioRequest**](AsignarFuncionarioRequest.md)|  | |

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Funcionario asignado correctamente |  -  |

<a id="asignarPrioridad"></a>
# **asignarPrioridad**
> asignarPrioridad(id, prioridadDTO)

Asignar prioridad y Triage

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String id = "id_example"; // String | 
    PrioridadDTO prioridadDTO = new PrioridadDTO(); // PrioridadDTO | 
    try {
      apiInstance.asignarPrioridad(id, prioridadDTO);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#asignarPrioridad");
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
| **id** | **String**|  | |
| **prioridadDTO** | [**PrioridadDTO**](PrioridadDTO.md)|  | |

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Prioridad asignada exitosamente |  -  |

<a id="consultarHistorial"></a>
# **consultarHistorial**
> List&lt;HistorialDTO&gt; consultarHistorial(id)

Ver historial de cambios de la solicitud

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      List<HistorialDTO> result = apiInstance.consultarHistorial(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#consultarHistorial");
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
| **id** | **String**|  | |

### Return type

[**List&lt;HistorialDTO&gt;**](HistorialDTO.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Historial obtenido |  -  |

<a id="consultarSolicitudes"></a>
# **consultarSolicitudes**
> List&lt;SolicitudDTO&gt; consultarSolicitudes(estado)

Consultar solicitudes (Funcionario)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    EstadoSolicitud estado = EstadoSolicitud.fromValue("Registrada"); // EstadoSolicitud | 
    try {
      List<SolicitudDTO> result = apiInstance.consultarSolicitudes(estado);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#consultarSolicitudes");
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
| **estado** | [**EstadoSolicitud**](.md)|  | [optional] [enum: Registrada, Clasificada, EnAtencion, Atendida, Cerrada] |

### Return type

[**List&lt;SolicitudDTO&gt;**](SolicitudDTO.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Lista de solicitudes obtenida |  -  |

<a id="login"></a>
# **login**
> LoginResponse login(loginRequest)

Autenticación de usuario

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080/api");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    LoginRequest loginRequest = new LoginRequest(); // LoginRequest | 
    try {
      LoginResponse result = apiInstance.login(loginRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#login");
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
| **loginRequest** | [**LoginRequest**](LoginRequest.md)|  | |

### Return type

[**LoginResponse**](LoginResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Token JWT generado correctamente |  -  |

<a id="registrarSolicitud"></a>
# **registrarSolicitud**
> SolicitudDTO registrarSolicitud(crearSolicitudDTO)

Registrar nueva solicitud (Estudiante)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    CrearSolicitudDTO crearSolicitudDTO = new CrearSolicitudDTO(); // CrearSolicitudDTO | 
    try {
      SolicitudDTO result = apiInstance.registrarSolicitud(crearSolicitudDTO);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#registrarSolicitud");
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
| **crearSolicitudDTO** | [**CrearSolicitudDTO**](CrearSolicitudDTO.md)|  | |

### Return type

[**SolicitudDTO**](SolicitudDTO.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Solicitud registrada correctamente |  -  |

