# Org.OpenAPITools.Api.SupplierConditionApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateSupplierCondition**](SupplierConditionApi.md#createsuppliercondition) | **POST** /api/v1/supplier-conditions |  |
| [**DeleteSupplierCondition**](SupplierConditionApi.md#deletesuppliercondition) | **DELETE** /api/v1/supplier-conditions/{supplier_condition_id} |  |
| [**GetSupplierCondition**](SupplierConditionApi.md#getsuppliercondition) | **GET** /api/v1/supplier-conditions/{supplier_condition_id} |  |
| [**ListSupplierConditions**](SupplierConditionApi.md#listsupplierconditions) | **GET** /api/v1/supplier-conditions/ |  |
| [**UpdateSupplierCondition**](SupplierConditionApi.md#updatesuppliercondition) | **PUT** /api/v1/supplier-conditions/{supplier_condition_id} |  |

<a id="createsuppliercondition"></a>
# **CreateSupplierCondition**
> SupplierCondition CreateSupplierCondition (SupplierConditionCreate supplierConditionCreate)



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
    public class CreateSupplierConditionExample
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
            var apiInstance = new SupplierConditionApi(httpClient, config, httpClientHandler);
            var supplierConditionCreate = new SupplierConditionCreate(); // SupplierConditionCreate | 

            try
            {
                SupplierCondition result = apiInstance.CreateSupplierCondition(supplierConditionCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupplierConditionApi.CreateSupplierCondition: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateSupplierConditionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<SupplierCondition> response = apiInstance.CreateSupplierConditionWithHttpInfo(supplierConditionCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupplierConditionApi.CreateSupplierConditionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **supplierConditionCreate** | [**SupplierConditionCreate**](SupplierConditionCreate.md) |  |  |

### Return type

[**SupplierCondition**](SupplierCondition.md)

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

<a id="deletesuppliercondition"></a>
# **DeleteSupplierCondition**
> void DeleteSupplierCondition (string supplierConditionId)



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
    public class DeleteSupplierConditionExample
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
            var apiInstance = new SupplierConditionApi(httpClient, config, httpClientHandler);
            var supplierConditionId = "supplierConditionId_example";  // string | 

            try
            {
                apiInstance.DeleteSupplierCondition(supplierConditionId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupplierConditionApi.DeleteSupplierCondition: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteSupplierConditionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeleteSupplierConditionWithHttpInfo(supplierConditionId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupplierConditionApi.DeleteSupplierConditionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **supplierConditionId** | **string** |  |  |

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

<a id="getsuppliercondition"></a>
# **GetSupplierCondition**
> SupplierCondition GetSupplierCondition (string supplierConditionId)



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
    public class GetSupplierConditionExample
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
            var apiInstance = new SupplierConditionApi(httpClient, config, httpClientHandler);
            var supplierConditionId = "supplierConditionId_example";  // string | 

            try
            {
                SupplierCondition result = apiInstance.GetSupplierCondition(supplierConditionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupplierConditionApi.GetSupplierCondition: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSupplierConditionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<SupplierCondition> response = apiInstance.GetSupplierConditionWithHttpInfo(supplierConditionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupplierConditionApi.GetSupplierConditionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **supplierConditionId** | **string** |  |  |

### Return type

[**SupplierCondition**](SupplierCondition.md)

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

<a id="listsupplierconditions"></a>
# **ListSupplierConditions**
> List&lt;SupplierCondition&gt; ListSupplierConditions (int? page = null, int? pageSize = null, string? supplierContactId = null, string? search = null)



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
    public class ListSupplierConditionsExample
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
            var apiInstance = new SupplierConditionApi(httpClient, config, httpClientHandler);
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 
            var supplierContactId = "supplierContactId_example";  // string? |  (optional) 
            var search = "search_example";  // string? |  (optional) 

            try
            {
                List<SupplierCondition> result = apiInstance.ListSupplierConditions(page, pageSize, supplierContactId, search);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupplierConditionApi.ListSupplierConditions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListSupplierConditionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<SupplierCondition>> response = apiInstance.ListSupplierConditionsWithHttpInfo(page, pageSize, supplierContactId, search);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupplierConditionApi.ListSupplierConditionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |
| **supplierContactId** | **string?** |  | [optional]  |
| **search** | **string?** |  | [optional]  |

### Return type

[**List&lt;SupplierCondition&gt;**](SupplierCondition.md)

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

<a id="updatesuppliercondition"></a>
# **UpdateSupplierCondition**
> SupplierCondition UpdateSupplierCondition (string supplierConditionId, SupplierConditionUpdate supplierConditionUpdate)



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
    public class UpdateSupplierConditionExample
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
            var apiInstance = new SupplierConditionApi(httpClient, config, httpClientHandler);
            var supplierConditionId = "supplierConditionId_example";  // string | 
            var supplierConditionUpdate = new SupplierConditionUpdate(); // SupplierConditionUpdate | 

            try
            {
                SupplierCondition result = apiInstance.UpdateSupplierCondition(supplierConditionId, supplierConditionUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SupplierConditionApi.UpdateSupplierCondition: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateSupplierConditionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<SupplierCondition> response = apiInstance.UpdateSupplierConditionWithHttpInfo(supplierConditionId, supplierConditionUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SupplierConditionApi.UpdateSupplierConditionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **supplierConditionId** | **string** |  |  |
| **supplierConditionUpdate** | [**SupplierConditionUpdate**](SupplierConditionUpdate.md) |  |  |

### Return type

[**SupplierCondition**](SupplierCondition.md)

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

