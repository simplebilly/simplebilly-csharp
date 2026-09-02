# Org.OpenAPITools.Api.DeliveryNoteApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateDeliveryNote**](DeliveryNoteApi.md#createdeliverynote) | **POST** /api/v1/delivery-notes |  |
| [**DeleteDeliveryNote**](DeliveryNoteApi.md#deletedeliverynote) | **DELETE** /api/v1/delivery-notes/{delivery_note_id} |  |
| [**DeliverynoteRestore**](DeliveryNoteApi.md#deliverynoterestore) | **POST** /api/v1/delivery-notes/{delivery_note_id}/restore |  |
| [**DownloadDeliveryNotePdf**](DeliveryNoteApi.md#downloaddeliverynotepdf) | **GET** /api/v1/delivery-notes/{delivery_note_id}/pdf |  |
| [**GetDeliveryNote**](DeliveryNoteApi.md#getdeliverynote) | **GET** /api/v1/delivery-notes/{delivery_note_id} |  |
| [**ListDeliveryNotes**](DeliveryNoteApi.md#listdeliverynotes) | **GET** /api/v1/delivery-notes/ |  |
| [**PursueDeliveryNote**](DeliveryNoteApi.md#pursuedeliverynote) | **POST** /api/v1/delivery-notes/{delivery_note_id}/pursue |  |

<a id="createdeliverynote"></a>
# **CreateDeliveryNote**
> DeliveryNote CreateDeliveryNote (DeliveryNoteCreate deliveryNoteCreate)



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
    public class CreateDeliveryNoteExample
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
            var apiInstance = new DeliveryNoteApi(httpClient, config, httpClientHandler);
            var deliveryNoteCreate = new DeliveryNoteCreate(); // DeliveryNoteCreate | 

            try
            {
                DeliveryNote result = apiInstance.CreateDeliveryNote(deliveryNoteCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryNoteApi.CreateDeliveryNote: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateDeliveryNoteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<DeliveryNote> response = apiInstance.CreateDeliveryNoteWithHttpInfo(deliveryNoteCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryNoteApi.CreateDeliveryNoteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryNoteCreate** | [**DeliveryNoteCreate**](DeliveryNoteCreate.md) |  |  |

### Return type

[**DeliveryNote**](DeliveryNote.md)

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

<a id="deletedeliverynote"></a>
# **DeleteDeliveryNote**
> void DeleteDeliveryNote (string deliveryNoteId)



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
    public class DeleteDeliveryNoteExample
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
            var apiInstance = new DeliveryNoteApi(httpClient, config, httpClientHandler);
            var deliveryNoteId = "deliveryNoteId_example";  // string | 

            try
            {
                apiInstance.DeleteDeliveryNote(deliveryNoteId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryNoteApi.DeleteDeliveryNote: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteDeliveryNoteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeleteDeliveryNoteWithHttpInfo(deliveryNoteId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryNoteApi.DeleteDeliveryNoteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryNoteId** | **string** |  |  |

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

<a id="deliverynoterestore"></a>
# **DeliverynoteRestore**
> DeliveryNote DeliverynoteRestore (string deliveryNoteId)



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
    public class DeliverynoteRestoreExample
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
            var apiInstance = new DeliveryNoteApi(httpClient, config, httpClientHandler);
            var deliveryNoteId = "deliveryNoteId_example";  // string | 

            try
            {
                DeliveryNote result = apiInstance.DeliverynoteRestore(deliveryNoteId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryNoteApi.DeliverynoteRestore: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeliverynoteRestoreWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<DeliveryNote> response = apiInstance.DeliverynoteRestoreWithHttpInfo(deliveryNoteId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryNoteApi.DeliverynoteRestoreWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryNoteId** | **string** |  |  |

### Return type

[**DeliveryNote**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Restored |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="downloaddeliverynotepdf"></a>
# **DownloadDeliveryNotePdf**
> void DownloadDeliveryNotePdf (string deliveryNoteId)



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
    public class DownloadDeliveryNotePdfExample
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
            var apiInstance = new DeliveryNoteApi(httpClient, config, httpClientHandler);
            var deliveryNoteId = "deliveryNoteId_example";  // string | 

            try
            {
                apiInstance.DownloadDeliveryNotePdf(deliveryNoteId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryNoteApi.DownloadDeliveryNotePdf: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DownloadDeliveryNotePdfWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DownloadDeliveryNotePdfWithHttpInfo(deliveryNoteId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryNoteApi.DownloadDeliveryNotePdfWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryNoteId** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | PDF file |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getdeliverynote"></a>
# **GetDeliveryNote**
> DeliveryNote GetDeliveryNote (string deliveryNoteId)



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
    public class GetDeliveryNoteExample
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
            var apiInstance = new DeliveryNoteApi(httpClient, config, httpClientHandler);
            var deliveryNoteId = "deliveryNoteId_example";  // string | 

            try
            {
                DeliveryNote result = apiInstance.GetDeliveryNote(deliveryNoteId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryNoteApi.GetDeliveryNote: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDeliveryNoteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<DeliveryNote> response = apiInstance.GetDeliveryNoteWithHttpInfo(deliveryNoteId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryNoteApi.GetDeliveryNoteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryNoteId** | **string** |  |  |

### Return type

[**DeliveryNote**](DeliveryNote.md)

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

<a id="listdeliverynotes"></a>
# **ListDeliveryNotes**
> List&lt;DeliveryNote&gt; ListDeliveryNotes (int? page = null, int? pageSize = null, string? search = null, bool? includeDeleted = null)



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
    public class ListDeliveryNotesExample
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
            var apiInstance = new DeliveryNoteApi(httpClient, config, httpClientHandler);
            var page = 1;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 
            var search = "search_example";  // string? |  (optional) 
            var includeDeleted = true;  // bool? | Soft-delete entities: set true to include rows with `deleted_at` set. (optional) 

            try
            {
                List<DeliveryNote> result = apiInstance.ListDeliveryNotes(page, pageSize, search, includeDeleted);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryNoteApi.ListDeliveryNotes: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListDeliveryNotesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<DeliveryNote>> response = apiInstance.ListDeliveryNotesWithHttpInfo(page, pageSize, search, includeDeleted);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryNoteApi.ListDeliveryNotesWithHttpInfo: " + e.Message);
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
| **includeDeleted** | **bool?** | Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional]  |

### Return type

[**List&lt;DeliveryNote&gt;**](DeliveryNote.md)

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

<a id="pursuedeliverynote"></a>
# **PursueDeliveryNote**
> Invoice PursueDeliveryNote (string deliveryNoteId)



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
    public class PursueDeliveryNoteExample
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
            var apiInstance = new DeliveryNoteApi(httpClient, config, httpClientHandler);
            var deliveryNoteId = "deliveryNoteId_example";  // string | 

            try
            {
                Invoice result = apiInstance.PursueDeliveryNote(deliveryNoteId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryNoteApi.PursueDeliveryNote: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PursueDeliveryNoteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<Invoice> response = apiInstance.PursueDeliveryNoteWithHttpInfo(deliveryNoteId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryNoteApi.PursueDeliveryNoteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryNoteId** | **string** |  |  |

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created Invoice |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

