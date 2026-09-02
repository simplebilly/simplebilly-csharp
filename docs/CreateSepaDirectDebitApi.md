# Org.OpenAPITools.Api.CreateSepaDirectDebitApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateSepaDirectDebitApi**](CreateSepaDirectDebitApi.md#createsepadirectdebitapi) | **POST** /api/v1/bookkeeping/sepa-direct-debit |  |

<a id="createsepadirectdebitapi"></a>
# **CreateSepaDirectDebitApi**
> SepaDirectDebitResponse CreateSepaDirectDebitApi (string creditorName, string creditorIban, string creditorId, string mandateId, string mandateDate, string debtorName, string debtorIban, string amount, string collectionDate, string? creditorBic = null, string? debtorBic = null, string? description = null)



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
    public class CreateSepaDirectDebitApiExample
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
            var apiInstance = new CreateSepaDirectDebitApi(httpClient, config, httpClientHandler);
            var creditorName = "creditorName_example";  // string | 
            var creditorIban = "creditorIban_example";  // string | 
            var creditorId = "creditorId_example";  // string | 
            var mandateId = "mandateId_example";  // string | 
            var mandateDate = "mandateDate_example";  // string | 
            var debtorName = "debtorName_example";  // string | 
            var debtorIban = "debtorIban_example";  // string | 
            var amount = "amount_example";  // string | 
            var collectionDate = "collectionDate_example";  // string | 
            var creditorBic = "creditorBic_example";  // string? |  (optional) 
            var debtorBic = "debtorBic_example";  // string? |  (optional) 
            var description = "description_example";  // string? |  (optional) 

            try
            {
                SepaDirectDebitResponse result = apiInstance.CreateSepaDirectDebitApi(creditorName, creditorIban, creditorId, mandateId, mandateDate, debtorName, debtorIban, amount, collectionDate, creditorBic, debtorBic, description);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreateSepaDirectDebitApi.CreateSepaDirectDebitApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateSepaDirectDebitApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<SepaDirectDebitResponse> response = apiInstance.CreateSepaDirectDebitApiWithHttpInfo(creditorName, creditorIban, creditorId, mandateId, mandateDate, debtorName, debtorIban, amount, collectionDate, creditorBic, debtorBic, description);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreateSepaDirectDebitApi.CreateSepaDirectDebitApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **creditorName** | **string** |  |  |
| **creditorIban** | **string** |  |  |
| **creditorId** | **string** |  |  |
| **mandateId** | **string** |  |  |
| **mandateDate** | **string** |  |  |
| **debtorName** | **string** |  |  |
| **debtorIban** | **string** |  |  |
| **amount** | **string** |  |  |
| **collectionDate** | **string** |  |  |
| **creditorBic** | **string?** |  | [optional]  |
| **debtorBic** | **string?** |  | [optional]  |
| **description** | **string?** |  | [optional]  |

### Return type

[**SepaDirectDebitResponse**](SepaDirectDebitResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | SEPA Direct Debit XML |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

