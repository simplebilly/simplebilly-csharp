# Org.OpenAPITools.Api.BankingApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BankLookupApi**](BankingApi.md#banklookupapi) | **GET** /api/v1/bookkeeping/banking/lookup |  |
| [**BankTransactionsApi**](BankingApi.md#banktransactionsapi) | **GET** /api/v1/bookkeeping/banking/transactions |  |
| [**HebesatzLookupApi**](BankingApi.md#hebesatzlookupapi) | **GET** /api/v1/bookkeeping/hebesatz |  |

<a id="banklookupapi"></a>
# **BankLookupApi**
> BankLookup BankLookupApi (string iban)



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
    public class BankLookupApiExample
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
            var apiInstance = new BankingApi(httpClient, config, httpClientHandler);
            var iban = "iban_example";  // string | 

            try
            {
                BankLookup result = apiInstance.BankLookupApi(iban);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BankingApi.BankLookupApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BankLookupApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<BankLookup> response = apiInstance.BankLookupApiWithHttpInfo(iban);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BankingApi.BankLookupApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **iban** | **string** |  |  |

### Return type

[**BankLookup**](BankLookup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Bank-Lookup Ergebnis |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="banktransactionsapi"></a>
# **BankTransactionsApi**
> void BankTransactionsApi ()



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
    public class BankTransactionsApiExample
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
            var apiInstance = new BankingApi(httpClient, config, httpClientHandler);

            try
            {
                apiInstance.BankTransactionsApi();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BankingApi.BankTransactionsApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BankTransactionsApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.BankTransactionsApiWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BankingApi.BankTransactionsApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Bank-Transaktionen |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="hebesatzlookupapi"></a>
# **HebesatzLookupApi**
> List&lt;HebesatzLookup&gt; HebesatzLookupApi (string? gemeindeschluessel = null, string? plz = null, string? name = null, string? stichtag = null, string? countryCode = null)



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
    public class HebesatzLookupApiExample
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
            var apiInstance = new BankingApi(httpClient, config, httpClientHandler);
            var gemeindeschluessel = "gemeindeschluessel_example";  // string? |  (optional) 
            var plz = "plz_example";  // string? |  (optional) 
            var name = "name_example";  // string? |  (optional) 
            var stichtag = "stichtag_example";  // string? | Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from <= date <= valid_to. (optional) 
            var countryCode = "countryCode_example";  // string? |  (optional) 

            try
            {
                List<HebesatzLookup> result = apiInstance.HebesatzLookupApi(gemeindeschluessel, plz, name, stichtag, countryCode);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BankingApi.HebesatzLookupApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the HebesatzLookupApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<List<HebesatzLookup>> response = apiInstance.HebesatzLookupApiWithHttpInfo(gemeindeschluessel, plz, name, stichtag, countryCode);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BankingApi.HebesatzLookupApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **gemeindeschluessel** | **string?** |  | [optional]  |
| **plz** | **string?** |  | [optional]  |
| **name** | **string?** |  | [optional]  |
| **stichtag** | **string?** | Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from &lt;&#x3D; date &lt;&#x3D; valid_to. | [optional]  |
| **countryCode** | **string?** |  | [optional]  |

### Return type

[**List&lt;HebesatzLookup&gt;**](HebesatzLookup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Hebesatz Lookup |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

