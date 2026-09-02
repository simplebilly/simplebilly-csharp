# Org.OpenAPITools.Api.EbilanzApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**EbilanzReportApi**](EbilanzApi.md#ebilanzreportapi) | **GET** /api/v1/bookkeeping/ebilanz |  |
| [**EbilanzXbrlExportApi**](EbilanzApi.md#ebilanzxbrlexportapi) | **GET** /api/v1/bookkeeping/ebilanz/xbrl |  |

<a id="ebilanzreportapi"></a>
# **EbilanzReportApi**
> EBilanzReport EbilanzReportApi (int? year = null, string? dateFrom = null, string? dateTo = null)



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
    public class EbilanzReportApiExample
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
            var apiInstance = new EbilanzApi(httpClient, config, httpClientHandler);
            var year = 56;  // int? |  (optional) 
            var dateFrom = "dateFrom_example";  // string? |  (optional) 
            var dateTo = "dateTo_example";  // string? |  (optional) 

            try
            {
                EBilanzReport result = apiInstance.EbilanzReportApi(year, dateFrom, dateTo);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EbilanzApi.EbilanzReportApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbilanzReportApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<EBilanzReport> response = apiInstance.EbilanzReportApiWithHttpInfo(year, dateFrom, dateTo);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EbilanzApi.EbilanzReportApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **year** | **int?** |  | [optional]  |
| **dateFrom** | **string?** |  | [optional]  |
| **dateTo** | **string?** |  | [optional]  |

### Return type

[**EBilanzReport**](EBilanzReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | E-Bilanz report |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="ebilanzxbrlexportapi"></a>
# **EbilanzXbrlExportApi**
> void EbilanzXbrlExportApi (int? year = null, string? dateFrom = null, string? dateTo = null)



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
    public class EbilanzXbrlExportApiExample
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
            var apiInstance = new EbilanzApi(httpClient, config, httpClientHandler);
            var year = 56;  // int? |  (optional) 
            var dateFrom = "dateFrom_example";  // string? |  (optional) 
            var dateTo = "dateTo_example";  // string? |  (optional) 

            try
            {
                apiInstance.EbilanzXbrlExportApi(year, dateFrom, dateTo);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EbilanzApi.EbilanzXbrlExportApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbilanzXbrlExportApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.EbilanzXbrlExportApiWithHttpInfo(year, dateFrom, dateTo);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EbilanzApi.EbilanzXbrlExportApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **year** | **int?** |  | [optional]  |
| **dateFrom** | **string?** |  | [optional]  |
| **dateTo** | **string?** |  | [optional]  |

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | XBRL XML content |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

