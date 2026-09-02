# Org.OpenAPITools.Api.GoodsReceiptApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateGoodsReceipt**](GoodsReceiptApi.md#creategoodsreceipt) | **POST** /api/v1/goods-receipts |  |
| [**DeleteGoodsReceipt**](GoodsReceiptApi.md#deletegoodsreceipt) | **DELETE** /api/v1/goods-receipts/{goods_receipt_id} |  |
| [**GetGoodsReceipt**](GoodsReceiptApi.md#getgoodsreceipt) | **GET** /api/v1/goods-receipts/{goods_receipt_id} |  |
| [**ListGoodsReceipts**](GoodsReceiptApi.md#listgoodsreceipts) | **GET** /api/v1/goods-receipts/ |  |

<a id="creategoodsreceipt"></a>
# **CreateGoodsReceipt**
> GoodsReceipt CreateGoodsReceipt (GoodsReceipt goodsReceipt)



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
    public class CreateGoodsReceiptExample
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
            var apiInstance = new GoodsReceiptApi(httpClient, config, httpClientHandler);
            var goodsReceipt = new GoodsReceipt(); // GoodsReceipt | 

            try
            {
                GoodsReceipt result = apiInstance.CreateGoodsReceipt(goodsReceipt);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoodsReceiptApi.CreateGoodsReceipt: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateGoodsReceiptWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<GoodsReceipt> response = apiInstance.CreateGoodsReceiptWithHttpInfo(goodsReceipt);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoodsReceiptApi.CreateGoodsReceiptWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goodsReceipt** | [**GoodsReceipt**](GoodsReceipt.md) |  |  |

### Return type

[**GoodsReceipt**](GoodsReceipt.md)

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

<a id="deletegoodsreceipt"></a>
# **DeleteGoodsReceipt**
> void DeleteGoodsReceipt (string goodsReceiptId)



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
    public class DeleteGoodsReceiptExample
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
            var apiInstance = new GoodsReceiptApi(httpClient, config, httpClientHandler);
            var goodsReceiptId = "goodsReceiptId_example";  // string | 

            try
            {
                apiInstance.DeleteGoodsReceipt(goodsReceiptId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoodsReceiptApi.DeleteGoodsReceipt: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteGoodsReceiptWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeleteGoodsReceiptWithHttpInfo(goodsReceiptId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoodsReceiptApi.DeleteGoodsReceiptWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goodsReceiptId** | **string** |  |  |

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

<a id="getgoodsreceipt"></a>
# **GetGoodsReceipt**
> GoodsReceipt GetGoodsReceipt (string goodsReceiptId)



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
    public class GetGoodsReceiptExample
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
            var apiInstance = new GoodsReceiptApi(httpClient, config, httpClientHandler);
            var goodsReceiptId = "goodsReceiptId_example";  // string | 

            try
            {
                GoodsReceipt result = apiInstance.GetGoodsReceipt(goodsReceiptId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoodsReceiptApi.GetGoodsReceipt: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetGoodsReceiptWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<GoodsReceipt> response = apiInstance.GetGoodsReceiptWithHttpInfo(goodsReceiptId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoodsReceiptApi.GetGoodsReceiptWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **goodsReceiptId** | **string** |  |  |

### Return type

[**GoodsReceipt**](GoodsReceipt.md)

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

<a id="listgoodsreceipts"></a>
# **ListGoodsReceipts**
> List&lt;GoodsReceipt&gt; ListGoodsReceipts (int? page = null, int? pageSize = null, string? purchaseOrderId = null, string? supplierName = null, string? warehouseId = null)



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
    public class ListGoodsReceiptsExample
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
            var apiInstance = new GoodsReceiptApi(httpClient, config, httpClientHandler);
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 
            var purchaseOrderId = "purchaseOrderId_example";  // string? |  (optional) 
            var supplierName = "supplierName_example";  // string? |  (optional) 
            var warehouseId = "warehouseId_example";  // string? |  (optional) 

            try
            {
                List<GoodsReceipt> result = apiInstance.ListGoodsReceipts(page, pageSize, purchaseOrderId, supplierName, warehouseId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoodsReceiptApi.ListGoodsReceipts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListGoodsReceiptsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<GoodsReceipt>> response = apiInstance.ListGoodsReceiptsWithHttpInfo(page, pageSize, purchaseOrderId, supplierName, warehouseId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoodsReceiptApi.ListGoodsReceiptsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |
| **purchaseOrderId** | **string?** |  | [optional]  |
| **supplierName** | **string?** |  | [optional]  |
| **warehouseId** | **string?** |  | [optional]  |

### Return type

[**List&lt;GoodsReceipt&gt;**](GoodsReceipt.md)

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

