# Org.OpenAPITools.Api.ProductionOrderApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateProductionOrder**](ProductionOrderApi.md#createproductionorder) | **POST** /api/v1/production-orders |  |
| [**DeleteProductionOrder**](ProductionOrderApi.md#deleteproductionorder) | **DELETE** /api/v1/production-orders/{production_order_id} |  |
| [**GetProductionOrder**](ProductionOrderApi.md#getproductionorder) | **GET** /api/v1/production-orders/{production_order_id} |  |
| [**ListProductionOrders**](ProductionOrderApi.md#listproductionorders) | **GET** /api/v1/production-orders/ |  |
| [**ProductionOrderCosting**](ProductionOrderApi.md#productionordercosting) | **GET** /api/v1/production-orders/{production_order_id}/costing | Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product&#39;s sale price. |
| [**UpdateProductionOrder**](ProductionOrderApi.md#updateproductionorder) | **PUT** /api/v1/production-orders/{production_order_id} |  |
| [**UpdateProductionOrderStatus**](ProductionOrderApi.md#updateproductionorderstatus) | **PUT** /api/v1/production-orders/{production_order_id}/status |  |

<a id="createproductionorder"></a>
# **CreateProductionOrder**
> ProductionOrder CreateProductionOrder (ProductionOrder productionOrder)



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
    public class CreateProductionOrderExample
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
            var apiInstance = new ProductionOrderApi(httpClient, config, httpClientHandler);
            var productionOrder = new ProductionOrder(); // ProductionOrder | 

            try
            {
                ProductionOrder result = apiInstance.CreateProductionOrder(productionOrder);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductionOrderApi.CreateProductionOrder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateProductionOrderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<ProductionOrder> response = apiInstance.CreateProductionOrderWithHttpInfo(productionOrder);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductionOrderApi.CreateProductionOrderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productionOrder** | [**ProductionOrder**](ProductionOrder.md) |  |  |

### Return type

[**ProductionOrder**](ProductionOrder.md)

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

<a id="deleteproductionorder"></a>
# **DeleteProductionOrder**
> void DeleteProductionOrder (Guid productionOrderId)



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
    public class DeleteProductionOrderExample
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
            var apiInstance = new ProductionOrderApi(httpClient, config, httpClientHandler);
            var productionOrderId = "productionOrderId_example";  // Guid | 

            try
            {
                apiInstance.DeleteProductionOrder(productionOrderId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductionOrderApi.DeleteProductionOrder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteProductionOrderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeleteProductionOrderWithHttpInfo(productionOrderId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductionOrderApi.DeleteProductionOrderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productionOrderId** | **Guid** |  |  |

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
| **200** | OK |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getproductionorder"></a>
# **GetProductionOrder**
> ProductionOrder GetProductionOrder (Guid productionOrderId)



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
    public class GetProductionOrderExample
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
            var apiInstance = new ProductionOrderApi(httpClient, config, httpClientHandler);
            var productionOrderId = "productionOrderId_example";  // Guid | 

            try
            {
                ProductionOrder result = apiInstance.GetProductionOrder(productionOrderId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductionOrderApi.GetProductionOrder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetProductionOrderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<ProductionOrder> response = apiInstance.GetProductionOrderWithHttpInfo(productionOrderId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductionOrderApi.GetProductionOrderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productionOrderId** | **Guid** |  |  |

### Return type

[**ProductionOrder**](ProductionOrder.md)

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

<a id="listproductionorders"></a>
# **ListProductionOrders**
> List&lt;ProductionOrder&gt; ListProductionOrders (int? page = null, int? pageSize = null, string? search = null, string? status = null)



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
    public class ListProductionOrdersExample
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
            var apiInstance = new ProductionOrderApi(httpClient, config, httpClientHandler);
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 
            var search = "search_example";  // string? |  (optional) 
            var status = "status_example";  // string? | Filter by status. (optional) 

            try
            {
                List<ProductionOrder> result = apiInstance.ListProductionOrders(page, pageSize, search, status);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductionOrderApi.ListProductionOrders: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListProductionOrdersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<ProductionOrder>> response = apiInstance.ListProductionOrdersWithHttpInfo(page, pageSize, search, status);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductionOrderApi.ListProductionOrdersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |
| **search** | **string?** |  | [optional]  |
| **status** | **string?** | Filter by status. | [optional]  |

### Return type

[**List&lt;ProductionOrder&gt;**](ProductionOrder.md)

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

<a id="productionordercosting"></a>
# **ProductionOrderCosting**
> ProductionOrderCosting ProductionOrderCosting (Guid productionOrderId)

Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product's sale price.

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
    public class ProductionOrderCostingExample
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
            var apiInstance = new ProductionOrderApi(httpClient, config, httpClientHandler);
            var productionOrderId = "productionOrderId_example";  // Guid | 

            try
            {
                // Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product's sale price.
                ProductionOrderCosting result = apiInstance.ProductionOrderCosting(productionOrderId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductionOrderApi.ProductionOrderCosting: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProductionOrderCostingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product's sale price.
    ApiResponse<ProductionOrderCosting> response = apiInstance.ProductionOrderCostingWithHttpInfo(productionOrderId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductionOrderApi.ProductionOrderCostingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productionOrderId** | **Guid** |  |  |

### Return type

[**ProductionOrderCosting**](ProductionOrderCosting.md)

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

<a id="updateproductionorder"></a>
# **UpdateProductionOrder**
> ProductionOrder UpdateProductionOrder (Guid productionOrderId, ProductionOrder productionOrder)



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
    public class UpdateProductionOrderExample
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
            var apiInstance = new ProductionOrderApi(httpClient, config, httpClientHandler);
            var productionOrderId = "productionOrderId_example";  // Guid | 
            var productionOrder = new ProductionOrder(); // ProductionOrder | 

            try
            {
                ProductionOrder result = apiInstance.UpdateProductionOrder(productionOrderId, productionOrder);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductionOrderApi.UpdateProductionOrder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateProductionOrderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<ProductionOrder> response = apiInstance.UpdateProductionOrderWithHttpInfo(productionOrderId, productionOrder);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductionOrderApi.UpdateProductionOrderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productionOrderId** | **Guid** |  |  |
| **productionOrder** | [**ProductionOrder**](ProductionOrder.md) |  |  |

### Return type

[**ProductionOrder**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateproductionorderstatus"></a>
# **UpdateProductionOrderStatus**
> ProductionOrder UpdateProductionOrderStatus (Guid productionOrderId, ProductionOrderStatusUpdate productionOrderStatusUpdate)



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
    public class UpdateProductionOrderStatusExample
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
            var apiInstance = new ProductionOrderApi(httpClient, config, httpClientHandler);
            var productionOrderId = "productionOrderId_example";  // Guid | 
            var productionOrderStatusUpdate = new ProductionOrderStatusUpdate(); // ProductionOrderStatusUpdate | 

            try
            {
                ProductionOrder result = apiInstance.UpdateProductionOrderStatus(productionOrderId, productionOrderStatusUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductionOrderApi.UpdateProductionOrderStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateProductionOrderStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<ProductionOrder> response = apiInstance.UpdateProductionOrderStatusWithHttpInfo(productionOrderId, productionOrderStatusUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductionOrderApi.UpdateProductionOrderStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productionOrderId** | **Guid** |  |  |
| **productionOrderStatusUpdate** | [**ProductionOrderStatusUpdate**](ProductionOrderStatusUpdate.md) |  |  |

### Return type

[**ProductionOrder**](ProductionOrder.md)

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

