# Org.OpenAPITools.Api.ListOpenItemsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ListOpenItemsApi**](ListOpenItemsApi.md#listopenitemsapi) | **GET** /api/v1/bookkeeping/open-items |  |

<a id="listopenitemsapi"></a>
# **ListOpenItemsApi**
> List&lt;OpenItem&gt; ListOpenItemsApi (long? reminderLevel1Days = null, long? reminderLevel2Days = null, long? reminderLevel3Days = null, string? customerId = null)



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
    public class ListOpenItemsApiExample
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
            var apiInstance = new ListOpenItemsApi(httpClient, config, httpClientHandler);
            var reminderLevel1Days = 789L;  // long? |  (optional) 
            var reminderLevel2Days = 789L;  // long? |  (optional) 
            var reminderLevel3Days = 789L;  // long? |  (optional) 
            var customerId = "customerId_example";  // string? |  (optional) 

            try
            {
                List<OpenItem> result = apiInstance.ListOpenItemsApi(reminderLevel1Days, reminderLevel2Days, reminderLevel3Days, customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ListOpenItemsApi.ListOpenItemsApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListOpenItemsApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<OpenItem>> response = apiInstance.ListOpenItemsApiWithHttpInfo(reminderLevel1Days, reminderLevel2Days, reminderLevel3Days, customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ListOpenItemsApi.ListOpenItemsApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **reminderLevel1Days** | **long?** |  | [optional]  |
| **reminderLevel2Days** | **long?** |  | [optional]  |
| **reminderLevel3Days** | **long?** |  | [optional]  |
| **customerId** | **string?** |  | [optional]  |

### Return type

[**List&lt;OpenItem&gt;**](OpenItem.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of open invoices |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

