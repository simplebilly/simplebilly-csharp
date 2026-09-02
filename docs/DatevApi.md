# Org.OpenAPITools.Api.DatevApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DatevExportApi**](DatevApi.md#datevexportapi) | **GET** /api/v1/bookkeeping/datev/export | Export bookkeeping data as DATEV CSV |
| [**DatevPreviewApi**](DatevApi.md#datevpreviewapi) | **GET** /api/v1/bookkeeping/datev/preview | Exported_datev_bookings: returns formed bookings for review |

<a id="datevexportapi"></a>
# **DatevExportApi**
> DatevExportResponse DatevExportApi (string? accountSchema = null, string? dateFrom = null, string? dateTo = null, int? page = null, int? pageSize = null)

Export bookkeeping data as DATEV CSV

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
    public class DatevExportApiExample
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
            var apiInstance = new DatevApi(httpClient, config, httpClientHandler);
            var accountSchema = "accountSchema_example";  // string? |  (optional) 
            var dateFrom = "dateFrom_example";  // string? |  (optional) 
            var dateTo = "dateTo_example";  // string? |  (optional) 
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 

            try
            {
                // Export bookkeeping data as DATEV CSV
                DatevExportResponse result = apiInstance.DatevExportApi(accountSchema, dateFrom, dateTo, page, pageSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DatevApi.DatevExportApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DatevExportApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Export bookkeeping data as DATEV CSV
    ApiResponse<DatevExportResponse> response = apiInstance.DatevExportApiWithHttpInfo(accountSchema, dateFrom, dateTo, page, pageSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DatevApi.DatevExportApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountSchema** | **string?** |  | [optional]  |
| **dateFrom** | **string?** |  | [optional]  |
| **dateTo** | **string?** |  | [optional]  |
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |

### Return type

[**DatevExportResponse**](DatevExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | DATEV CSV export |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="datevpreviewapi"></a>
# **DatevPreviewApi**
> List&lt;DatevBookingPreview&gt; DatevPreviewApi (string? accountSchema = null, string? dateFrom = null, string? dateTo = null, int? page = null, int? pageSize = null)

Exported_datev_bookings: returns formed bookings for review

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
    public class DatevPreviewApiExample
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
            var apiInstance = new DatevApi(httpClient, config, httpClientHandler);
            var accountSchema = "accountSchema_example";  // string? |  (optional) 
            var dateFrom = "dateFrom_example";  // string? |  (optional) 
            var dateTo = "dateTo_example";  // string? |  (optional) 
            var page = 56;  // int? |  (optional) 
            var pageSize = 56;  // int? |  (optional) 

            try
            {
                // Exported_datev_bookings: returns formed bookings for review
                List<DatevBookingPreview> result = apiInstance.DatevPreviewApi(accountSchema, dateFrom, dateTo, page, pageSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DatevApi.DatevPreviewApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DatevPreviewApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Exported_datev_bookings: returns formed bookings for review
    ApiResponse<List<DatevBookingPreview>> response = apiInstance.DatevPreviewApiWithHttpInfo(accountSchema, dateFrom, dateTo, page, pageSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DatevApi.DatevPreviewApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountSchema** | **string?** |  | [optional]  |
| **dateFrom** | **string?** |  | [optional]  |
| **dateTo** | **string?** |  | [optional]  |
| **page** | **int?** |  | [optional]  |
| **pageSize** | **int?** |  | [optional]  |

### Return type

[**List&lt;DatevBookingPreview&gt;**](DatevBookingPreview.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | DATEV booking preview |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

