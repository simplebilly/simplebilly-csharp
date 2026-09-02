# Org.OpenAPITools.Api.SupplierInvoiceApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateSupplierInvoice**](SupplierInvoiceApi.md#createsupplierinvoice) | **POST** /api/v1/supplier-invoices |  |
| [**DeleteSupplierInvoice**](SupplierInvoiceApi.md#deletesupplierinvoice) | **DELETE** /api/v1/supplier-invoices/{supplier_invoice_id} |  |
| [**GetSupplierInvoice**](SupplierInvoiceApi.md#getsupplierinvoice) | **GET** /api/v1/supplier-invoices/{supplier_invoice_id} |  |
| [**ListSupplierInvoices**](SupplierInvoiceApi.md#listsupplierinvoices) | **GET** /api/v1/supplier-invoices/ |  |
| [**UpdateSupplierInvoice**](SupplierInvoiceApi.md#updatesupplierinvoice) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id} |  |
| [**UpdateSupplierInvoiceStatus**](SupplierInvoiceApi.md#updatesupplierinvoicestatus) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id}/status |  |

<a id="createsupplierinvoice"></a>
# **CreateSupplierInvoice**
> SupplierInvoice CreateSupplierInvoice (SupplierInvoice supplierInvoice)



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
    public class CreateSupplierInvoiceExample
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
            var apiInstance = new SupplierInvoiceApi(httpClient, config, httpClientHandler);
            var supplierInvoice = new SupplierInvoice(); // SupplierInvoice | 

            try
            {
                SupplierInvoice result = apiInstance.CreateSupplierInvoice(supplierInvoice);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupplierInvoiceApi.CreateSupplierInvoice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateSupplierInvoiceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<SupplierInvoice> response = apiInstance.CreateSupplierInvoiceWithHttpInfo(supplierInvoice);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupplierInvoiceApi.CreateSupplierInvoiceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **supplierInvoice** | [**SupplierInvoice**](SupplierInvoice.md) |  |  |

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

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

<a id="deletesupplierinvoice"></a>
# **DeleteSupplierInvoice**
> void DeleteSupplierInvoice (string supplierInvoiceId)



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
    public class DeleteSupplierInvoiceExample
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
            var apiInstance = new SupplierInvoiceApi(httpClient, config, httpClientHandler);
            var supplierInvoiceId = "supplierInvoiceId_example";  // string | 

            try
            {
                apiInstance.DeleteSupplierInvoice(supplierInvoiceId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupplierInvoiceApi.DeleteSupplierInvoice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteSupplierInvoiceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeleteSupplierInvoiceWithHttpInfo(supplierInvoiceId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupplierInvoiceApi.DeleteSupplierInvoiceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **supplierInvoiceId** | **string** |  |  |

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

<a id="getsupplierinvoice"></a>
# **GetSupplierInvoice**
> SupplierInvoice GetSupplierInvoice (string supplierInvoiceId)



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
    public class GetSupplierInvoiceExample
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
            var apiInstance = new SupplierInvoiceApi(httpClient, config, httpClientHandler);
            var supplierInvoiceId = "supplierInvoiceId_example";  // string | 

            try
            {
                SupplierInvoice result = apiInstance.GetSupplierInvoice(supplierInvoiceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupplierInvoiceApi.GetSupplierInvoice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSupplierInvoiceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<SupplierInvoice> response = apiInstance.GetSupplierInvoiceWithHttpInfo(supplierInvoiceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupplierInvoiceApi.GetSupplierInvoiceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **supplierInvoiceId** | **string** |  |  |

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

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

<a id="listsupplierinvoices"></a>
# **ListSupplierInvoices**
> List&lt;SupplierInvoice&gt; ListSupplierInvoices (int? page = null, int? pageSize = null, string? status = null, string? purchaseOrderId = null, string? supplierName = null)



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
    public class ListSupplierInvoicesExample
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
            var apiInstance = new SupplierInvoiceApi(httpClient, config, httpClientHandler);
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 
            var status = "status_example";  // string? |  (optional) 
            var purchaseOrderId = "purchaseOrderId_example";  // string? |  (optional) 
            var supplierName = "supplierName_example";  // string? |  (optional) 

            try
            {
                List<SupplierInvoice> result = apiInstance.ListSupplierInvoices(page, pageSize, status, purchaseOrderId, supplierName);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupplierInvoiceApi.ListSupplierInvoices: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListSupplierInvoicesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<SupplierInvoice>> response = apiInstance.ListSupplierInvoicesWithHttpInfo(page, pageSize, status, purchaseOrderId, supplierName);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupplierInvoiceApi.ListSupplierInvoicesWithHttpInfo: " + e.Message);
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
| **purchaseOrderId** | **string?** |  | [optional]  |
| **supplierName** | **string?** |  | [optional]  |

### Return type

[**List&lt;SupplierInvoice&gt;**](SupplierInvoice.md)

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

<a id="updatesupplierinvoice"></a>
# **UpdateSupplierInvoice**
> SupplierInvoice UpdateSupplierInvoice (string supplierInvoiceId, Object body)



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
    public class UpdateSupplierInvoiceExample
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
            var apiInstance = new SupplierInvoiceApi(httpClient, config, httpClientHandler);
            var supplierInvoiceId = "supplierInvoiceId_example";  // string | 
            var body = null;  // Object | 

            try
            {
                SupplierInvoice result = apiInstance.UpdateSupplierInvoice(supplierInvoiceId, body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupplierInvoiceApi.UpdateSupplierInvoice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateSupplierInvoiceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<SupplierInvoice> response = apiInstance.UpdateSupplierInvoiceWithHttpInfo(supplierInvoiceId, body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupplierInvoiceApi.UpdateSupplierInvoiceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **supplierInvoiceId** | **string** |  |  |
| **body** | **Object** |  |  |

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

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

<a id="updatesupplierinvoicestatus"></a>
# **UpdateSupplierInvoiceStatus**
> SupplierInvoice UpdateSupplierInvoiceStatus (string supplierInvoiceId, SupplierInvoiceStatusUpdate supplierInvoiceStatusUpdate)



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
    public class UpdateSupplierInvoiceStatusExample
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
            var apiInstance = new SupplierInvoiceApi(httpClient, config, httpClientHandler);
            var supplierInvoiceId = "supplierInvoiceId_example";  // string | 
            var supplierInvoiceStatusUpdate = new SupplierInvoiceStatusUpdate(); // SupplierInvoiceStatusUpdate | 

            try
            {
                SupplierInvoice result = apiInstance.UpdateSupplierInvoiceStatus(supplierInvoiceId, supplierInvoiceStatusUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupplierInvoiceApi.UpdateSupplierInvoiceStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateSupplierInvoiceStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<SupplierInvoice> response = apiInstance.UpdateSupplierInvoiceStatusWithHttpInfo(supplierInvoiceId, supplierInvoiceStatusUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupplierInvoiceApi.UpdateSupplierInvoiceStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **supplierInvoiceId** | **string** |  |  |
| **supplierInvoiceStatusUpdate** | [**SupplierInvoiceStatusUpdate**](SupplierInvoiceStatusUpdate.md) |  |  |

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

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

