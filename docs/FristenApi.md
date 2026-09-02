# Org.OpenAPITools.Api.FristenApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FristenApi**](FristenApi.md#fristenapi) | **GET** /api/v1/bookkeeping/fristen |  |

<a id="fristenapi"></a>
# **FristenApi**
> FristenErgebnis FristenApi (string? bundesland = null, string? voranmeldungsrhythmus = null, bool? dauerfristverlaengerung = null, bool? estAktiv = null, bool? gewstAktiv = null, int? monate = null)



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
    public class FristenApiExample
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
            var apiInstance = new FristenApi(httpClient, config, httpClientHandler);
            var bundesland = "bundesland_example";  // string? |  (optional) 
            var voranmeldungsrhythmus = "voranmeldungsrhythmus_example";  // string? |  (optional) 
            var dauerfristverlaengerung = true;  // bool? |  (optional) 
            var estAktiv = true;  // bool? |  (optional) 
            var gewstAktiv = true;  // bool? |  (optional) 
            var monate = 56;  // int? |  (optional) 

            try
            {
                FristenErgebnis result = apiInstance.FristenApi(bundesland, voranmeldungsrhythmus, dauerfristverlaengerung, estAktiv, gewstAktiv, monate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FristenApi.FristenApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FristenApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<FristenErgebnis> response = apiInstance.FristenApiWithHttpInfo(bundesland, voranmeldungsrhythmus, dauerfristverlaengerung, estAktiv, gewstAktiv, monate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FristenApi.FristenApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **bundesland** | **string?** |  | [optional]  |
| **voranmeldungsrhythmus** | **string?** |  | [optional]  |
| **dauerfristverlaengerung** | **bool?** |  | [optional]  |
| **estAktiv** | **bool?** |  | [optional]  |
| **gewstAktiv** | **bool?** |  | [optional]  |
| **monate** | **int?** |  | [optional]  |

### Return type

[**FristenErgebnis**](FristenErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Steuerliche Fristen |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

