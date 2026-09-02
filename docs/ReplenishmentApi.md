# Org.OpenAPITools.Api.ReplenishmentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ApplyReplenishments**](ReplenishmentApi.md#applyreplenishments) | **POST** /api/v1/replenishments/apply | Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair. |
| [**GetReplenishments**](ReplenishmentApi.md#getreplenishments) | **GET** /api/v1/replenishments |  |

<a id="applyreplenishments"></a>
# **ApplyReplenishments**
> Object ApplyReplenishments (string? targetWarehouseId = null, string? sourceWarehouseId = null)

Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.

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
    public class ApplyReplenishmentsExample
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
            var apiInstance = new ReplenishmentApi(httpClient, config, httpClientHandler);
            var targetWarehouseId = "targetWarehouseId_example";  // string? | Warehouse to be replenished. Defaults to the tenant's default warehouse. (optional) 
            var sourceWarehouseId = "sourceWarehouseId_example";  // string? | Restrict source warehouses to this id. (optional) 

            try
            {
                // Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.
                Object result = apiInstance.ApplyReplenishments(targetWarehouseId, sourceWarehouseId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReplenishmentApi.ApplyReplenishments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ApplyReplenishmentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.
    ApiResponse<Object> response = apiInstance.ApplyReplenishmentsWithHttpInfo(targetWarehouseId, sourceWarehouseId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReplenishmentApi.ApplyReplenishmentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **targetWarehouseId** | **string?** | Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional]  |
| **sourceWarehouseId** | **string?** | Restrict source warehouses to this id. | [optional]  |

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

<a id="getreplenishments"></a>
# **GetReplenishments**
> ReplenishmentResponse GetReplenishments (string? targetWarehouseId = null, string? sourceWarehouseId = null)



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
    public class GetReplenishmentsExample
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
            var apiInstance = new ReplenishmentApi(httpClient, config, httpClientHandler);
            var targetWarehouseId = "targetWarehouseId_example";  // string? | Warehouse to be replenished. Defaults to the tenant's default warehouse. (optional) 
            var sourceWarehouseId = "sourceWarehouseId_example";  // string? | Restrict source warehouses to this id. (optional) 

            try
            {
                ReplenishmentResponse result = apiInstance.GetReplenishments(targetWarehouseId, sourceWarehouseId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReplenishmentApi.GetReplenishments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReplenishmentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<ReplenishmentResponse> response = apiInstance.GetReplenishmentsWithHttpInfo(targetWarehouseId, sourceWarehouseId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReplenishmentApi.GetReplenishmentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **targetWarehouseId** | **string?** | Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional]  |
| **sourceWarehouseId** | **string?** | Restrict source warehouses to this id. | [optional]  |

### Return type

[**ReplenishmentResponse**](ReplenishmentResponse.md)

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

