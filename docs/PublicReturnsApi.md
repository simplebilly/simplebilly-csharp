# Org.OpenAPITools.Api.PublicReturnsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetPublicReturnStatus**](PublicReturnsApi.md#getpublicreturnstatus) | **GET** /api/v1/public/returns/status | Customer checks the status of a return (public, no auth). The return is only revealed when its linked order&#39;s email matches. |
| [**ListPublicReturns**](PublicReturnsApi.md#listpublicreturns) | **GET** /api/v1/public/returns/list | List all returns for an order (public, no auth). |
| [**RequestPublicReturn**](PublicReturnsApi.md#requestpublicreturn) | **POST** /api/v1/public/returns/request | Customer requests a return for an order (public, no auth). |

<a id="getpublicreturnstatus"></a>
# **GetPublicReturnStatus**
> PublicReturnStatusResponse GetPublicReturnStatus (string email, string? returnNumber = null, string? returnOrderId = null, string? orderNumber = null)

Customer checks the status of a return (public, no auth). The return is only revealed when its linked order's email matches.

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
    public class GetPublicReturnStatusExample
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
            var apiInstance = new PublicReturnsApi(httpClient, config, httpClientHandler);
            var email = "email_example";  // string | 
            var returnNumber = "returnNumber_example";  // string? | Either return_number or return_order_id must be provided. (optional) 
            var returnOrderId = "returnOrderId_example";  // string? |  (optional) 
            var orderNumber = "orderNumber_example";  // string? |  (optional) 

            try
            {
                // Customer checks the status of a return (public, no auth). The return is only revealed when its linked order's email matches.
                PublicReturnStatusResponse result = apiInstance.GetPublicReturnStatus(email, returnNumber, returnOrderId, orderNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PublicReturnsApi.GetPublicReturnStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPublicReturnStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Customer checks the status of a return (public, no auth). The return is only revealed when its linked order's email matches.
    ApiResponse<PublicReturnStatusResponse> response = apiInstance.GetPublicReturnStatusWithHttpInfo(email, returnNumber, returnOrderId, orderNumber);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PublicReturnsApi.GetPublicReturnStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **email** | **string** |  |  |
| **returnNumber** | **string?** | Either return_number or return_order_id must be provided. | [optional]  |
| **returnOrderId** | **string?** |  | [optional]  |
| **orderNumber** | **string?** |  | [optional]  |

### Return type

[**PublicReturnStatusResponse**](PublicReturnStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return status |  -  |
| **400** | Bad request (missing return identifier) |  -  |
| **404** | Return not found or email mismatch |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listpublicreturns"></a>
# **ListPublicReturns**
> List&lt;PublicReturnStatusResponse&gt; ListPublicReturns (string orderNumber, string email)

List all returns for an order (public, no auth).

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
    public class ListPublicReturnsExample
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
            var apiInstance = new PublicReturnsApi(httpClient, config, httpClientHandler);
            var orderNumber = "orderNumber_example";  // string | 
            var email = "email_example";  // string | 

            try
            {
                // List all returns for an order (public, no auth).
                List<PublicReturnStatusResponse> result = apiInstance.ListPublicReturns(orderNumber, email);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PublicReturnsApi.ListPublicReturns: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListPublicReturnsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List all returns for an order (public, no auth).
    ApiResponse<List<PublicReturnStatusResponse>> response = apiInstance.ListPublicReturnsWithHttpInfo(orderNumber, email);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PublicReturnsApi.ListPublicReturnsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orderNumber** | **string** |  |  |
| **email** | **string** |  |  |

### Return type

[**List&lt;PublicReturnStatusResponse&gt;**](PublicReturnStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Returns for the order |  -  |
| **404** | Order not found or email mismatch |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="requestpublicreturn"></a>
# **RequestPublicReturn**
> PublicReturnResponse RequestPublicReturn (PublicReturnRequest publicReturnRequest)

Customer requests a return for an order (public, no auth).

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
    public class RequestPublicReturnExample
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
            var apiInstance = new PublicReturnsApi(httpClient, config, httpClientHandler);
            var publicReturnRequest = new PublicReturnRequest(); // PublicReturnRequest | 

            try
            {
                // Customer requests a return for an order (public, no auth).
                PublicReturnResponse result = apiInstance.RequestPublicReturn(publicReturnRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PublicReturnsApi.RequestPublicReturn: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RequestPublicReturnWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Customer requests a return for an order (public, no auth).
    ApiResponse<PublicReturnResponse> response = apiInstance.RequestPublicReturnWithHttpInfo(publicReturnRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PublicReturnsApi.RequestPublicReturnWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **publicReturnRequest** | [**PublicReturnRequest**](PublicReturnRequest.md) |  |  |

### Return type

[**PublicReturnResponse**](PublicReturnResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Return requested |  -  |
| **400** | Bad request (item not in order / quantity too high) |  -  |
| **404** | Order not found or email mismatch |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

