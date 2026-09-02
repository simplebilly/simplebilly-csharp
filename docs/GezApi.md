# Org.OpenAPITools.Api.GezApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GezApi**](GezApi.md#gezapi) | **GET** /api/v1/bookkeeping/gez |  |

<a id="gezapi"></a>
# **GezApi**
> GezReport GezApi (int? jahr = null, string? betriebsstaetten = null, long? kfz = null, long? hotelzimmer = null, long? beschaefigte = null)



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
    public class GezApiExample
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
            var apiInstance = new GezApi(httpClient, config, httpClientHandler);
            var jahr = 56;  // int? |  (optional) 
            var betriebsstaetten = "betriebsstaetten_example";  // string? | Liste der Betriebsstätten als JSON, z.B. `[{\"name\":\"Filiale 1\",\"beschaefigte\":12}]`. (optional) 
            var kfz = 789L;  // long? | Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind). (optional) 
            var hotelzimmer = 789L;  // long? | Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen. (optional) 
            var beschaefigte = 789L;  // long? | Gesamtzahl der Beschäftigten (verwendet nur, wenn `betriebsstaetten` fehlt; dann wird eine einzelne Betriebsstätte angenommen). (optional) 

            try
            {
                GezReport result = apiInstance.GezApi(jahr, betriebsstaetten, kfz, hotelzimmer, beschaefigte);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GezApi.GezApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GezApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<GezReport> response = apiInstance.GezApiWithHttpInfo(jahr, betriebsstaetten, kfz, hotelzimmer, beschaefigte);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GezApi.GezApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **jahr** | **int?** |  | [optional]  |
| **betriebsstaetten** | **string?** | Liste der Betriebsstätten als JSON, z.B. &#x60;[{\&quot;name\&quot;:\&quot;Filiale 1\&quot;,\&quot;beschaefigte\&quot;:12}]&#x60;. | [optional]  |
| **kfz** | **long?** | Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind). | [optional]  |
| **hotelzimmer** | **long?** | Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen. | [optional]  |
| **beschaefigte** | **long?** | Gesamtzahl der Beschäftigten (verwendet nur, wenn &#x60;betriebsstaetten&#x60; fehlt; dann wird eine einzelne Betriebsstätte angenommen). | [optional]  |

### Return type

[**GezReport**](GezReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rundfunkbeitrag (GEZ) Berechnung nach § 5 RBStV |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

