# Org.OpenAPITools.Api.PlausibilityApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**PlausibilityCheckApi**](PlausibilityApi.md#plausibilitycheckapi) | **GET** /api/v1/bookkeeping/plausibility |  |

<a id="plausibilitycheckapi"></a>
# **PlausibilityCheckApi**
> PlausibilityReport PlausibilityCheckApi (string? dateFrom = null, string? dateTo = null)



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
    public class PlausibilityCheckApiExample
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
            var apiInstance = new PlausibilityApi(httpClient, config, httpClientHandler);
            var dateFrom = "dateFrom_example";  // string? |  (optional) 
            var dateTo = "dateTo_example";  // string? |  (optional) 

            try
            {
                PlausibilityReport result = apiInstance.PlausibilityCheckApi(dateFrom, dateTo);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PlausibilityApi.PlausibilityCheckApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PlausibilityCheckApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<PlausibilityReport> response = apiInstance.PlausibilityCheckApiWithHttpInfo(dateFrom, dateTo);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PlausibilityApi.PlausibilityCheckApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dateFrom** | **string?** |  | [optional]  |
| **dateTo** | **string?** |  | [optional]  |

### Return type

[**PlausibilityReport**](PlausibilityReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Plausibility report |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

