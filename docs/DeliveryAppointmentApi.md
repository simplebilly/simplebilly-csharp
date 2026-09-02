# Org.OpenAPITools.Api.DeliveryAppointmentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateDeliveryAppointment**](DeliveryAppointmentApi.md#createdeliveryappointment) | **POST** /api/v1/delivery-appointments |  |
| [**DeleteDeliveryAppointment**](DeliveryAppointmentApi.md#deletedeliveryappointment) | **DELETE** /api/v1/delivery-appointments/{appointment_id} |  |
| [**GetDeliveryAppointment**](DeliveryAppointmentApi.md#getdeliveryappointment) | **GET** /api/v1/delivery-appointments/{appointment_id} |  |
| [**GetPublicDeliveryAppointmentStatus**](DeliveryAppointmentApi.md#getpublicdeliveryappointmentstatus) | **GET** /api/v1/public/delivery-appointments/status | Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match. |
| [**ListDeliveryAppointments**](DeliveryAppointmentApi.md#listdeliveryappointments) | **GET** /api/v1/delivery-appointments |  |
| [**RequestPublicDeliveryAppointment**](DeliveryAppointmentApi.md#requestpublicdeliveryappointment) | **POST** /api/v1/public/delivery-appointments/request | Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by &#x60;code&#x60; — never from the request. |
| [**UpdateDeliveryAppointment**](DeliveryAppointmentApi.md#updatedeliveryappointment) | **PUT** /api/v1/delivery-appointments/{appointment_id} |  |
| [**UpdateDeliveryAppointmentStatus**](DeliveryAppointmentApi.md#updatedeliveryappointmentstatus) | **PUT** /api/v1/delivery-appointments/{appointment_id}/status |  |

<a id="createdeliveryappointment"></a>
# **CreateDeliveryAppointment**
> DeliveryAppointment CreateDeliveryAppointment (DeliveryAppointmentCreate deliveryAppointmentCreate)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class CreateDeliveryAppointmentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://demo.simplebilly.com";
            // Configure Bearer token for authorization: bearer_token
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DeliveryAppointmentApi(httpClient, config, httpClientHandler);
            var deliveryAppointmentCreate = new DeliveryAppointmentCreate(); // DeliveryAppointmentCreate | 

            try
            {
                DeliveryAppointment result = apiInstance.CreateDeliveryAppointment(deliveryAppointmentCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryAppointmentApi.CreateDeliveryAppointment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateDeliveryAppointmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<DeliveryAppointment> response = apiInstance.CreateDeliveryAppointmentWithHttpInfo(deliveryAppointmentCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryAppointmentApi.CreateDeliveryAppointmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryAppointmentCreate** | [**DeliveryAppointmentCreate**](DeliveryAppointmentCreate.md) |  |  |

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletedeliveryappointment"></a>
# **DeleteDeliveryAppointment**
> void DeleteDeliveryAppointment (string appointmentId)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class DeleteDeliveryAppointmentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://demo.simplebilly.com";
            // Configure Bearer token for authorization: bearer_token
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DeliveryAppointmentApi(httpClient, config, httpClientHandler);
            var appointmentId = "appointmentId_example";  // string | 

            try
            {
                apiInstance.DeleteDeliveryAppointment(appointmentId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryAppointmentApi.DeleteDeliveryAppointment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteDeliveryAppointmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeleteDeliveryAppointmentWithHttpInfo(appointmentId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryAppointmentApi.DeleteDeliveryAppointmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appointmentId** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | No Content |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getdeliveryappointment"></a>
# **GetDeliveryAppointment**
> DeliveryAppointment GetDeliveryAppointment (string appointmentId)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class GetDeliveryAppointmentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://demo.simplebilly.com";
            // Configure Bearer token for authorization: bearer_token
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DeliveryAppointmentApi(httpClient, config, httpClientHandler);
            var appointmentId = "appointmentId_example";  // string | 

            try
            {
                DeliveryAppointment result = apiInstance.GetDeliveryAppointment(appointmentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryAppointmentApi.GetDeliveryAppointment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDeliveryAppointmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<DeliveryAppointment> response = apiInstance.GetDeliveryAppointmentWithHttpInfo(appointmentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryAppointmentApi.GetDeliveryAppointmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appointmentId** | **string** |  |  |

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getpublicdeliveryappointmentstatus"></a>
# **GetPublicDeliveryAppointmentStatus**
> PublicDeliveryAppointmentStatusResponse GetPublicDeliveryAppointmentStatus (string appointmentId, string email, string token)

Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class GetPublicDeliveryAppointmentStatusExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://demo.simplebilly.com";
            // Configure Bearer token for authorization: bearer_token
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DeliveryAppointmentApi(httpClient, config, httpClientHandler);
            var appointmentId = "appointmentId_example";  // string | 
            var email = "email_example";  // string | 
            var token = "token_example";  // string | 

            try
            {
                // Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.
                PublicDeliveryAppointmentStatusResponse result = apiInstance.GetPublicDeliveryAppointmentStatus(appointmentId, email, token);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryAppointmentApi.GetPublicDeliveryAppointmentStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPublicDeliveryAppointmentStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.
    ApiResponse<PublicDeliveryAppointmentStatusResponse> response = apiInstance.GetPublicDeliveryAppointmentStatusWithHttpInfo(appointmentId, email, token);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryAppointmentApi.GetPublicDeliveryAppointmentStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appointmentId** | **string** |  |  |
| **email** | **string** |  |  |
| **token** | **string** |  |  |

### Return type

[**PublicDeliveryAppointmentStatusResponse**](PublicDeliveryAppointmentStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Appointment status |  -  |
| **404** | Appointment not found or credentials mismatch |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listdeliveryappointments"></a>
# **ListDeliveryAppointments**
> List&lt;DeliveryAppointment&gt; ListDeliveryAppointments (int? page = null, int? pageSize = null, string? status = null, string? warehouseId = null, DateOnly? from = null, DateOnly? to = null)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ListDeliveryAppointmentsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://demo.simplebilly.com";
            // Configure Bearer token for authorization: bearer_token
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DeliveryAppointmentApi(httpClient, config, httpClientHandler);
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 
            var status = "status_example";  // string? |  (optional) 
            var warehouseId = "warehouseId_example";  // string? |  (optional) 
            var from = DateOnly.Parse("2013-10-20");  // DateOnly? |  (optional) 
            var to = DateOnly.Parse("2013-10-20");  // DateOnly? |  (optional) 

            try
            {
                List<DeliveryAppointment> result = apiInstance.ListDeliveryAppointments(page, pageSize, status, warehouseId, from, to);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryAppointmentApi.ListDeliveryAppointments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListDeliveryAppointmentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<DeliveryAppointment>> response = apiInstance.ListDeliveryAppointmentsWithHttpInfo(page, pageSize, status, warehouseId, from, to);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryAppointmentApi.ListDeliveryAppointmentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |
| **status** | **string?** |  | [optional]  |
| **warehouseId** | **string?** |  | [optional]  |
| **from** | **DateOnly?** |  | [optional]  |
| **to** | **DateOnly?** |  | [optional]  |

### Return type

[**List&lt;DeliveryAppointment&gt;**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="requestpublicdeliveryappointment"></a>
# **RequestPublicDeliveryAppointment**
> PublicDeliveryAppointmentResponse RequestPublicDeliveryAppointment (PublicDeliveryAppointmentRequest publicDeliveryAppointmentRequest)

Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by `code` — never from the request.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class RequestPublicDeliveryAppointmentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://demo.simplebilly.com";
            // Configure Bearer token for authorization: bearer_token
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DeliveryAppointmentApi(httpClient, config, httpClientHandler);
            var publicDeliveryAppointmentRequest = new PublicDeliveryAppointmentRequest(); // PublicDeliveryAppointmentRequest | 

            try
            {
                // Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by `code` — never from the request.
                PublicDeliveryAppointmentResponse result = apiInstance.RequestPublicDeliveryAppointment(publicDeliveryAppointmentRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryAppointmentApi.RequestPublicDeliveryAppointment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RequestPublicDeliveryAppointmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by `code` — never from the request.
    ApiResponse<PublicDeliveryAppointmentResponse> response = apiInstance.RequestPublicDeliveryAppointmentWithHttpInfo(publicDeliveryAppointmentRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryAppointmentApi.RequestPublicDeliveryAppointmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **publicDeliveryAppointmentRequest** | [**PublicDeliveryAppointmentRequest**](PublicDeliveryAppointmentRequest.md) |  |  |

### Return type

[**PublicDeliveryAppointmentResponse**](PublicDeliveryAppointmentResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Appointment requested |  -  |
| **404** | Warehouse not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatedeliveryappointment"></a>
# **UpdateDeliveryAppointment**
> DeliveryAppointment UpdateDeliveryAppointment (string appointmentId, Object body)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class UpdateDeliveryAppointmentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://demo.simplebilly.com";
            // Configure Bearer token for authorization: bearer_token
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DeliveryAppointmentApi(httpClient, config, httpClientHandler);
            var appointmentId = "appointmentId_example";  // string | 
            var body = null;  // Object | 

            try
            {
                DeliveryAppointment result = apiInstance.UpdateDeliveryAppointment(appointmentId, body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryAppointmentApi.UpdateDeliveryAppointment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateDeliveryAppointmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<DeliveryAppointment> response = apiInstance.UpdateDeliveryAppointmentWithHttpInfo(appointmentId, body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryAppointmentApi.UpdateDeliveryAppointmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appointmentId** | **string** |  |  |
| **body** | **Object** |  |  |

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad request |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatedeliveryappointmentstatus"></a>
# **UpdateDeliveryAppointmentStatus**
> DeliveryAppointment UpdateDeliveryAppointmentStatus (string appointmentId, AppointmentStatusUpdate appointmentStatusUpdate)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class UpdateDeliveryAppointmentStatusExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://demo.simplebilly.com";
            // Configure Bearer token for authorization: bearer_token
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DeliveryAppointmentApi(httpClient, config, httpClientHandler);
            var appointmentId = "appointmentId_example";  // string | 
            var appointmentStatusUpdate = new AppointmentStatusUpdate(); // AppointmentStatusUpdate | 

            try
            {
                DeliveryAppointment result = apiInstance.UpdateDeliveryAppointmentStatus(appointmentId, appointmentStatusUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryAppointmentApi.UpdateDeliveryAppointmentStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateDeliveryAppointmentStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<DeliveryAppointment> response = apiInstance.UpdateDeliveryAppointmentStatusWithHttpInfo(appointmentId, appointmentStatusUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryAppointmentApi.UpdateDeliveryAppointmentStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appointmentId** | **string** |  |  |
| **appointmentStatusUpdate** | [**AppointmentStatusUpdate**](AppointmentStatusUpdate.md) |  |  |

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad request / invalid transition |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

