# Org.OpenAPITools.Api.DeliveryDateApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateDeliveryDate**](DeliveryDateApi.md#createdeliverydate) | **POST** /api/v1/delivery-dates |  |
| [**DeleteDeliveryDate**](DeliveryDateApi.md#deletedeliverydate) | **DELETE** /api/v1/delivery-dates/{delivery_date_id} |  |
| [**GetDeliveryDate**](DeliveryDateApi.md#getdeliverydate) | **GET** /api/v1/delivery-dates/{delivery_date_id} |  |
| [**GetDeliveryPerformance**](DeliveryDateApi.md#getdeliveryperformance) | **GET** /api/v1/delivery-dates/performance | On-time performance summary: how many promised delivery dates were met within a period. |
| [**ListDeliveryDates**](DeliveryDateApi.md#listdeliverydates) | **GET** /api/v1/delivery-dates/ |  |
| [**UpdateDeliveryDate**](DeliveryDateApi.md#updatedeliverydate) | **PUT** /api/v1/delivery-dates/{delivery_date_id} |  |
| [**UpdateDeliveryDateStatus**](DeliveryDateApi.md#updatedeliverydatestatus) | **PUT** /api/v1/delivery-dates/{delivery_date_id}/status |  |

<a id="createdeliverydate"></a>
# **CreateDeliveryDate**
> DeliveryDate CreateDeliveryDate (DeliveryDateCreate deliveryDateCreate)



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
    public class CreateDeliveryDateExample
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
            var apiInstance = new DeliveryDateApi(httpClient, config, httpClientHandler);
            var deliveryDateCreate = new DeliveryDateCreate(); // DeliveryDateCreate | 

            try
            {
                DeliveryDate result = apiInstance.CreateDeliveryDate(deliveryDateCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryDateApi.CreateDeliveryDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateDeliveryDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<DeliveryDate> response = apiInstance.CreateDeliveryDateWithHttpInfo(deliveryDateCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryDateApi.CreateDeliveryDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryDateCreate** | [**DeliveryDateCreate**](DeliveryDateCreate.md) |  |  |

### Return type

[**DeliveryDate**](DeliveryDate.md)

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

<a id="deletedeliverydate"></a>
# **DeleteDeliveryDate**
> void DeleteDeliveryDate (string deliveryDateId)



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
    public class DeleteDeliveryDateExample
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
            var apiInstance = new DeliveryDateApi(httpClient, config, httpClientHandler);
            var deliveryDateId = "deliveryDateId_example";  // string | 

            try
            {
                apiInstance.DeleteDeliveryDate(deliveryDateId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryDateApi.DeleteDeliveryDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteDeliveryDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeleteDeliveryDateWithHttpInfo(deliveryDateId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryDateApi.DeleteDeliveryDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryDateId** | **string** |  |  |

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

<a id="getdeliverydate"></a>
# **GetDeliveryDate**
> DeliveryDate GetDeliveryDate (string deliveryDateId)



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
    public class GetDeliveryDateExample
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
            var apiInstance = new DeliveryDateApi(httpClient, config, httpClientHandler);
            var deliveryDateId = "deliveryDateId_example";  // string | 

            try
            {
                DeliveryDate result = apiInstance.GetDeliveryDate(deliveryDateId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryDateApi.GetDeliveryDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDeliveryDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<DeliveryDate> response = apiInstance.GetDeliveryDateWithHttpInfo(deliveryDateId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryDateApi.GetDeliveryDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryDateId** | **string** |  |  |

### Return type

[**DeliveryDate**](DeliveryDate.md)

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

<a id="getdeliveryperformance"></a>
# **GetDeliveryPerformance**
> Object GetDeliveryPerformance (int? page = null, int? pageSize = null, string? orderNumber = null, string? status = null, DateOnly? from = null, DateOnly? to = null)

On-time performance summary: how many promised delivery dates were met within a period.

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
    public class GetDeliveryPerformanceExample
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
            var apiInstance = new DeliveryDateApi(httpClient, config, httpClientHandler);
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 
            var orderNumber = "orderNumber_example";  // string? |  (optional) 
            var status = "status_example";  // string? |  (optional) 
            var from = DateOnly.Parse("2013-10-20");  // DateOnly? | Only dates on or after this date. (optional) 
            var to = DateOnly.Parse("2013-10-20");  // DateOnly? | Only dates on or before this date. (optional) 

            try
            {
                // On-time performance summary: how many promised delivery dates were met within a period.
                Object result = apiInstance.GetDeliveryPerformance(page, pageSize, orderNumber, status, from, to);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryDateApi.GetDeliveryPerformance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDeliveryPerformanceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // On-time performance summary: how many promised delivery dates were met within a period.
    ApiResponse<Object> response = apiInstance.GetDeliveryPerformanceWithHttpInfo(page, pageSize, orderNumber, status, from, to);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryDateApi.GetDeliveryPerformanceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |
| **orderNumber** | **string?** |  | [optional]  |
| **status** | **string?** |  | [optional]  |
| **from** | **DateOnly?** | Only dates on or after this date. | [optional]  |
| **to** | **DateOnly?** | Only dates on or before this date. | [optional]  |

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
| **200** | OK |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listdeliverydates"></a>
# **ListDeliveryDates**
> List&lt;DeliveryDate&gt; ListDeliveryDates (int? page = null, int? pageSize = null, string? orderNumber = null, string? status = null, DateOnly? from = null, DateOnly? to = null)



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
    public class ListDeliveryDatesExample
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
            var apiInstance = new DeliveryDateApi(httpClient, config, httpClientHandler);
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 
            var orderNumber = "orderNumber_example";  // string? |  (optional) 
            var status = "status_example";  // string? |  (optional) 
            var from = DateOnly.Parse("2013-10-20");  // DateOnly? | Only dates on or after this date. (optional) 
            var to = DateOnly.Parse("2013-10-20");  // DateOnly? | Only dates on or before this date. (optional) 

            try
            {
                List<DeliveryDate> result = apiInstance.ListDeliveryDates(page, pageSize, orderNumber, status, from, to);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryDateApi.ListDeliveryDates: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListDeliveryDatesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<DeliveryDate>> response = apiInstance.ListDeliveryDatesWithHttpInfo(page, pageSize, orderNumber, status, from, to);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryDateApi.ListDeliveryDatesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |
| **orderNumber** | **string?** |  | [optional]  |
| **status** | **string?** |  | [optional]  |
| **from** | **DateOnly?** | Only dates on or after this date. | [optional]  |
| **to** | **DateOnly?** | Only dates on or before this date. | [optional]  |

### Return type

[**List&lt;DeliveryDate&gt;**](DeliveryDate.md)

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

<a id="updatedeliverydate"></a>
# **UpdateDeliveryDate**
> DeliveryDate UpdateDeliveryDate (string deliveryDateId, Object body)



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
    public class UpdateDeliveryDateExample
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
            var apiInstance = new DeliveryDateApi(httpClient, config, httpClientHandler);
            var deliveryDateId = "deliveryDateId_example";  // string | 
            var body = null;  // Object | 

            try
            {
                DeliveryDate result = apiInstance.UpdateDeliveryDate(deliveryDateId, body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryDateApi.UpdateDeliveryDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateDeliveryDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<DeliveryDate> response = apiInstance.UpdateDeliveryDateWithHttpInfo(deliveryDateId, body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryDateApi.UpdateDeliveryDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryDateId** | **string** |  |  |
| **body** | **Object** |  |  |

### Return type

[**DeliveryDate**](DeliveryDate.md)

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

<a id="updatedeliverydatestatus"></a>
# **UpdateDeliveryDateStatus**
> DeliveryDate UpdateDeliveryDateStatus (string deliveryDateId, DeliveryDateStatusUpdate deliveryDateStatusUpdate)



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
    public class UpdateDeliveryDateStatusExample
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
            var apiInstance = new DeliveryDateApi(httpClient, config, httpClientHandler);
            var deliveryDateId = "deliveryDateId_example";  // string | 
            var deliveryDateStatusUpdate = new DeliveryDateStatusUpdate(); // DeliveryDateStatusUpdate | 

            try
            {
                DeliveryDate result = apiInstance.UpdateDeliveryDateStatus(deliveryDateId, deliveryDateStatusUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveryDateApi.UpdateDeliveryDateStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateDeliveryDateStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<DeliveryDate> response = apiInstance.UpdateDeliveryDateStatusWithHttpInfo(deliveryDateId, deliveryDateStatusUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveryDateApi.UpdateDeliveryDateStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryDateId** | **string** |  |  |
| **deliveryDateStatusUpdate** | [**DeliveryDateStatusUpdate**](DeliveryDateStatusUpdate.md) |  |  |

### Return type

[**DeliveryDate**](DeliveryDate.md)

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

