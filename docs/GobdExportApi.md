# Org.OpenAPITools.Api.GobdExportApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BuchhalterCsvApi**](GobdExportApi.md#buchhaltercsvapi) | **GET** /api/v1/bookkeeping/buchhalter-csv |  |
| [**GobdExportApi**](GobdExportApi.md#gobdexportapi) | **GET** /api/v1/bookkeeping/gobd | GoBD/GDPdU export. Default: ZIP archive (&#x60;index.xml&#x60; + CSV tables, IDEA format). &#x60;?format&#x3D;csv&#x60; returns the legacy single-journal CSV as JSON. |

<a id="buchhaltercsvapi"></a>
# **BuchhalterCsvApi**
> GoBDExportResponse BuchhalterCsvApi (string dateFrom, string dateTo)



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
    public class BuchhalterCsvApiExample
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
            var apiInstance = new GobdExportApi(httpClient, config, httpClientHandler);
            var dateFrom = "dateFrom_example";  // string | 
            var dateTo = "dateTo_example";  // string | 

            try
            {
                GoBDExportResponse result = apiInstance.BuchhalterCsvApi(dateFrom, dateTo);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GobdExportApi.BuchhalterCsvApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BuchhalterCsvApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<GoBDExportResponse> response = apiInstance.BuchhalterCsvApiWithHttpInfo(dateFrom, dateTo);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GobdExportApi.BuchhalterCsvApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dateFrom** | **string** |  |  |
| **dateTo** | **string** |  |  |

### Return type

[**GoBDExportResponse**](GoBDExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Buchhalter CSV |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gobdexportapi"></a>
# **GobdExportApi**
> void GobdExportApi (int year, string? format = null)

GoBD/GDPdU export. Default: ZIP archive (`index.xml` + CSV tables, IDEA format). `?format=csv` returns the legacy single-journal CSV as JSON.

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
    public class GobdExportApiExample
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
            var apiInstance = new GobdExportApi(httpClient, config, httpClientHandler);
            var year = 56;  // int | 
            var format = zip;  // string? | Export format: `zip` (default, full GDPdU/IDEA export) or `csv` (legacy single-journal CSV as JSON). (optional) 

            try
            {
                // GoBD/GDPdU export. Default: ZIP archive (`index.xml` + CSV tables, IDEA format). `?format=csv` returns the legacy single-journal CSV as JSON.
                apiInstance.GobdExportApi(year, format);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GobdExportApi.GobdExportApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GobdExportApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // GoBD/GDPdU export. Default: ZIP archive (`index.xml` + CSV tables, IDEA format). `?format=csv` returns the legacy single-journal CSV as JSON.
    apiInstance.GobdExportApiWithHttpInfo(year, format);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GobdExportApi.GobdExportApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **year** | **int** |  |  |
| **format** | **string?** | Export format: &#x60;zip&#x60; (default, full GDPdU/IDEA export) or &#x60;csv&#x60; (legacy single-journal CSV as JSON). | [optional]  |

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/zip, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | GoBD/GDPdU export: ZIP (application/zip) with index.xml (IDEA table specification) and one UTF-8 CSV per tax-relevant table; legacy single-journal CSV JSON via ?format&#x3D;csv |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

