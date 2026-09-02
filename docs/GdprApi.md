# Org.OpenAPITools.Api.GdprApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AcceptDpa**](GdprApi.md#acceptdpa) | **PUT** /api/v1/gdpr/dpa | Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing). |
| [**AccountErasure**](GdprApi.md#accounterasure) | **POST** /api/v1/gdpr/account-erasure | Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination). |
| [**ErasureContact**](GdprApi.md#erasurecontact) | **POST** /api/v1/gdpr/erasure/{contact_id} | Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on &#x60;contacts&#x60; already records who/when. |
| [**ExportContactData**](GdprApi.md#exportcontactdata) | **GET** /api/v1/gdpr/export/{contact_id} | Art. 15 data-subject access export for a contact. |
| [**ExportGdpr**](GdprApi.md#exportgdpr) | **GET** /api/v1/gdpr/export | Export the current user&#39;s personal data (GDPR Art. 15/20). |
| [**GetDpa**](GdprApi.md#getdpa) | **GET** /api/v1/gdpr/dpa | Current DPA acceptance status (from tenant_settings). |

<a id="acceptdpa"></a>
# **AcceptDpa**
> DpaStatus AcceptDpa (DpaAcceptRequest dpaAcceptRequest)

Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing).

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
    public class AcceptDpaExample
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
            var apiInstance = new GdprApi(httpClient, config, httpClientHandler);
            var dpaAcceptRequest = new DpaAcceptRequest(); // DpaAcceptRequest | 

            try
            {
                // Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing).
                DpaStatus result = apiInstance.AcceptDpa(dpaAcceptRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GdprApi.AcceptDpa: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AcceptDpaWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing).
    ApiResponse<DpaStatus> response = apiInstance.AcceptDpaWithHttpInfo(dpaAcceptRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GdprApi.AcceptDpaWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dpaAcceptRequest** | [**DpaAcceptRequest**](DpaAcceptRequest.md) |  |  |

### Return type

[**DpaStatus**](DpaStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | DPA acceptance recorded |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="accounterasure"></a>
# **AccountErasure**
> Object AccountErasure ()

Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination).

Anonymizes every contact, anonymizes personal fields on bookkeeping records (orders/invoices/payments keep amounts and dates for GoBD), removes the tenant linkage of the (global, saasy-framework) users and marks the erasure on `tenant_settings.gdpr_erased_at`. No row is physically deleted. The audit triggers on the touched tables record who/when.

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
    public class AccountErasureExample
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
            var apiInstance = new GdprApi(httpClient, config, httpClientHandler);

            try
            {
                // Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination).
                Object result = apiInstance.AccountErasure();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GdprApi.AccountErasure: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AccountErasureWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination).
    ApiResponse<Object> response = apiInstance.AccountErasureWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GdprApi.AccountErasureWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tenant personal data anonymized |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="erasurecontact"></a>
# **ErasureContact**
> Object ErasureContact (string contactId)

Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on `contacts` already records who/when.

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
    public class ErasureContactExample
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
            var apiInstance = new GdprApi(httpClient, config, httpClientHandler);
            var contactId = "contactId_example";  // string | 

            try
            {
                // Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on `contacts` already records who/when.
                Object result = apiInstance.ErasureContact(contactId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GdprApi.ErasureContact: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ErasureContactWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on `contacts` already records who/when.
    ApiResponse<Object> response = apiInstance.ErasureContactWithHttpInfo(contactId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GdprApi.ErasureContactWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **contactId** | **string** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Contact anonymized |  -  |
| **404** | Contact not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="exportcontactdata"></a>
# **ExportContactData**
> Object ExportContactData (string contactId)

Art. 15 data-subject access export for a contact.

Returns the contact itself plus the tenant-scoped rows linked to it.  ## Relations The `customers`/`orders`/`invoices`/`payments` tables have no FK to `contacts`; they are linked through the `customer_id` column, which per the app's conventions holds one of: - the admin customer's `customer_id` (a UUID, often the same value as   the contact's `contact_id`/`customer_number`), - the buyer's email for shop orders, or - the marketplace's external customer id for plugin orders.  The export therefore matches the contact's identifiers (`contact_id`, `customer_number`, `external_id`, `email`) plus any resolved customer ids against `customer_id`. `delivery_notes` and `customer_communications` reference contacts directly via `contact_id`. Soft-deleted rows are included (their data is still processed and retained for GoBD). Relations that genuinely do not exist for a contact stay empty but the key is always present.

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
    public class ExportContactDataExample
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
            var apiInstance = new GdprApi(httpClient, config, httpClientHandler);
            var contactId = "contactId_example";  // string | 

            try
            {
                // Art. 15 data-subject access export for a contact.
                Object result = apiInstance.ExportContactData(contactId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GdprApi.ExportContactData: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExportContactDataWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Art. 15 data-subject access export for a contact.
    ApiResponse<Object> response = apiInstance.ExportContactDataWithHttpInfo(contactId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GdprApi.ExportContactDataWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **contactId** | **string** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Art. 15 data-subject export |  -  |
| **404** | Contact not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="exportgdpr"></a>
# **ExportGdpr**
> ApiResponseGdprExport ExportGdpr ()

Export the current user's personal data (GDPR Art. 15/20).

No admin permission required: a user always exports their own data.

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
    public class ExportGdprExample
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
            var apiInstance = new GdprApi(httpClient, config, httpClientHandler);

            try
            {
                // Export the current user's personal data (GDPR Art. 15/20).
                ApiResponseGdprExport result = apiInstance.ExportGdpr();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GdprApi.ExportGdpr: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExportGdprWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Export the current user's personal data (GDPR Art. 15/20).
    ApiResponse<ApiResponseGdprExport> response = apiInstance.ExportGdprWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GdprApi.ExportGdprWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ApiResponseGdprExport**](ApiResponseGdprExport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Personal data export |  -  |
| **404** | User not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getdpa"></a>
# **GetDpa**
> DpaStatus GetDpa ()

Current DPA acceptance status (from tenant_settings).

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
    public class GetDpaExample
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
            var apiInstance = new GdprApi(httpClient, config, httpClientHandler);

            try
            {
                // Current DPA acceptance status (from tenant_settings).
                DpaStatus result = apiInstance.GetDpa();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GdprApi.GetDpa: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDpaWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Current DPA acceptance status (from tenant_settings).
    ApiResponse<DpaStatus> response = apiInstance.GetDpaWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GdprApi.GetDpaWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**DpaStatus**](DpaStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | DPA acceptance status |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

