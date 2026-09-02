# Org.OpenAPITools.Api.BookkeepingApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AllocatePaymentApi**](BookkeepingApi.md#allocatepaymentapi) | **POST** /api/v1/payments/allocate | Allocate a payment to an invoice |
| [**BwaReportApi**](BookkeepingApi.md#bwareportapi) | **GET** /api/v1/bookkeeping/bwa | Get BWA (Betriebswirtschaftliche Auswertung) report |
| [**ElsterStatusApi**](BookkeepingApi.md#elsterstatusapi) | **GET** /api/v1/bookkeeping/elster/status |  |
| [**ElsterValidateApi**](BookkeepingApi.md#elstervalidateapi) | **POST** /api/v1/bookkeeping/ustva/elster-validate |  |
| [**ElsterXmlApi**](BookkeepingApi.md#elsterxmlapi) | **GET** /api/v1/bookkeeping/ustva/elster-xml |  |
| [**GetCashflow**](BookkeepingApi.md#getcashflow) | **GET** /api/v1/bookkeeping/cashflow | GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period. |
| [**GetLiquidity**](BookkeepingApi.md#getliquidity) | **GET** /api/v1/bookkeeping/liquidity | GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios. |
| [**GetOpenInvoicesApi**](BookkeepingApi.md#getopeninvoicesapi) | **GET** /api/v1/payments/open-invoices/{customer_id} | Get open invoices for a customer |
| [**GetVerfahrensdokumentation**](BookkeepingApi.md#getverfahrensdokumentation) | **GET** /api/v1/bookkeeping/verfahrensdokumentation | GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules. |
| [**RunDunningApi**](BookkeepingApi.md#rundunningapi) | **POST** /api/v1/bookkeeping/dunning |  |

<a id="allocatepaymentapi"></a>
# **AllocatePaymentApi**
> void AllocatePaymentApi (AllocatePaymentRequest allocatePaymentRequest)

Allocate a payment to an invoice

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
    public class AllocatePaymentApiExample
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
            var apiInstance = new BookkeepingApi(httpClient, config, httpClientHandler);
            var allocatePaymentRequest = new AllocatePaymentRequest(); // AllocatePaymentRequest | 

            try
            {
                // Allocate a payment to an invoice
                apiInstance.AllocatePaymentApi(allocatePaymentRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookkeepingApi.AllocatePaymentApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AllocatePaymentApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Allocate a payment to an invoice
    apiInstance.AllocatePaymentApiWithHttpInfo(allocatePaymentRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookkeepingApi.AllocatePaymentApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **allocatePaymentRequest** | [**AllocatePaymentRequest**](AllocatePaymentRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payment allocated successfully |  -  |
| **400** | Invalid request |  -  |
| **404** | Payment or invoice not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="bwareportapi"></a>
# **BwaReportApi**
> BWAReport BwaReportApi (int? year = null, int? month = null)

Get BWA (Betriebswirtschaftliche Auswertung) report

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
    public class BwaReportApiExample
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
            var apiInstance = new BookkeepingApi(httpClient, config, httpClientHandler);
            var year = 56;  // int? |  (optional) 
            var month = 56;  // int? |  (optional) 

            try
            {
                // Get BWA (Betriebswirtschaftliche Auswertung) report
                BWAReport result = apiInstance.BwaReportApi(year, month);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookkeepingApi.BwaReportApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BwaReportApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get BWA (Betriebswirtschaftliche Auswertung) report
    ApiResponse<BWAReport> response = apiInstance.BwaReportApiWithHttpInfo(year, month);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookkeepingApi.BwaReportApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **year** | **int?** |  | [optional]  |
| **month** | **int?** |  | [optional]  |

### Return type

[**BWAReport**](BWAReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | BWA Report |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="elsterstatusapi"></a>
# **ElsterStatusApi**
> ElsterStatus ElsterStatusApi ()



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
    public class ElsterStatusApiExample
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
            var apiInstance = new BookkeepingApi(httpClient, config, httpClientHandler);

            try
            {
                ElsterStatus result = apiInstance.ElsterStatusApi();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookkeepingApi.ElsterStatusApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ElsterStatusApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<ElsterStatus> response = apiInstance.ElsterStatusApiWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookkeepingApi.ElsterStatusApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ElsterStatus**](ElsterStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | ELSTER integration status |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="elstervalidateapi"></a>
# **ElsterValidateApi**
> void ElsterValidateApi (string zeitraum)



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
    public class ElsterValidateApiExample
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
            var apiInstance = new BookkeepingApi(httpClient, config, httpClientHandler);
            var zeitraum = "zeitraum_example";  // string | 

            try
            {
                apiInstance.ElsterValidateApi(zeitraum);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookkeepingApi.ElsterValidateApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ElsterValidateApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.ElsterValidateApiWithHttpInfo(zeitraum);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookkeepingApi.ElsterValidateApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **zeitraum** | **string** |  |  |

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
| **200** | Validate UStVA XML (mock or ERiC) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="elsterxmlapi"></a>
# **ElsterXmlApi**
> void ElsterXmlApi (string zeitraum)



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
    public class ElsterXmlApiExample
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
            var apiInstance = new BookkeepingApi(httpClient, config, httpClientHandler);
            var zeitraum = "zeitraum_example";  // string | 

            try
            {
                apiInstance.ElsterXmlApi(zeitraum);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookkeepingApi.ElsterXmlApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ElsterXmlApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.ElsterXmlApiWithHttpInfo(zeitraum);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookkeepingApi.ElsterXmlApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **zeitraum** | **string** |  |  |

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
| **200** | ELSTER UStVA XML template (manual upload) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcashflow"></a>
# **GetCashflow**
> CashflowReport GetCashflow (int? year = null, int? month = null)

GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.

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
    public class GetCashflowExample
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
            var apiInstance = new BookkeepingApi(httpClient, config, httpClientHandler);
            var year = 56;  // int? |  (optional) 
            var month = 56;  // int? |  (optional) 

            try
            {
                // GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.
                CashflowReport result = apiInstance.GetCashflow(year, month);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookkeepingApi.GetCashflow: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCashflowWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.
    ApiResponse<CashflowReport> response = apiInstance.GetCashflowWithHttpInfo(year, month);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookkeepingApi.GetCashflowWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **year** | **int?** |  | [optional]  |
| **month** | **int?** |  | [optional]  |

### Return type

[**CashflowReport**](CashflowReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Cashflow report |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getliquidity"></a>
# **GetLiquidity**
> LiquidityPosition GetLiquidity ()

GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.

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
    public class GetLiquidityExample
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
            var apiInstance = new BookkeepingApi(httpClient, config, httpClientHandler);

            try
            {
                // GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.
                LiquidityPosition result = apiInstance.GetLiquidity();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookkeepingApi.GetLiquidity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetLiquidityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.
    ApiResponse<LiquidityPosition> response = apiInstance.GetLiquidityWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookkeepingApi.GetLiquidityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**LiquidityPosition**](LiquidityPosition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Liquidity position |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getopeninvoicesapi"></a>
# **GetOpenInvoicesApi**
> List&lt;Invoice&gt; GetOpenInvoicesApi (string customerId)

Get open invoices for a customer

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
    public class GetOpenInvoicesApiExample
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
            var apiInstance = new BookkeepingApi(httpClient, config, httpClientHandler);
            var customerId = "customerId_example";  // string | 

            try
            {
                // Get open invoices for a customer
                List<Invoice> result = apiInstance.GetOpenInvoicesApi(customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookkeepingApi.GetOpenInvoicesApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetOpenInvoicesApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get open invoices for a customer
    ApiResponse<List<Invoice>> response = apiInstance.GetOpenInvoicesApiWithHttpInfo(customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookkeepingApi.GetOpenInvoicesApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **string** |  |  |

### Return type

[**List&lt;Invoice&gt;**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Open invoices list |  -  |
| **404** | Customer not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getverfahrensdokumentation"></a>
# **GetVerfahrensdokumentation**
> Verfahrensdokumentation GetVerfahrensdokumentation ()

GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.

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
    public class GetVerfahrensdokumentationExample
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
            var apiInstance = new BookkeepingApi(httpClient, config, httpClientHandler);

            try
            {
                // GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.
                Verfahrensdokumentation result = apiInstance.GetVerfahrensdokumentation();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookkeepingApi.GetVerfahrensdokumentation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetVerfahrensdokumentationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.
    ApiResponse<Verfahrensdokumentation> response = apiInstance.GetVerfahrensdokumentationWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookkeepingApi.GetVerfahrensdokumentationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**Verfahrensdokumentation**](Verfahrensdokumentation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Verfahrensdokumentation |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="rundunningapi"></a>
# **RunDunningApi**
> DunningResult RunDunningApi ()



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
    public class RunDunningApiExample
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
            var apiInstance = new BookkeepingApi(httpClient, config, httpClientHandler);

            try
            {
                DunningResult result = apiInstance.RunDunningApi();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookkeepingApi.RunDunningApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RunDunningApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<DunningResult> response = apiInstance.RunDunningApiWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookkeepingApi.RunDunningApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**DunningResult**](DunningResult.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Dunning run completed successfully |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

