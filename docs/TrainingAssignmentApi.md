# Org.OpenAPITools.Api.TrainingAssignmentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateTrainingAssignment**](TrainingAssignmentApi.md#createtrainingassignment) | **POST** /api/v1/training-assignments |  |
| [**DeleteTrainingAssignment**](TrainingAssignmentApi.md#deletetrainingassignment) | **DELETE** /api/v1/training-assignments/{id} |  |
| [**GetTrainingAssignment**](TrainingAssignmentApi.md#gettrainingassignment) | **GET** /api/v1/training-assignments/{id} |  |
| [**GetTrainingAssignments**](TrainingAssignmentApi.md#gettrainingassignments) | **GET** /api/v1/training-assignments/ |  |
| [**UpdateTrainingAssignment**](TrainingAssignmentApi.md#updatetrainingassignment) | **PUT** /api/v1/training-assignments/{id} |  |

<a id="createtrainingassignment"></a>
# **CreateTrainingAssignment**
> TrainingAssignment CreateTrainingAssignment (TrainingAssignmentCreate trainingAssignmentCreate)



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
    public class CreateTrainingAssignmentExample
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
            var apiInstance = new TrainingAssignmentApi(httpClient, config, httpClientHandler);
            var trainingAssignmentCreate = new TrainingAssignmentCreate(); // TrainingAssignmentCreate | 

            try
            {
                TrainingAssignment result = apiInstance.CreateTrainingAssignment(trainingAssignmentCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrainingAssignmentApi.CreateTrainingAssignment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTrainingAssignmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<TrainingAssignment> response = apiInstance.CreateTrainingAssignmentWithHttpInfo(trainingAssignmentCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrainingAssignmentApi.CreateTrainingAssignmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **trainingAssignmentCreate** | [**TrainingAssignmentCreate**](TrainingAssignmentCreate.md) |  |  |

### Return type

[**TrainingAssignment**](TrainingAssignment.md)

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

<a id="deletetrainingassignment"></a>
# **DeleteTrainingAssignment**
> void DeleteTrainingAssignment (Guid id)



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
    public class DeleteTrainingAssignmentExample
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
            var apiInstance = new TrainingAssignmentApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // Guid | 

            try
            {
                apiInstance.DeleteTrainingAssignment(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrainingAssignmentApi.DeleteTrainingAssignment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTrainingAssignmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeleteTrainingAssignmentWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrainingAssignmentApi.DeleteTrainingAssignmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **Guid** |  |  |

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

<a id="gettrainingassignment"></a>
# **GetTrainingAssignment**
> TrainingAssignment GetTrainingAssignment (Guid id)



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
    public class GetTrainingAssignmentExample
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
            var apiInstance = new TrainingAssignmentApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // Guid | 

            try
            {
                TrainingAssignment result = apiInstance.GetTrainingAssignment(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrainingAssignmentApi.GetTrainingAssignment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTrainingAssignmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<TrainingAssignment> response = apiInstance.GetTrainingAssignmentWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrainingAssignmentApi.GetTrainingAssignmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **Guid** |  |  |

### Return type

[**TrainingAssignment**](TrainingAssignment.md)

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

<a id="gettrainingassignments"></a>
# **GetTrainingAssignments**
> List&lt;TrainingAssignment&gt; GetTrainingAssignments (int? page = null, int? pageSize = null, string? search = null, bool? includeDeleted = null)



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
    public class GetTrainingAssignmentsExample
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
            var apiInstance = new TrainingAssignmentApi(httpClient, config, httpClientHandler);
            var page = 1;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 
            var search = "search_example";  // string? |  (optional) 
            var includeDeleted = true;  // bool? | Soft-delete entities: set true to include rows with `deleted_at` set. (optional) 

            try
            {
                List<TrainingAssignment> result = apiInstance.GetTrainingAssignments(page, pageSize, search, includeDeleted);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrainingAssignmentApi.GetTrainingAssignments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTrainingAssignmentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<TrainingAssignment>> response = apiInstance.GetTrainingAssignmentsWithHttpInfo(page, pageSize, search, includeDeleted);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrainingAssignmentApi.GetTrainingAssignmentsWithHttpInfo: " + e.Message);
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

[**List&lt;TrainingAssignment&gt;**](TrainingAssignment.md)

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

<a id="updatetrainingassignment"></a>
# **UpdateTrainingAssignment**
> TrainingAssignment UpdateTrainingAssignment (Guid id, TrainingAssignmentUpdate trainingAssignmentUpdate)



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
    public class UpdateTrainingAssignmentExample
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
            var apiInstance = new TrainingAssignmentApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // Guid | 
            var trainingAssignmentUpdate = new TrainingAssignmentUpdate(); // TrainingAssignmentUpdate | 

            try
            {
                TrainingAssignment result = apiInstance.UpdateTrainingAssignment(id, trainingAssignmentUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrainingAssignmentApi.UpdateTrainingAssignment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTrainingAssignmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<TrainingAssignment> response = apiInstance.UpdateTrainingAssignmentWithHttpInfo(id, trainingAssignmentUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrainingAssignmentApi.UpdateTrainingAssignmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **Guid** |  |  |
| **trainingAssignmentUpdate** | [**TrainingAssignmentUpdate**](TrainingAssignmentUpdate.md) |  |  |

### Return type

[**TrainingAssignment**](TrainingAssignment.md)

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

