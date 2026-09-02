# Org.OpenAPITools.Api.ReportsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BilanzReportApi**](ReportsApi.md#bilanzreportapi) | **GET** /api/v1/bookkeeping/reports/bilanz | Bilanz (Balance Sheet) |
| [**GuvReportApi**](ReportsApi.md#guvreportapi) | **GET** /api/v1/bookkeeping/reports/guv | Gewinn- und Verlustrechnung (P&amp;L statement) |
| [**KontenansichtReportApi**](ReportsApi.md#kontenansichtreportapi) | **GET** /api/v1/bookkeeping/reports/kontenansicht | Kontenansicht (Account Overview) |
| [**UmsatzsteuerReportApi**](ReportsApi.md#umsatzsteuerreportapi) | **GET** /api/v1/bookkeeping/reports/umsatzsteuer | Umsatzsteuer-Voranmeldung (VAT report) |

<a id="bilanzreportapi"></a>
# **BilanzReportApi**
> BilanzReport BilanzReportApi (int? year = null, int? month = null, string? dateFrom = null, string? dateTo = null, int? page = null, int? pageSize = null)

Bilanz (Balance Sheet)

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
    public class BilanzReportApiExample
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
            var apiInstance = new ReportsApi(httpClient, config, httpClientHandler);
            var year = 56;  // int? |  (optional) 
            var month = 56;  // int? |  (optional) 
            var dateFrom = "dateFrom_example";  // string? |  (optional) 
            var dateTo = "dateTo_example";  // string? |  (optional) 
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 

            try
            {
                // Bilanz (Balance Sheet)
                BilanzReport result = apiInstance.BilanzReportApi(year, month, dateFrom, dateTo, page, pageSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportsApi.BilanzReportApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BilanzReportApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Bilanz (Balance Sheet)
    ApiResponse<BilanzReport> response = apiInstance.BilanzReportApiWithHttpInfo(year, month, dateFrom, dateTo, page, pageSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportsApi.BilanzReportApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **year** | **int?** |  | [optional]  |
| **month** | **int?** |  | [optional]  |
| **dateFrom** | **string?** |  | [optional]  |
| **dateTo** | **string?** |  | [optional]  |
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |

### Return type

[**BilanzReport**](BilanzReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Balance sheet |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="guvreportapi"></a>
# **GuvReportApi**
> GuVReport GuvReportApi (int? year = null, int? month = null, string? dateFrom = null, string? dateTo = null, int? page = null, int? pageSize = null)

Gewinn- und Verlustrechnung (P&L statement)

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
    public class GuvReportApiExample
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
            var apiInstance = new ReportsApi(httpClient, config, httpClientHandler);
            var year = 56;  // int? |  (optional) 
            var month = 56;  // int? |  (optional) 
            var dateFrom = "dateFrom_example";  // string? |  (optional) 
            var dateTo = "dateTo_example";  // string? |  (optional) 
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 

            try
            {
                // Gewinn- und Verlustrechnung (P&L statement)
                GuVReport result = apiInstance.GuvReportApi(year, month, dateFrom, dateTo, page, pageSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportsApi.GuvReportApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GuvReportApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gewinn- und Verlustrechnung (P&L statement)
    ApiResponse<GuVReport> response = apiInstance.GuvReportApiWithHttpInfo(year, month, dateFrom, dateTo, page, pageSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportsApi.GuvReportApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **year** | **int?** |  | [optional]  |
| **month** | **int?** |  | [optional]  |
| **dateFrom** | **string?** |  | [optional]  |
| **dateTo** | **string?** |  | [optional]  |
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |

### Return type

[**GuVReport**](GuVReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | GuV report |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="kontenansichtreportapi"></a>
# **KontenansichtReportApi**
> KontoReport KontenansichtReportApi (int? year = null, int? month = null, string? dateFrom = null, string? dateTo = null, int? page = null, int? pageSize = null)

Kontenansicht (Account Overview)

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
    public class KontenansichtReportApiExample
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
            var apiInstance = new ReportsApi(httpClient, config, httpClientHandler);
            var year = 56;  // int? |  (optional) 
            var month = 56;  // int? |  (optional) 
            var dateFrom = "dateFrom_example";  // string? |  (optional) 
            var dateTo = "dateTo_example";  // string? |  (optional) 
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 

            try
            {
                // Kontenansicht (Account Overview)
                KontoReport result = apiInstance.KontenansichtReportApi(year, month, dateFrom, dateTo, page, pageSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportsApi.KontenansichtReportApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the KontenansichtReportApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Kontenansicht (Account Overview)
    ApiResponse<KontoReport> response = apiInstance.KontenansichtReportApiWithHttpInfo(year, month, dateFrom, dateTo, page, pageSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportsApi.KontenansichtReportApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **year** | **int?** |  | [optional]  |
| **month** | **int?** |  | [optional]  |
| **dateFrom** | **string?** |  | [optional]  |
| **dateTo** | **string?** |  | [optional]  |
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |

### Return type

[**KontoReport**](KontoReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account overview |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="umsatzsteuerreportapi"></a>
# **UmsatzsteuerReportApi**
> UmsatzsteuerReport UmsatzsteuerReportApi (int? year = null, int? month = null, string? dateFrom = null, string? dateTo = null, int? page = null, int? pageSize = null)

Umsatzsteuer-Voranmeldung (VAT report)

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
    public class UmsatzsteuerReportApiExample
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
            var apiInstance = new ReportsApi(httpClient, config, httpClientHandler);
            var year = 56;  // int? |  (optional) 
            var month = 56;  // int? |  (optional) 
            var dateFrom = "dateFrom_example";  // string? |  (optional) 
            var dateTo = "dateTo_example";  // string? |  (optional) 
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 

            try
            {
                // Umsatzsteuer-Voranmeldung (VAT report)
                UmsatzsteuerReport result = apiInstance.UmsatzsteuerReportApi(year, month, dateFrom, dateTo, page, pageSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportsApi.UmsatzsteuerReportApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UmsatzsteuerReportApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Umsatzsteuer-Voranmeldung (VAT report)
    ApiResponse<UmsatzsteuerReport> response = apiInstance.UmsatzsteuerReportApiWithHttpInfo(year, month, dateFrom, dateTo, page, pageSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportsApi.UmsatzsteuerReportApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **year** | **int?** |  | [optional]  |
| **month** | **int?** |  | [optional]  |
| **dateFrom** | **string?** |  | [optional]  |
| **dateTo** | **string?** |  | [optional]  |
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |

### Return type

[**UmsatzsteuerReport**](UmsatzsteuerReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | VAT report |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

