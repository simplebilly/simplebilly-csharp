# Org.OpenAPITools.Api.TaxApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateTaxRate**](TaxApi.md#createtaxrate) | **POST** /api/v1/tax-rates | Create a tax rate (&#x60;admin:settings&#x60;). |
| [**DeleteTaxRate**](TaxApi.md#deletetaxrate) | **DELETE** /api/v1/tax-rates/{id} | Delete a tax rate by id (&#x60;admin:settings&#x60;). |
| [**ListTaxRates**](TaxApi.md#listtaxrates) | **GET** /api/v1/tax-rates | List the calling tenant&#39;s tax rates. |
| [**UpdateTaxRate**](TaxApi.md#updatetaxrate) | **PUT** /api/v1/tax-rates/{id} | Update a tax rate by id (&#x60;admin:settings&#x60;). Replaces all body fields. |

<a id="createtaxrate"></a>
# **CreateTaxRate**
> void CreateTaxRate (TaxRateCreate taxRateCreate)

Create a tax rate (`admin:settings`).

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
    public class CreateTaxRateExample
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
            var apiInstance = new TaxApi(httpClient, config, httpClientHandler);
            var taxRateCreate = new TaxRateCreate(); // TaxRateCreate | 

            try
            {
                // Create a tax rate (`admin:settings`).
                apiInstance.CreateTaxRate(taxRateCreate);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TaxApi.CreateTaxRate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTaxRateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a tax rate (`admin:settings`).
    apiInstance.CreateTaxRateWithHttpInfo(taxRateCreate);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TaxApi.CreateTaxRateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taxRateCreate** | [**TaxRateCreate**](TaxRateCreate.md) |  |  |

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
| **200** | Tax rate created |  -  |
| **400** | Invalid body |  -  |
| **403** | Missing admin:settings permission |  -  |
| **409** | Default rate for the country already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletetaxrate"></a>
# **DeleteTaxRate**
> void DeleteTaxRate (Guid id)

Delete a tax rate by id (`admin:settings`).

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
    public class DeleteTaxRateExample
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
            var apiInstance = new TaxApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // Guid | 

            try
            {
                // Delete a tax rate by id (`admin:settings`).
                apiInstance.DeleteTaxRate(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TaxApi.DeleteTaxRate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTaxRateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a tax rate by id (`admin:settings`).
    apiInstance.DeleteTaxRateWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TaxApi.DeleteTaxRateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **Guid** |  |  |

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
| **200** | Tax rate deleted |  -  |
| **403** | Missing admin:settings permission |  -  |
| **404** | Tax rate not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtaxrates"></a>
# **ListTaxRates**
> void ListTaxRates ()

List the calling tenant's tax rates.

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
    public class ListTaxRatesExample
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
            var apiInstance = new TaxApi(httpClient, config, httpClientHandler);

            try
            {
                // List the calling tenant's tax rates.
                apiInstance.ListTaxRates();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TaxApi.ListTaxRates: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTaxRatesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List the calling tenant's tax rates.
    apiInstance.ListTaxRatesWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TaxApi.ListTaxRatesWithHttpInfo: " + e.Message);
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
| **200** | Tenant&#39;s tax rates |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatetaxrate"></a>
# **UpdateTaxRate**
> void UpdateTaxRate (Guid id, TaxRateCreate taxRateCreate)

Update a tax rate by id (`admin:settings`). Replaces all body fields.

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
    public class UpdateTaxRateExample
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
            var apiInstance = new TaxApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // Guid | 
            var taxRateCreate = new TaxRateCreate(); // TaxRateCreate | 

            try
            {
                // Update a tax rate by id (`admin:settings`). Replaces all body fields.
                apiInstance.UpdateTaxRate(id, taxRateCreate);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TaxApi.UpdateTaxRate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTaxRateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a tax rate by id (`admin:settings`). Replaces all body fields.
    apiInstance.UpdateTaxRateWithHttpInfo(id, taxRateCreate);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TaxApi.UpdateTaxRateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **Guid** |  |  |
| **taxRateCreate** | [**TaxRateCreate**](TaxRateCreate.md) |  |  |

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
| **200** | Tax rate updated |  -  |
| **400** | Invalid body |  -  |
| **403** | Missing admin:settings permission |  -  |
| **404** | Tax rate not found |  -  |
| **409** | Default rate for the country already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

