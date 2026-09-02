# Org.OpenAPITools.Api.StockMovementApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetStockMovement**](StockMovementApi.md#getstockmovement) | **GET** /api/v1/stock-movements/{movement_id} |  |
| [**ListStockMovements**](StockMovementApi.md#liststockmovements) | **GET** /api/v1/stock-movements/ |  |

<a id="getstockmovement"></a>
# **GetStockMovement**
> StockMovement GetStockMovement (string movementId)



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
    public class GetStockMovementExample
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
            var apiInstance = new StockMovementApi(httpClient, config, httpClientHandler);
            var movementId = "movementId_example";  // string | 

            try
            {
                StockMovement result = apiInstance.GetStockMovement(movementId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StockMovementApi.GetStockMovement: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStockMovementWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<StockMovement> response = apiInstance.GetStockMovementWithHttpInfo(movementId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StockMovementApi.GetStockMovementWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **movementId** | **string** |  |  |

### Return type

[**StockMovement**](StockMovement.md)

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

<a id="liststockmovements"></a>
# **ListStockMovements**
> List&lt;StockMovement&gt; ListStockMovements (int? page = null, int? pageSize = null, Guid? productId = null, string? warehouseId = null, string? movementType = null, DateOnly? from = null, DateOnly? to = null)



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
    public class ListStockMovementsExample
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
            var apiInstance = new StockMovementApi(httpClient, config, httpClientHandler);
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 
            var productId = "productId_example";  // Guid? |  (optional) 
            var warehouseId = "warehouseId_example";  // string? |  (optional) 
            var movementType = "movementType_example";  // string? |  (optional) 
            var from = DateOnly.Parse("2013-10-20");  // DateOnly? | Only movements on or after this date (inclusive). (optional) 
            var to = DateOnly.Parse("2013-10-20");  // DateOnly? | Only movements on or before this date (inclusive). (optional) 

            try
            {
                List<StockMovement> result = apiInstance.ListStockMovements(page, pageSize, productId, warehouseId, movementType, from, to);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StockMovementApi.ListStockMovements: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListStockMovementsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<StockMovement>> response = apiInstance.ListStockMovementsWithHttpInfo(page, pageSize, productId, warehouseId, movementType, from, to);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StockMovementApi.ListStockMovementsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |
| **productId** | **Guid?** |  | [optional]  |
| **warehouseId** | **string?** |  | [optional]  |
| **movementType** | **string?** |  | [optional]  |
| **from** | **DateOnly?** | Only movements on or after this date (inclusive). | [optional]  |
| **to** | **DateOnly?** | Only movements on or before this date (inclusive). | [optional]  |

### Return type

[**List&lt;StockMovement&gt;**](StockMovement.md)

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

