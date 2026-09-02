# Org.OpenAPITools.Api.GenerateQrcodeApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GenerateQrcodeApi**](GenerateQrcodeApi.md#generateqrcodeapi) | **GET** /api/v1/invoices/{id}/qrcode |  |

<a id="generateqrcodeapi"></a>
# **GenerateQrcodeApi**
> QRCodeResponse GenerateQrcodeApi (string iban, string id, string? holderName = null, string? bic = null, string? amount = null, string? reference = null, string? purpose = null)



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
    public class GenerateQrcodeApiExample
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
            var apiInstance = new GenerateQrcodeApi(httpClient, config, httpClientHandler);
            var iban = "iban_example";  // string | 
            var id = "id_example";  // string | 
            var holderName = "holderName_example";  // string? |  (optional) 
            var bic = "bic_example";  // string? |  (optional) 
            var amount = "amount_example";  // string? |  (optional) 
            var reference = "reference_example";  // string? |  (optional) 
            var purpose = "purpose_example";  // string? |  (optional) 

            try
            {
                QRCodeResponse result = apiInstance.GenerateQrcodeApi(iban, id, holderName, bic, amount, reference, purpose);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GenerateQrcodeApi.GenerateQrcodeApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GenerateQrcodeApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<QRCodeResponse> response = apiInstance.GenerateQrcodeApiWithHttpInfo(iban, id, holderName, bic, amount, reference, purpose);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GenerateQrcodeApi.GenerateQrcodeApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **iban** | **string** |  |  |
| **id** | **string** |  |  |
| **holderName** | **string?** |  | [optional]  |
| **bic** | **string?** |  | [optional]  |
| **amount** | **string?** |  | [optional]  |
| **reference** | **string?** |  | [optional]  |
| **purpose** | **string?** |  | [optional]  |

### Return type

[**QRCodeResponse**](QRCodeResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | QR Code for invoice payment |  -  |
| **404** | Invoice not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

