# Org.OpenAPITools.Api.TimeEntriesApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ClockInTimeEntry**](TimeEntriesApi.md#clockintimeentry) | **POST** /api/v1/time-entries | Clock in for the authenticated user (resolved via their employee profile). |
| [**ClockOutTimeEntry**](TimeEntriesApi.md#clockouttimeentry) | **PATCH** /api/v1/time-entries/{id} | Clock out an entry: the entry&#39;s owner, or anyone with &#x60;time_entries:write&#x60;. |
| [**GetLaborCosts**](TimeEntriesApi.md#getlaborcosts) | **GET** /api/v1/labor-costs | Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee&#39;s hourly cost rate. |
| [**ListTimeEntries**](TimeEntriesApi.md#listtimeentries) | **GET** /api/v1/time-entries | List time entries with optional date-range / active / employee filters. |

<a id="clockintimeentry"></a>
# **ClockInTimeEntry**
> TimeEntryDto ClockInTimeEntry (TimeEntryClockIn timeEntryClockIn)

Clock in for the authenticated user (resolved via their employee profile).

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
    public class ClockInTimeEntryExample
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
            var apiInstance = new TimeEntriesApi(httpClient, config, httpClientHandler);
            var timeEntryClockIn = new TimeEntryClockIn(); // TimeEntryClockIn | 

            try
            {
                // Clock in for the authenticated user (resolved via their employee profile).
                TimeEntryDto result = apiInstance.ClockInTimeEntry(timeEntryClockIn);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TimeEntriesApi.ClockInTimeEntry: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ClockInTimeEntryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Clock in for the authenticated user (resolved via their employee profile).
    ApiResponse<TimeEntryDto> response = apiInstance.ClockInTimeEntryWithHttpInfo(timeEntryClockIn);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TimeEntriesApi.ClockInTimeEntryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **timeEntryClockIn** | [**TimeEntryClockIn**](TimeEntryClockIn.md) |  |  |

### Return type

[**TimeEntryDto**](TimeEntryDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | No employee profile for this user |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="clockouttimeentry"></a>
# **ClockOutTimeEntry**
> TimeEntryDto ClockOutTimeEntry (Guid id, TimeEntryClockOut timeEntryClockOut)

Clock out an entry: the entry's owner, or anyone with `time_entries:write`.

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
    public class ClockOutTimeEntryExample
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
            var apiInstance = new TimeEntriesApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // Guid | 
            var timeEntryClockOut = new TimeEntryClockOut(); // TimeEntryClockOut | 

            try
            {
                // Clock out an entry: the entry's owner, or anyone with `time_entries:write`.
                TimeEntryDto result = apiInstance.ClockOutTimeEntry(id, timeEntryClockOut);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TimeEntriesApi.ClockOutTimeEntry: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ClockOutTimeEntryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Clock out an entry: the entry's owner, or anyone with `time_entries:write`.
    ApiResponse<TimeEntryDto> response = apiInstance.ClockOutTimeEntryWithHttpInfo(id, timeEntryClockOut);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TimeEntriesApi.ClockOutTimeEntryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **Guid** |  |  |
| **timeEntryClockOut** | [**TimeEntryClockOut**](TimeEntryClockOut.md) |  |  |

### Return type

[**TimeEntryDto**](TimeEntryDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad request |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getlaborcosts"></a>
# **GetLaborCosts**
> List&lt;LaborCostRow&gt; GetLaborCosts (DateOnly from, DateOnly to, string groupBy)

Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee's hourly cost rate.

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
    public class GetLaborCostsExample
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
            var apiInstance = new TimeEntriesApi(httpClient, config, httpClientHandler);
            var from = DateOnly.Parse("2013-10-20");  // DateOnly | 
            var to = DateOnly.Parse("2013-10-20");  // DateOnly | 
            var groupBy = "groupBy_example";  // string | One of \"employee\", \"order\" or \"day\".

            try
            {
                // Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee's hourly cost rate.
                List<LaborCostRow> result = apiInstance.GetLaborCosts(from, to, groupBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TimeEntriesApi.GetLaborCosts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetLaborCostsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee's hourly cost rate.
    ApiResponse<List<LaborCostRow>> response = apiInstance.GetLaborCostsWithHttpInfo(from, to, groupBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TimeEntriesApi.GetLaborCostsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **from** | **DateOnly** |  |  |
| **to** | **DateOnly** |  |  |
| **groupBy** | **string** | One of \&quot;employee\&quot;, \&quot;order\&quot; or \&quot;day\&quot;. |  |

### Return type

[**List&lt;LaborCostRow&gt;**](LaborCostRow.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtimeentries"></a>
# **ListTimeEntries**
> List&lt;TimeEntryDto&gt; ListTimeEntries (DateOnly? from = null, DateOnly? to = null, bool? active = null, Guid? employeeId = null)

List time entries with optional date-range / active / employee filters.

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
    public class ListTimeEntriesExample
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
            var apiInstance = new TimeEntriesApi(httpClient, config, httpClientHandler);
            var from = DateOnly.Parse("2013-10-20");  // DateOnly? |  (optional) 
            var to = DateOnly.Parse("2013-10-20");  // DateOnly? |  (optional) 
            var active = true;  // bool? | Only currently running shifts (clock_in set, clock_out null). (optional) 
            var employeeId = "employeeId_example";  // Guid? |  (optional) 

            try
            {
                // List time entries with optional date-range / active / employee filters.
                List<TimeEntryDto> result = apiInstance.ListTimeEntries(from, to, active, employeeId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TimeEntriesApi.ListTimeEntries: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTimeEntriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List time entries with optional date-range / active / employee filters.
    ApiResponse<List<TimeEntryDto>> response = apiInstance.ListTimeEntriesWithHttpInfo(from, to, active, employeeId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TimeEntriesApi.ListTimeEntriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **from** | **DateOnly?** |  | [optional]  |
| **to** | **DateOnly?** |  | [optional]  |
| **active** | **bool?** | Only currently running shifts (clock_in set, clock_out null). | [optional]  |
| **employeeId** | **Guid?** |  | [optional]  |

### Return type

[**List&lt;TimeEntryDto&gt;**](TimeEntryDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

