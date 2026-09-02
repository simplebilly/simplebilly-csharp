# Org.OpenAPITools.Api.LegalDocumentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetLegalDocuments**](LegalDocumentApi.md#getlegaldocuments) | **GET** /api/v1/legal/documents | List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access. |
| [**ResetLegalDocuments**](LegalDocumentApi.md#resetlegaldocuments) | **POST** /api/v1/legal/documents/reset | Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list. |
| [**UpsertLegalDocuments**](LegalDocumentApi.md#upsertlegaldocuments) | **PUT** /api/v1/legal/documents | Upsert legal documents per (doc_type, lang). Returns the full tenant list. |

<a id="getlegaldocuments"></a>
# **GetLegalDocuments**
> List&lt;LegalDocument&gt; GetLegalDocuments ()

List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.

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
    public class GetLegalDocumentsExample
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
            var apiInstance = new LegalDocumentApi(httpClient, config, httpClientHandler);

            try
            {
                // List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.
                List<LegalDocument> result = apiInstance.GetLegalDocuments();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LegalDocumentApi.GetLegalDocuments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetLegalDocumentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.
    ApiResponse<List<LegalDocument>> response = apiInstance.GetLegalDocumentsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LegalDocumentApi.GetLegalDocumentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;LegalDocument&gt;**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | All legal documents of the tenant |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="resetlegaldocuments"></a>
# **ResetLegalDocuments**
> List&lt;LegalDocument&gt; ResetLegalDocuments (LegalDocumentReset legalDocumentReset)

Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.

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
    public class ResetLegalDocumentsExample
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
            var apiInstance = new LegalDocumentApi(httpClient, config, httpClientHandler);
            var legalDocumentReset = new LegalDocumentReset(); // LegalDocumentReset | 

            try
            {
                // Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.
                List<LegalDocument> result = apiInstance.ResetLegalDocuments(legalDocumentReset);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LegalDocumentApi.ResetLegalDocuments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResetLegalDocumentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.
    ApiResponse<List<LegalDocument>> response = apiInstance.ResetLegalDocumentsWithHttpInfo(legalDocumentReset);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LegalDocumentApi.ResetLegalDocumentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **legalDocumentReset** | [**LegalDocumentReset**](LegalDocumentReset.md) |  |  |

### Return type

[**List&lt;LegalDocument&gt;**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reset legal documents |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="upsertlegaldocuments"></a>
# **UpsertLegalDocuments**
> List&lt;LegalDocument&gt; UpsertLegalDocuments (List<LegalDocumentUpsert> legalDocumentUpsert)

Upsert legal documents per (doc_type, lang). Returns the full tenant list.

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
    public class UpsertLegalDocumentsExample
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
            var apiInstance = new LegalDocumentApi(httpClient, config, httpClientHandler);
            var legalDocumentUpsert = new List<LegalDocumentUpsert>(); // List<LegalDocumentUpsert> | 

            try
            {
                // Upsert legal documents per (doc_type, lang). Returns the full tenant list.
                List<LegalDocument> result = apiInstance.UpsertLegalDocuments(legalDocumentUpsert);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LegalDocumentApi.UpsertLegalDocuments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpsertLegalDocumentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upsert legal documents per (doc_type, lang). Returns the full tenant list.
    ApiResponse<List<LegalDocument>> response = apiInstance.UpsertLegalDocumentsWithHttpInfo(legalDocumentUpsert);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LegalDocumentApi.UpsertLegalDocumentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **legalDocumentUpsert** | [**List&lt;LegalDocumentUpsert&gt;**](LegalDocumentUpsert.md) |  |  |

### Return type

[**List&lt;LegalDocument&gt;**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Saved legal documents |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

