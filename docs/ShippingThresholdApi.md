# Org.OpenAPITools.Api.ShippingThresholdApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateShippingThreshold**](ShippingThresholdApi.md#createshippingthreshold) | **POST** /api/v1/shipping-thresholds |  |
| [**DeleteShippingThreshold**](ShippingThresholdApi.md#deleteshippingthreshold) | **DELETE** /api/v1/shipping-thresholds/{threshold_id} |  |
| [**GetDeliverable**](ShippingThresholdApi.md#getdeliverable) | **GET** /api/v1/shipping-thresholds/deliverable |  |
| [**GetShippingThreshold**](ShippingThresholdApi.md#getshippingthreshold) | **GET** /api/v1/shipping-thresholds/{threshold_id} |  |
| [**ListShippingThresholds**](ShippingThresholdApi.md#listshippingthresholds) | **GET** /api/v1/shipping-thresholds/ |  |
| [**UpdateShippingThreshold**](ShippingThresholdApi.md#updateshippingthreshold) | **PUT** /api/v1/shipping-thresholds/{threshold_id} |  |

<a id="createshippingthreshold"></a>
# **CreateShippingThreshold**
> ShippingThreshold CreateShippingThreshold (ShippingThresholdCreate shippingThresholdCreate)



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
    public class CreateShippingThresholdExample
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
            var apiInstance = new ShippingThresholdApi(httpClient, config, httpClientHandler);
            var shippingThresholdCreate = new ShippingThresholdCreate(); // ShippingThresholdCreate | 

            try
            {
                ShippingThreshold result = apiInstance.CreateShippingThreshold(shippingThresholdCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ShippingThresholdApi.CreateShippingThreshold: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateShippingThresholdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<ShippingThreshold> response = apiInstance.CreateShippingThresholdWithHttpInfo(shippingThresholdCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ShippingThresholdApi.CreateShippingThresholdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **shippingThresholdCreate** | [**ShippingThresholdCreate**](ShippingThresholdCreate.md) |  |  |

### Return type

[**ShippingThreshold**](ShippingThreshold.md)

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

<a id="deleteshippingthreshold"></a>
# **DeleteShippingThreshold**
> void DeleteShippingThreshold (string thresholdId)



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
    public class DeleteShippingThresholdExample
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
            var apiInstance = new ShippingThresholdApi(httpClient, config, httpClientHandler);
            var thresholdId = "thresholdId_example";  // string | 

            try
            {
                apiInstance.DeleteShippingThreshold(thresholdId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ShippingThresholdApi.DeleteShippingThreshold: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteShippingThresholdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeleteShippingThresholdWithHttpInfo(thresholdId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ShippingThresholdApi.DeleteShippingThresholdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **thresholdId** | **string** |  |  |

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

<a id="getdeliverable"></a>
# **GetDeliverable**
> DeliverableResponse GetDeliverable (Guid productId, string? warehouseId = null)



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
    public class GetDeliverableExample
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
            var apiInstance = new ShippingThresholdApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // Guid | 
            var warehouseId = "warehouseId_example";  // string? |  (optional) 

            try
            {
                DeliverableResponse result = apiInstance.GetDeliverable(productId, warehouseId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ShippingThresholdApi.GetDeliverable: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDeliverableWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<DeliverableResponse> response = apiInstance.GetDeliverableWithHttpInfo(productId, warehouseId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ShippingThresholdApi.GetDeliverableWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **Guid** |  |  |
| **warehouseId** | **string?** |  | [optional]  |

### Return type

[**DeliverableResponse**](DeliverableResponse.md)

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

<a id="getshippingthreshold"></a>
# **GetShippingThreshold**
> ShippingThreshold GetShippingThreshold (string thresholdId)



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
    public class GetShippingThresholdExample
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
            var apiInstance = new ShippingThresholdApi(httpClient, config, httpClientHandler);
            var thresholdId = "thresholdId_example";  // string | 

            try
            {
                ShippingThreshold result = apiInstance.GetShippingThreshold(thresholdId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ShippingThresholdApi.GetShippingThreshold: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetShippingThresholdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<ShippingThreshold> response = apiInstance.GetShippingThresholdWithHttpInfo(thresholdId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ShippingThresholdApi.GetShippingThresholdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **thresholdId** | **string** |  |  |

### Return type

[**ShippingThreshold**](ShippingThreshold.md)

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

<a id="listshippingthresholds"></a>
# **ListShippingThresholds**
> List&lt;ShippingThreshold&gt; ListShippingThresholds (int? page = null, int? pageSize = null, Guid? productId = null, string? warehouseId = null, bool? isActive = null)



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
    public class ListShippingThresholdsExample
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
            var apiInstance = new ShippingThresholdApi(httpClient, config, httpClientHandler);
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 
            var productId = "productId_example";  // Guid? |  (optional) 
            var warehouseId = "warehouseId_example";  // string? |  (optional) 
            var isActive = true;  // bool? |  (optional) 

            try
            {
                List<ShippingThreshold> result = apiInstance.ListShippingThresholds(page, pageSize, productId, warehouseId, isActive);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ShippingThresholdApi.ListShippingThresholds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListShippingThresholdsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<ShippingThreshold>> response = apiInstance.ListShippingThresholdsWithHttpInfo(page, pageSize, productId, warehouseId, isActive);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ShippingThresholdApi.ListShippingThresholdsWithHttpInfo: " + e.Message);
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
| **isActive** | **bool?** |  | [optional]  |

### Return type

[**List&lt;ShippingThreshold&gt;**](ShippingThreshold.md)

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

<a id="updateshippingthreshold"></a>
# **UpdateShippingThreshold**
> ShippingThreshold UpdateShippingThreshold (string thresholdId, ShippingThresholdUpdate shippingThresholdUpdate)



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
    public class UpdateShippingThresholdExample
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
            var apiInstance = new ShippingThresholdApi(httpClient, config, httpClientHandler);
            var thresholdId = "thresholdId_example";  // string | 
            var shippingThresholdUpdate = new ShippingThresholdUpdate(); // ShippingThresholdUpdate | 

            try
            {
                ShippingThreshold result = apiInstance.UpdateShippingThreshold(thresholdId, shippingThresholdUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ShippingThresholdApi.UpdateShippingThreshold: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateShippingThresholdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<ShippingThreshold> response = apiInstance.UpdateShippingThresholdWithHttpInfo(thresholdId, shippingThresholdUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ShippingThresholdApi.UpdateShippingThresholdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **thresholdId** | **string** |  |  |
| **shippingThresholdUpdate** | [**ShippingThresholdUpdate**](ShippingThresholdUpdate.md) |  |  |

### Return type

[**ShippingThreshold**](ShippingThreshold.md)

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

