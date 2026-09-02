# Org.OpenAPITools.Api.ProposeAssignmentsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ProposeAssignmentsApi**](ProposeAssignmentsApi.md#proposeassignmentsapi) | **GET** /api/v1/bookkeeping/propose-assignments |  |

<a id="proposeassignmentsapi"></a>
# **ProposeAssignmentsApi**
> List&lt;ProposedAssignment&gt; ProposeAssignmentsApi (double? minConfidence = null, string? customerId = null)



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
    public class ProposeAssignmentsApiExample
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
            var apiInstance = new ProposeAssignmentsApi(httpClient, config, httpClientHandler);
            var minConfidence = 1.2D;  // double? |  (optional) 
            var customerId = "customerId_example";  // string? |  (optional) 

            try
            {
                List<ProposedAssignment> result = apiInstance.ProposeAssignmentsApi(minConfidence, customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProposeAssignmentsApi.ProposeAssignmentsApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProposeAssignmentsApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<ProposedAssignment>> response = apiInstance.ProposeAssignmentsApiWithHttpInfo(minConfidence, customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProposeAssignmentsApi.ProposeAssignmentsApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **minConfidence** | **double?** |  | [optional]  |
| **customerId** | **string?** |  | [optional]  |

### Return type

[**List&lt;ProposedAssignment&gt;**](ProposedAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Proposed payment to invoice assignments |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

