# Org.OpenAPITools.Api.SupportTicketApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateTicketApi**](SupportTicketApi.md#createticketapi) | **POST** /api/v1/support/tickets |  |
| [**DeleteTicketApi**](SupportTicketApi.md#deleteticketapi) | **DELETE** /api/v1/support/tickets/{ticket_id} |  |
| [**GetTicketApi**](SupportTicketApi.md#getticketapi) | **GET** /api/v1/support/tickets/{ticket_id} |  |
| [**ListTicketsApi**](SupportTicketApi.md#listticketsapi) | **GET** /api/v1/support/tickets |  |
| [**UpdateTicketApi**](SupportTicketApi.md#updateticketapi) | **PUT** /api/v1/support/tickets/{ticket_id} |  |

<a id="createticketapi"></a>
# **CreateTicketApi**
> SupportTicket CreateTicketApi (CreateTicketRequest createTicketRequest)



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
    public class CreateTicketApiExample
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
            var apiInstance = new SupportTicketApi(httpClient, config, httpClientHandler);
            var createTicketRequest = new CreateTicketRequest(); // CreateTicketRequest | 

            try
            {
                SupportTicket result = apiInstance.CreateTicketApi(createTicketRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupportTicketApi.CreateTicketApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTicketApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<SupportTicket> response = apiInstance.CreateTicketApiWithHttpInfo(createTicketRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupportTicketApi.CreateTicketApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createTicketRequest** | [**CreateTicketRequest**](CreateTicketRequest.md) |  |  |

### Return type

[**SupportTicket**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Ticket created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteticketapi"></a>
# **DeleteTicketApi**
> void DeleteTicketApi (Guid ticketId)



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
    public class DeleteTicketApiExample
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
            var apiInstance = new SupportTicketApi(httpClient, config, httpClientHandler);
            var ticketId = "ticketId_example";  // Guid | 

            try
            {
                apiInstance.DeleteTicketApi(ticketId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupportTicketApi.DeleteTicketApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTicketApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeleteTicketApiWithHttpInfo(ticketId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupportTicketApi.DeleteTicketApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ticketId** | **Guid** |  |  |

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Ticket deleted |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getticketapi"></a>
# **GetTicketApi**
> SupportTicket GetTicketApi (Guid ticketId)



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
    public class GetTicketApiExample
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
            var apiInstance = new SupportTicketApi(httpClient, config, httpClientHandler);
            var ticketId = "ticketId_example";  // Guid | 

            try
            {
                SupportTicket result = apiInstance.GetTicketApi(ticketId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupportTicketApi.GetTicketApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTicketApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<SupportTicket> response = apiInstance.GetTicketApiWithHttpInfo(ticketId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupportTicketApi.GetTicketApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ticketId** | **Guid** |  |  |

### Return type

[**SupportTicket**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ticket detail |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listticketsapi"></a>
# **ListTicketsApi**
> List&lt;SupportTicket&gt; ListTicketsApi (string? status = null, string? priority = null, Guid? assignedTo = null, string? channelType = null, string? customerId = null, string? search = null, int? page = null, int? pageSize = null)



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
    public class ListTicketsApiExample
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
            var apiInstance = new SupportTicketApi(httpClient, config, httpClientHandler);
            var status = "status_example";  // string? |  (optional) 
            var priority = "priority_example";  // string? |  (optional) 
            var assignedTo = "assignedTo_example";  // Guid? |  (optional) 
            var channelType = "channelType_example";  // string? |  (optional) 
            var customerId = "customerId_example";  // string? |  (optional) 
            var search = "search_example";  // string? |  (optional) 
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 

            try
            {
                List<SupportTicket> result = apiInstance.ListTicketsApi(status, priority, assignedTo, channelType, customerId, search, page, pageSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupportTicketApi.ListTicketsApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTicketsApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<SupportTicket>> response = apiInstance.ListTicketsApiWithHttpInfo(status, priority, assignedTo, channelType, customerId, search, page, pageSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupportTicketApi.ListTicketsApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **status** | **string?** |  | [optional]  |
| **priority** | **string?** |  | [optional]  |
| **assignedTo** | **Guid?** |  | [optional]  |
| **channelType** | **string?** |  | [optional]  |
| **customerId** | **string?** |  | [optional]  |
| **search** | **string?** |  | [optional]  |
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |

### Return type

[**List&lt;SupportTicket&gt;**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tickets list |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateticketapi"></a>
# **UpdateTicketApi**
> SupportTicket UpdateTicketApi (Guid ticketId, SupportTicketUpdate supportTicketUpdate)



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
    public class UpdateTicketApiExample
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
            var apiInstance = new SupportTicketApi(httpClient, config, httpClientHandler);
            var ticketId = "ticketId_example";  // Guid | 
            var supportTicketUpdate = new SupportTicketUpdate(); // SupportTicketUpdate | 

            try
            {
                SupportTicket result = apiInstance.UpdateTicketApi(ticketId, supportTicketUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupportTicketApi.UpdateTicketApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTicketApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<SupportTicket> response = apiInstance.UpdateTicketApiWithHttpInfo(ticketId, supportTicketUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupportTicketApi.UpdateTicketApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ticketId** | **Guid** |  |  |
| **supportTicketUpdate** | [**SupportTicketUpdate**](SupportTicketUpdate.md) |  |  |

### Return type

[**SupportTicket**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ticket updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

