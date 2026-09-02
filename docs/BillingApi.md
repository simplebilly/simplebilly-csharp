# Org.OpenAPITools.Api.BillingApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetPlans**](BillingApi.md#getplans) | **GET** /api/v1/plans | All canonical plans (free/starter/business/enterprise) — the single source of truth lives in &#x60;crate::saasy::plans&#x60;, matching marketing. |
| [**GetQuotaApi**](BillingApi.md#getquotaapi) | **GET** /api/v1/quota | Effective limits + current usage for the calling tenant. |
| [**GetSubscriptionApi**](BillingApi.md#getsubscriptionapi) | **GET** /api/v1/subscription |  |
| [**GetUsageApi**](BillingApi.md#getusageapi) | **GET** /api/v1/usage |  |
| [**PaddleSubscriptionWebhook**](BillingApi.md#paddlesubscriptionwebhook) | **POST** /api/webhooks/paddle/subscription | Paddle Billing subscription webhook. Verifies the &#x60;Paddle-Signature&#x60; header (HMAC-SHA256 over &#x60;\&quot;{ts}:{raw_body}\&quot;&#x60; with the webhook secret), then updates &#x60;billing_info&#x60; and &#x60;tenants.plan&#x60; for the tenant identified by the subscription &#x60;custom_data&#x60; (JSON &#x60;{\&quot;tenant_id\&quot;: \&quot;...\&quot;}&#x60; or a bare tenant UUID). |
| [**PutQuotaApi**](BillingApi.md#putquotaapi) | **PUT** /api/v1/quota | Write the per-tenant quota override (&#x60;admin:settings&#x60;). An empty object clears the override. |

<a id="getplans"></a>
# **GetPlans**
> ApiResponseVecPlan GetPlans ()

All canonical plans (free/starter/business/enterprise) — the single source of truth lives in `crate::saasy::plans`, matching marketing.

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
    public class GetPlansExample
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
            var apiInstance = new BillingApi(httpClient, config, httpClientHandler);

            try
            {
                // All canonical plans (free/starter/business/enterprise) — the single source of truth lives in `crate::saasy::plans`, matching marketing.
                ApiResponseVecPlan result = apiInstance.GetPlans();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BillingApi.GetPlans: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPlansWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // All canonical plans (free/starter/business/enterprise) — the single source of truth lives in `crate::saasy::plans`, matching marketing.
    ApiResponse<ApiResponseVecPlan> response = apiInstance.GetPlansWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BillingApi.GetPlansWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ApiResponseVecPlan**](ApiResponseVecPlan.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | All subscription plans |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getquotaapi"></a>
# **GetQuotaApi**
> void GetQuotaApi ()

Effective limits + current usage for the calling tenant.

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
    public class GetQuotaApiExample
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
            var apiInstance = new BillingApi(httpClient, config, httpClientHandler);

            try
            {
                // Effective limits + current usage for the calling tenant.
                apiInstance.GetQuotaApi();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BillingApi.GetQuotaApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetQuotaApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Effective limits + current usage for the calling tenant.
    apiInstance.GetQuotaApiWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BillingApi.GetQuotaApiWithHttpInfo: " + e.Message);
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
| **200** | Effective limits and current usage |  -  |
| **404** | Tenant not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getsubscriptionapi"></a>
# **GetSubscriptionApi**
> ApiResponseSubscriptionOverview GetSubscriptionApi ()



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
    public class GetSubscriptionApiExample
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
            var apiInstance = new BillingApi(httpClient, config, httpClientHandler);

            try
            {
                ApiResponseSubscriptionOverview result = apiInstance.GetSubscriptionApi();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BillingApi.GetSubscriptionApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSubscriptionApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<ApiResponseSubscriptionOverview> response = apiInstance.GetSubscriptionApiWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BillingApi.GetSubscriptionApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ApiResponseSubscriptionOverview**](ApiResponseSubscriptionOverview.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tenant subscription overview |  -  |
| **404** | Tenant not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getusageapi"></a>
# **GetUsageApi**
> void GetUsageApi (string? meter = null)



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
    public class GetUsageApiExample
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
            var apiInstance = new BillingApi(httpClient, config, httpClientHandler);
            var meter = "meter_example";  // string? |  (optional) 

            try
            {
                apiInstance.GetUsageApi(meter);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BillingApi.GetUsageApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetUsageApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.GetUsageApiWithHttpInfo(meter);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BillingApi.GetUsageApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **meter** | **string?** |  | [optional]  |

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
| **200** | Metered usage this period |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="paddlesubscriptionwebhook"></a>
# **PaddleSubscriptionWebhook**
> void PaddleSubscriptionWebhook ()

Paddle Billing subscription webhook. Verifies the `Paddle-Signature` header (HMAC-SHA256 over `\"{ts}:{raw_body}\"` with the webhook secret), then updates `billing_info` and `tenants.plan` for the tenant identified by the subscription `custom_data` (JSON `{\"tenant_id\": \"...\"}` or a bare tenant UUID).

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
    public class PaddleSubscriptionWebhookExample
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
            var apiInstance = new BillingApi(httpClient, config, httpClientHandler);

            try
            {
                // Paddle Billing subscription webhook. Verifies the `Paddle-Signature` header (HMAC-SHA256 over `\"{ts}:{raw_body}\"` with the webhook secret), then updates `billing_info` and `tenants.plan` for the tenant identified by the subscription `custom_data` (JSON `{\"tenant_id\": \"...\"}` or a bare tenant UUID).
                apiInstance.PaddleSubscriptionWebhook();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BillingApi.PaddleSubscriptionWebhook: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PaddleSubscriptionWebhookWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Paddle Billing subscription webhook. Verifies the `Paddle-Signature` header (HMAC-SHA256 over `\"{ts}:{raw_body}\"` with the webhook secret), then updates `billing_info` and `tenants.plan` for the tenant identified by the subscription `custom_data` (JSON `{\"tenant_id\": \"...\"}` or a bare tenant UUID).
    apiInstance.PaddleSubscriptionWebhookWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BillingApi.PaddleSubscriptionWebhookWithHttpInfo: " + e.Message);
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
| **200** | Webhook processed |  -  |
| **401** | Signature verification failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="putquotaapi"></a>
# **PutQuotaApi**
> void PutQuotaApi (QuotaOverride quotaOverride)

Write the per-tenant quota override (`admin:settings`). An empty object clears the override.

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
    public class PutQuotaApiExample
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
            var apiInstance = new BillingApi(httpClient, config, httpClientHandler);
            var quotaOverride = new QuotaOverride(); // QuotaOverride | 

            try
            {
                // Write the per-tenant quota override (`admin:settings`). An empty object clears the override.
                apiInstance.PutQuotaApi(quotaOverride);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BillingApi.PutQuotaApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PutQuotaApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Write the per-tenant quota override (`admin:settings`). An empty object clears the override.
    apiInstance.PutQuotaApiWithHttpInfo(quotaOverride);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BillingApi.PutQuotaApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **quotaOverride** | [**QuotaOverride**](QuotaOverride.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Override saved, effective limits returned |  -  |
| **403** | Missing admin:settings permission |  -  |
| **404** | Tenant not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

