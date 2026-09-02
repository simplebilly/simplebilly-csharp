# Org.OpenAPITools.Api.GewerbesteuerApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GewerbesteuerApi**](GewerbesteuerApi.md#gewerbesteuerapi) | **GET** /api/v1/bookkeeping/gewerbesteuer |  |

<a id="gewerbesteuerapi"></a>
# **GewerbesteuerApi**
> GewerbesteuerErgebnis GewerbesteuerApi (int year, string? hebesatz = null, string? gewerbeertrag = null, string? country = null, string? gemeindeschluessel = null)



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
    public class GewerbesteuerApiExample
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
            var apiInstance = new GewerbesteuerApi(httpClient, config, httpClientHandler);
            var year = 56;  // int | 
            var hebesatz = "hebesatz_example";  // string? |  (optional) 
            var gewerbeertrag = "gewerbeertrag_example";  // string? |  (optional) 
            var country = "country_example";  // string? |  (optional) 
            var gemeindeschluessel = "gemeindeschluessel_example";  // string? |  (optional) 

            try
            {
                GewerbesteuerErgebnis result = apiInstance.GewerbesteuerApi(year, hebesatz, gewerbeertrag, country, gemeindeschluessel);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GewerbesteuerApi.GewerbesteuerApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GewerbesteuerApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<GewerbesteuerErgebnis> response = apiInstance.GewerbesteuerApiWithHttpInfo(year, hebesatz, gewerbeertrag, country, gemeindeschluessel);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GewerbesteuerApi.GewerbesteuerApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **year** | **int** |  |  |
| **hebesatz** | **string?** |  | [optional]  |
| **gewerbeertrag** | **string?** |  | [optional]  |
| **country** | **string?** |  | [optional]  |
| **gemeindeschluessel** | **string?** |  | [optional]  |

### Return type

[**GewerbesteuerErgebnis**](GewerbesteuerErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Gewerbesteuer / Trade Tax Ergebnis |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

