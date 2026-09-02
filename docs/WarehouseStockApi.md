# Org.OpenAPITools.Api.WarehouseStockApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateWarehouseStock**](WarehouseStockApi.md#createwarehousestock) | **POST** /api/v1/warehouses/{warehouse_id}/stock |  |
| [**DeleteWarehouseStock**](WarehouseStockApi.md#deletewarehousestock) | **DELETE** /api/v1/warehouses/{warehouse_id}/stock/{product_id} |  |
| [**ListWarehouseStock**](WarehouseStockApi.md#listwarehousestock) | **GET** /api/v1/warehouses/{warehouse_id}/stock |  |
| [**UpdateWarehouseStock**](WarehouseStockApi.md#updatewarehousestock) | **PUT** /api/v1/warehouses/{warehouse_id}/stock/{product_id} |  |

<a id="createwarehousestock"></a>
# **CreateWarehouseStock**
> WarehouseStock CreateWarehouseStock (string warehouseId, StockAdjustment stockAdjustment)



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
    public class CreateWarehouseStockExample
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
            var apiInstance = new WarehouseStockApi(httpClient, config, httpClientHandler);
            var warehouseId = "warehouseId_example";  // string | 
            var stockAdjustment = new StockAdjustment(); // StockAdjustment | 

            try
            {
                WarehouseStock result = apiInstance.CreateWarehouseStock(warehouseId, stockAdjustment);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WarehouseStockApi.CreateWarehouseStock: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateWarehouseStockWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<WarehouseStock> response = apiInstance.CreateWarehouseStockWithHttpInfo(warehouseId, stockAdjustment);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WarehouseStockApi.CreateWarehouseStockWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **warehouseId** | **string** |  |  |
| **stockAdjustment** | [**StockAdjustment**](StockAdjustment.md) |  |  |

### Return type

[**WarehouseStock**](WarehouseStock.md)

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

<a id="deletewarehousestock"></a>
# **DeleteWarehouseStock**
> void DeleteWarehouseStock (string warehouseId, Guid productId)



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
    public class DeleteWarehouseStockExample
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
            var apiInstance = new WarehouseStockApi(httpClient, config, httpClientHandler);
            var warehouseId = "warehouseId_example";  // string | 
            var productId = "productId_example";  // Guid | 

            try
            {
                apiInstance.DeleteWarehouseStock(warehouseId, productId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WarehouseStockApi.DeleteWarehouseStock: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteWarehouseStockWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeleteWarehouseStockWithHttpInfo(warehouseId, productId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WarehouseStockApi.DeleteWarehouseStockWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **warehouseId** | **string** |  |  |
| **productId** | **Guid** |  |  |

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

<a id="listwarehousestock"></a>
# **ListWarehouseStock**
> List&lt;WarehouseStock&gt; ListWarehouseStock (string warehouseId)



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
    public class ListWarehouseStockExample
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
            var apiInstance = new WarehouseStockApi(httpClient, config, httpClientHandler);
            var warehouseId = "warehouseId_example";  // string | 

            try
            {
                List<WarehouseStock> result = apiInstance.ListWarehouseStock(warehouseId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WarehouseStockApi.ListWarehouseStock: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWarehouseStockWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<WarehouseStock>> response = apiInstance.ListWarehouseStockWithHttpInfo(warehouseId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WarehouseStockApi.ListWarehouseStockWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **warehouseId** | **string** |  |  |

### Return type

[**List&lt;WarehouseStock&gt;**](WarehouseStock.md)

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

<a id="updatewarehousestock"></a>
# **UpdateWarehouseStock**
> WarehouseStock UpdateWarehouseStock (string warehouseId, Guid productId, StockAdjustment stockAdjustment)



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
    public class UpdateWarehouseStockExample
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
            var apiInstance = new WarehouseStockApi(httpClient, config, httpClientHandler);
            var warehouseId = "warehouseId_example";  // string | 
            var productId = "productId_example";  // Guid | 
            var stockAdjustment = new StockAdjustment(); // StockAdjustment | 

            try
            {
                WarehouseStock result = apiInstance.UpdateWarehouseStock(warehouseId, productId, stockAdjustment);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WarehouseStockApi.UpdateWarehouseStock: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateWarehouseStockWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<WarehouseStock> response = apiInstance.UpdateWarehouseStockWithHttpInfo(warehouseId, productId, stockAdjustment);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WarehouseStockApi.UpdateWarehouseStockWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **warehouseId** | **string** |  |  |
| **productId** | **Guid** |  |  |
| **stockAdjustment** | [**StockAdjustment**](StockAdjustment.md) |  |  |

### Return type

[**WarehouseStock**](WarehouseStock.md)

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

