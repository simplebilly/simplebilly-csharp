# Org.OpenAPITools.Api.SuitabilityApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ShippingSuitabilityApi**](SuitabilityApi.md#shippingsuitabilityapi) | **POST** /api/v1/shipping/suitability |  |

<a id="shippingsuitabilityapi"></a>
# **ShippingSuitabilityApi**
> SuitabilityResult ShippingSuitabilityApi (SuitabilityRequest suitabilityRequest)



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
    public class ShippingSuitabilityApiExample
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
            var apiInstance = new SuitabilityApi(httpClient, config, httpClientHandler);
            var suitabilityRequest = new SuitabilityRequest(); // SuitabilityRequest | 

            try
            {
                SuitabilityResult result = apiInstance.ShippingSuitabilityApi(suitabilityRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SuitabilityApi.ShippingSuitabilityApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ShippingSuitabilityApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<SuitabilityResult> response = apiInstance.ShippingSuitabilityApiWithHttpInfo(suitabilityRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SuitabilityApi.ShippingSuitabilityApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **suitabilityRequest** | [**SuitabilityRequest**](SuitabilityRequest.md) |  |  |

### Return type

[**SuitabilityResult**](SuitabilityResult.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Shipping suitability results |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

