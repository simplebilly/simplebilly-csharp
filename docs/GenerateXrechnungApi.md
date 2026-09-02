# Org.OpenAPITools.Api.GenerateXrechnungApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GenerateXrechnungApi**](GenerateXrechnungApi.md#generatexrechnungapi) | **GET** /api/v1/invoices/{id}/xrechnung |  |

<a id="generatexrechnungapi"></a>
# **GenerateXrechnungApi**
> XRechnungResponse GenerateXrechnungApi (string id, string? supplierName = null, string? supplierStreet = null, string? supplierCity = null, string? supplierZip = null, string? supplierCountry = null, string? supplierVatId = null)



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
    public class GenerateXrechnungApiExample
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
            var apiInstance = new GenerateXrechnungApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var supplierName = "supplierName_example";  // string? |  (optional) 
            var supplierStreet = "supplierStreet_example";  // string? |  (optional) 
            var supplierCity = "supplierCity_example";  // string? |  (optional) 
            var supplierZip = "supplierZip_example";  // string? |  (optional) 
            var supplierCountry = "supplierCountry_example";  // string? |  (optional) 
            var supplierVatId = "supplierVatId_example";  // string? |  (optional) 

            try
            {
                XRechnungResponse result = apiInstance.GenerateXrechnungApi(id, supplierName, supplierStreet, supplierCity, supplierZip, supplierCountry, supplierVatId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GenerateXrechnungApi.GenerateXrechnungApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GenerateXrechnungApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<XRechnungResponse> response = apiInstance.GenerateXrechnungApiWithHttpInfo(id, supplierName, supplierStreet, supplierCity, supplierZip, supplierCountry, supplierVatId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GenerateXrechnungApi.GenerateXrechnungApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **supplierName** | **string?** |  | [optional]  |
| **supplierStreet** | **string?** |  | [optional]  |
| **supplierCity** | **string?** |  | [optional]  |
| **supplierZip** | **string?** |  | [optional]  |
| **supplierCountry** | **string?** |  | [optional]  |
| **supplierVatId** | **string?** |  | [optional]  |

### Return type

[**XRechnungResponse**](XRechnungResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | XRechnung XML |  -  |
| **404** | Invoice not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

