# Org.OpenAPITools.Api.ReorderProposalApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ApplyReorderProposal**](ReorderProposalApi.md#applyreorderproposal) | **POST** /api/v1/reorder-proposals/apply | Convert a reorder proposal into a draft purchase order. |
| [**GetReorderProposal**](ReorderProposalApi.md#getreorderproposal) | **GET** /api/v1/reorder-proposals |  |

<a id="applyreorderproposal"></a>
# **ApplyReorderProposal**
> Object ApplyReorderProposal (bool? configuredOnly = null, string? warehouseId = null)

Convert a reorder proposal into a draft purchase order.

Returns the created purchase order id. Suggested line items are generated with the current reorder quantity per product.

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
    public class ApplyReorderProposalExample
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
            var apiInstance = new ReorderProposalApi(httpClient, config, httpClientHandler);
            var configuredOnly = true;  // bool? | Only include products with a reorder point configured (`min_stock`). (optional) 
            var warehouseId = "warehouseId_example";  // string? | Limit to a single warehouse id. (optional) 

            try
            {
                // Convert a reorder proposal into a draft purchase order.
                Object result = apiInstance.ApplyReorderProposal(configuredOnly, warehouseId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReorderProposalApi.ApplyReorderProposal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ApplyReorderProposalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Convert a reorder proposal into a draft purchase order.
    ApiResponse<Object> response = apiInstance.ApplyReorderProposalWithHttpInfo(configuredOnly, warehouseId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReorderProposalApi.ApplyReorderProposalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **configuredOnly** | **bool?** | Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional]  |
| **warehouseId** | **string?** | Limit to a single warehouse id. | [optional]  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getreorderproposal"></a>
# **GetReorderProposal**
> ReorderProposalResponse GetReorderProposal (bool? configuredOnly = null, string? warehouseId = null)



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
    public class GetReorderProposalExample
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
            var apiInstance = new ReorderProposalApi(httpClient, config, httpClientHandler);
            var configuredOnly = true;  // bool? | Only include products with a reorder point configured (`min_stock`). (optional) 
            var warehouseId = "warehouseId_example";  // string? | Limit to a single warehouse id. (optional) 

            try
            {
                ReorderProposalResponse result = apiInstance.GetReorderProposal(configuredOnly, warehouseId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReorderProposalApi.GetReorderProposal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReorderProposalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<ReorderProposalResponse> response = apiInstance.GetReorderProposalWithHttpInfo(configuredOnly, warehouseId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReorderProposalApi.GetReorderProposalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **configuredOnly** | **bool?** | Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional]  |
| **warehouseId** | **string?** | Limit to a single warehouse id. | [optional]  |

### Return type

[**ReorderProposalResponse**](ReorderProposalResponse.md)

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

