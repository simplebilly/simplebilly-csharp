# Org.OpenAPITools.Api.PurchaseOrderApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreatePurchaseOrder**](PurchaseOrderApi.md#createpurchaseorder) | **POST** /api/v1/purchase-orders |  |
| [**DeletePurchaseOrder**](PurchaseOrderApi.md#deletepurchaseorder) | **DELETE** /api/v1/purchase-orders/{purchase_order_id} |  |
| [**GetPurchaseOrder**](PurchaseOrderApi.md#getpurchaseorder) | **GET** /api/v1/purchase-orders/{purchase_order_id} |  |
| [**ListPurchaseOrders**](PurchaseOrderApi.md#listpurchaseorders) | **GET** /api/v1/purchase-orders/ |  |
| [**MatchInvoice**](PurchaseOrderApi.md#matchinvoice) | **POST** /api/v1/purchase-orders/{purchase_order_id}/match-invoice | 3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product. |
| [**UpdatePurchaseOrder**](PurchaseOrderApi.md#updatepurchaseorder) | **PUT** /api/v1/purchase-orders/{purchase_order_id} |  |
| [**UpdatePurchaseOrderStatus**](PurchaseOrderApi.md#updatepurchaseorderstatus) | **PUT** /api/v1/purchase-orders/{purchase_order_id}/status |  |

<a id="createpurchaseorder"></a>
# **CreatePurchaseOrder**
> PurchaseOrder CreatePurchaseOrder (PurchaseOrder purchaseOrder)



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
    public class CreatePurchaseOrderExample
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
            var apiInstance = new PurchaseOrderApi(httpClient, config, httpClientHandler);
            var purchaseOrder = new PurchaseOrder(); // PurchaseOrder | 

            try
            {
                PurchaseOrder result = apiInstance.CreatePurchaseOrder(purchaseOrder);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PurchaseOrderApi.CreatePurchaseOrder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreatePurchaseOrderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<PurchaseOrder> response = apiInstance.CreatePurchaseOrderWithHttpInfo(purchaseOrder);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PurchaseOrderApi.CreatePurchaseOrderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **purchaseOrder** | [**PurchaseOrder**](PurchaseOrder.md) |  |  |

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

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

<a id="deletepurchaseorder"></a>
# **DeletePurchaseOrder**
> void DeletePurchaseOrder (string purchaseOrderId)



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
    public class DeletePurchaseOrderExample
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
            var apiInstance = new PurchaseOrderApi(httpClient, config, httpClientHandler);
            var purchaseOrderId = "purchaseOrderId_example";  // string | 

            try
            {
                apiInstance.DeletePurchaseOrder(purchaseOrderId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PurchaseOrderApi.DeletePurchaseOrder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeletePurchaseOrderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeletePurchaseOrderWithHttpInfo(purchaseOrderId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PurchaseOrderApi.DeletePurchaseOrderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **purchaseOrderId** | **string** |  |  |

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
| **400** | Bad request |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getpurchaseorder"></a>
# **GetPurchaseOrder**
> PurchaseOrder GetPurchaseOrder (string purchaseOrderId)



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
    public class GetPurchaseOrderExample
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
            var apiInstance = new PurchaseOrderApi(httpClient, config, httpClientHandler);
            var purchaseOrderId = "purchaseOrderId_example";  // string | 

            try
            {
                PurchaseOrder result = apiInstance.GetPurchaseOrder(purchaseOrderId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PurchaseOrderApi.GetPurchaseOrder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPurchaseOrderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<PurchaseOrder> response = apiInstance.GetPurchaseOrderWithHttpInfo(purchaseOrderId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PurchaseOrderApi.GetPurchaseOrderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **purchaseOrderId** | **string** |  |  |

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

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

<a id="listpurchaseorders"></a>
# **ListPurchaseOrders**
> List&lt;PurchaseOrder&gt; ListPurchaseOrders (int? page = null, int? pageSize = null, string? status = null, string? supplierName = null, string? search = null)



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
    public class ListPurchaseOrdersExample
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
            var apiInstance = new PurchaseOrderApi(httpClient, config, httpClientHandler);
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 
            var status = "status_example";  // string? |  (optional) 
            var supplierName = "supplierName_example";  // string? |  (optional) 
            var search = "search_example";  // string? |  (optional) 

            try
            {
                List<PurchaseOrder> result = apiInstance.ListPurchaseOrders(page, pageSize, status, supplierName, search);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PurchaseOrderApi.ListPurchaseOrders: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListPurchaseOrdersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<PurchaseOrder>> response = apiInstance.ListPurchaseOrdersWithHttpInfo(page, pageSize, status, supplierName, search);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PurchaseOrderApi.ListPurchaseOrdersWithHttpInfo: " + e.Message);
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
| **supplierName** | **string?** |  | [optional]  |
| **search** | **string?** |  | [optional]  |

### Return type

[**List&lt;PurchaseOrder&gt;**](PurchaseOrder.md)

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

<a id="matchinvoice"></a>
# **MatchInvoice**
> Object MatchInvoice (string purchaseOrderId, InvoiceMatchRequest invoiceMatchRequest)

3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.

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
    public class MatchInvoiceExample
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
            var apiInstance = new PurchaseOrderApi(httpClient, config, httpClientHandler);
            var purchaseOrderId = "purchaseOrderId_example";  // string | 
            var invoiceMatchRequest = new InvoiceMatchRequest(); // InvoiceMatchRequest | 

            try
            {
                // 3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.
                Object result = apiInstance.MatchInvoice(purchaseOrderId, invoiceMatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PurchaseOrderApi.MatchInvoice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MatchInvoiceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // 3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.
    ApiResponse<Object> response = apiInstance.MatchInvoiceWithHttpInfo(purchaseOrderId, invoiceMatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PurchaseOrderApi.MatchInvoiceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **purchaseOrderId** | **string** |  |  |
| **invoiceMatchRequest** | [**InvoiceMatchRequest**](InvoiceMatchRequest.md) |  |  |

### Return type

**Object**

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

<a id="updatepurchaseorder"></a>
# **UpdatePurchaseOrder**
> PurchaseOrder UpdatePurchaseOrder (string purchaseOrderId, Object body)



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
    public class UpdatePurchaseOrderExample
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
            var apiInstance = new PurchaseOrderApi(httpClient, config, httpClientHandler);
            var purchaseOrderId = "purchaseOrderId_example";  // string | 
            var body = null;  // Object | 

            try
            {
                PurchaseOrder result = apiInstance.UpdatePurchaseOrder(purchaseOrderId, body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PurchaseOrderApi.UpdatePurchaseOrder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdatePurchaseOrderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<PurchaseOrder> response = apiInstance.UpdatePurchaseOrderWithHttpInfo(purchaseOrderId, body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PurchaseOrderApi.UpdatePurchaseOrderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **purchaseOrderId** | **string** |  |  |
| **body** | **Object** |  |  |

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

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

<a id="updatepurchaseorderstatus"></a>
# **UpdatePurchaseOrderStatus**
> PurchaseOrder UpdatePurchaseOrderStatus (string purchaseOrderId, PurchaseOrderStatusUpdate purchaseOrderStatusUpdate)



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
    public class UpdatePurchaseOrderStatusExample
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
            var apiInstance = new PurchaseOrderApi(httpClient, config, httpClientHandler);
            var purchaseOrderId = "purchaseOrderId_example";  // string | 
            var purchaseOrderStatusUpdate = new PurchaseOrderStatusUpdate(); // PurchaseOrderStatusUpdate | 

            try
            {
                PurchaseOrder result = apiInstance.UpdatePurchaseOrderStatus(purchaseOrderId, purchaseOrderStatusUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PurchaseOrderApi.UpdatePurchaseOrderStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdatePurchaseOrderStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<PurchaseOrder> response = apiInstance.UpdatePurchaseOrderStatusWithHttpInfo(purchaseOrderId, purchaseOrderStatusUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PurchaseOrderApi.UpdatePurchaseOrderStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **purchaseOrderId** | **string** |  |  |
| **purchaseOrderStatusUpdate** | [**PurchaseOrderStatusUpdate**](PurchaseOrderStatusUpdate.md) |  |  |

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

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

