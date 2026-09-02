# Org.OpenAPITools.Api.MarketplaceApiApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateConnectionApi**](MarketplaceApiApi.md#createconnectionapi) | **POST** /api/v1/marketplace/connections | Create a new connection (for API-key based platforms) |
| [**DeleteConnectionApi**](MarketplaceApiApi.md#deleteconnectionapi) | **DELETE** /api/v1/marketplace/connections/{connection_id} | Soft-delete a connection |
| [**GetConnectionApi**](MarketplaceApiApi.md#getconnectionapi) | **GET** /api/v1/marketplace/connections/{connection_id} | Get a single connection |
| [**GetSyncDirectionApi**](MarketplaceApiApi.md#getsyncdirectionapi) | **GET** /api/v1/marketplace/connections/{connection_id}/directions | Get current sync direction configuration for a connection |
| [**GetSyncLogsApi**](MarketplaceApiApi.md#getsynclogsapi) | **GET** /api/v1/marketplace/connections/{connection_id}/logs | Get sync logs for a connection |
| [**ListConnectionsApi**](MarketplaceApiApi.md#listconnectionsapi) | **GET** /api/v1/marketplace/connections | List connections for the current tenant |
| [**ListPlatformsApi**](MarketplaceApiApi.md#listplatformsapi) | **GET** /api/v1/marketplace/platforms | List all supported platforms |
| [**OauthAuthorizeApi**](MarketplaceApiApi.md#oauthauthorizeapi) | **POST** /api/v1/marketplace/oauth/authorize | OAuth: initiate authorization flow |
| [**OauthCallbackApi**](MarketplaceApiApi.md#oauthcallbackapi) | **POST** /api/v1/marketplace/oauth/callback | OAuth: handle callback after authorization |
| [**TriggerSyncApi**](MarketplaceApiApi.md#triggersyncapi) | **POST** /api/v1/marketplace/connections/{connection_id}/sync | Trigger sync for a connection |
| [**UpdateConnectionApi**](MarketplaceApiApi.md#updateconnectionapi) | **PUT** /api/v1/marketplace/connections/{connection_id} | Update a connection |
| [**UpdateSyncDirectionApi**](MarketplaceApiApi.md#updatesyncdirectionapi) | **PUT** /api/v1/marketplace/connections/{connection_id}/directions | Update per-entity sync direction configuration for a connection |
| [**WebhookReceiverApi**](MarketplaceApiApi.md#webhookreceiverapi) | **POST** /api/v1/marketplace/webhook/{platform}/{connection_id} | Webhook receiver |

<a id="createconnectionapi"></a>
# **CreateConnectionApi**
> MarketplaceConnection CreateConnectionApi (CreateConnectionRequest createConnectionRequest)

Create a new connection (for API-key based platforms)

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
    public class CreateConnectionApiExample
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
            var apiInstance = new MarketplaceApiApi(httpClient, config, httpClientHandler);
            var createConnectionRequest = new CreateConnectionRequest(); // CreateConnectionRequest | 

            try
            {
                // Create a new connection (for API-key based platforms)
                MarketplaceConnection result = apiInstance.CreateConnectionApi(createConnectionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MarketplaceApiApi.CreateConnectionApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateConnectionApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a new connection (for API-key based platforms)
    ApiResponse<MarketplaceConnection> response = apiInstance.CreateConnectionApiWithHttpInfo(createConnectionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MarketplaceApiApi.CreateConnectionApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createConnectionRequest** | [**CreateConnectionRequest**](CreateConnectionRequest.md) |  |  |

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteconnectionapi"></a>
# **DeleteConnectionApi**
> void DeleteConnectionApi (string connectionId)

Soft-delete a connection

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
    public class DeleteConnectionApiExample
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
            var apiInstance = new MarketplaceApiApi(httpClient, config, httpClientHandler);
            var connectionId = "connectionId_example";  // string | 

            try
            {
                // Soft-delete a connection
                apiInstance.DeleteConnectionApi(connectionId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MarketplaceApiApi.DeleteConnectionApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteConnectionApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Soft-delete a connection
    apiInstance.DeleteConnectionApiWithHttpInfo(connectionId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MarketplaceApiApi.DeleteConnectionApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectionId** | **string** |  |  |

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
| **204** | Deleted |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getconnectionapi"></a>
# **GetConnectionApi**
> MarketplaceConnection GetConnectionApi (string connectionId)

Get a single connection

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
    public class GetConnectionApiExample
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
            var apiInstance = new MarketplaceApiApi(httpClient, config, httpClientHandler);
            var connectionId = "connectionId_example";  // string | 

            try
            {
                // Get a single connection
                MarketplaceConnection result = apiInstance.GetConnectionApi(connectionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MarketplaceApiApi.GetConnectionApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetConnectionApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a single connection
    ApiResponse<MarketplaceConnection> response = apiInstance.GetConnectionApiWithHttpInfo(connectionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MarketplaceApiApi.GetConnectionApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectionId** | **string** |  |  |

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connection details |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getsyncdirectionapi"></a>
# **GetSyncDirectionApi**
> void GetSyncDirectionApi (string connectionId)

Get current sync direction configuration for a connection

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
    public class GetSyncDirectionApiExample
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
            var apiInstance = new MarketplaceApiApi(httpClient, config, httpClientHandler);
            var connectionId = "connectionId_example";  // string | 

            try
            {
                // Get current sync direction configuration for a connection
                apiInstance.GetSyncDirectionApi(connectionId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MarketplaceApiApi.GetSyncDirectionApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSyncDirectionApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get current sync direction configuration for a connection
    apiInstance.GetSyncDirectionApiWithHttpInfo(connectionId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MarketplaceApiApi.GetSyncDirectionApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectionId** | **string** |  |  |

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
| **200** | Current sync directions |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getsynclogsapi"></a>
# **GetSyncLogsApi**
> List&lt;SyncLog&gt; GetSyncLogsApi (string connectionId)

Get sync logs for a connection

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
    public class GetSyncLogsApiExample
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
            var apiInstance = new MarketplaceApiApi(httpClient, config, httpClientHandler);
            var connectionId = "connectionId_example";  // string | 

            try
            {
                // Get sync logs for a connection
                List<SyncLog> result = apiInstance.GetSyncLogsApi(connectionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MarketplaceApiApi.GetSyncLogsApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSyncLogsApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get sync logs for a connection
    ApiResponse<List<SyncLog>> response = apiInstance.GetSyncLogsApiWithHttpInfo(connectionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MarketplaceApiApi.GetSyncLogsApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectionId** | **string** |  |  |

### Return type

[**List&lt;SyncLog&gt;**](SyncLog.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sync logs |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listconnectionsapi"></a>
# **ListConnectionsApi**
> List&lt;MarketplaceConnection&gt; ListConnectionsApi ()

List connections for the current tenant

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
    public class ListConnectionsApiExample
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
            var apiInstance = new MarketplaceApiApi(httpClient, config, httpClientHandler);

            try
            {
                // List connections for the current tenant
                List<MarketplaceConnection> result = apiInstance.ListConnectionsApi();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MarketplaceApiApi.ListConnectionsApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListConnectionsApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List connections for the current tenant
    ApiResponse<List<MarketplaceConnection>> response = apiInstance.ListConnectionsApiWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MarketplaceApiApi.ListConnectionsApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;MarketplaceConnection&gt;**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of connections |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listplatformsapi"></a>
# **ListPlatformsApi**
> List&lt;PlatformInfo&gt; ListPlatformsApi ()

List all supported platforms

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
    public class ListPlatformsApiExample
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
            var apiInstance = new MarketplaceApiApi(httpClient, config, httpClientHandler);

            try
            {
                // List all supported platforms
                List<PlatformInfo> result = apiInstance.ListPlatformsApi();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MarketplaceApiApi.ListPlatformsApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListPlatformsApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List all supported platforms
    ApiResponse<List<PlatformInfo>> response = apiInstance.ListPlatformsApiWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MarketplaceApiApi.ListPlatformsApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;PlatformInfo&gt;**](PlatformInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Supported platforms |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="oauthauthorizeapi"></a>
# **OauthAuthorizeApi**
> OAuthAuthorizeResponse OauthAuthorizeApi (OAuthAuthorizeRequest oAuthAuthorizeRequest)

OAuth: initiate authorization flow

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
    public class OauthAuthorizeApiExample
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
            var apiInstance = new MarketplaceApiApi(httpClient, config, httpClientHandler);
            var oAuthAuthorizeRequest = new OAuthAuthorizeRequest(); // OAuthAuthorizeRequest | 

            try
            {
                // OAuth: initiate authorization flow
                OAuthAuthorizeResponse result = apiInstance.OauthAuthorizeApi(oAuthAuthorizeRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MarketplaceApiApi.OauthAuthorizeApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OauthAuthorizeApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // OAuth: initiate authorization flow
    ApiResponse<OAuthAuthorizeResponse> response = apiInstance.OauthAuthorizeApiWithHttpInfo(oAuthAuthorizeRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MarketplaceApiApi.OauthAuthorizeApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **oAuthAuthorizeRequest** | [**OAuthAuthorizeRequest**](OAuthAuthorizeRequest.md) |  |  |

### Return type

[**OAuthAuthorizeResponse**](OAuthAuthorizeResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Authorization URL |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="oauthcallbackapi"></a>
# **OauthCallbackApi**
> MarketplaceConnection OauthCallbackApi (OAuthCallbackRequest oAuthCallbackRequest)

OAuth: handle callback after authorization

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
    public class OauthCallbackApiExample
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
            var apiInstance = new MarketplaceApiApi(httpClient, config, httpClientHandler);
            var oAuthCallbackRequest = new OAuthCallbackRequest(); // OAuthCallbackRequest | 

            try
            {
                // OAuth: handle callback after authorization
                MarketplaceConnection result = apiInstance.OauthCallbackApi(oAuthCallbackRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MarketplaceApiApi.OauthCallbackApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OauthCallbackApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // OAuth: handle callback after authorization
    ApiResponse<MarketplaceConnection> response = apiInstance.OauthCallbackApiWithHttpInfo(oAuthCallbackRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MarketplaceApiApi.OauthCallbackApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **oAuthCallbackRequest** | [**OAuthCallbackRequest**](OAuthCallbackRequest.md) |  |  |

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Connection created/updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="triggersyncapi"></a>
# **TriggerSyncApi**
> SyncSummary TriggerSyncApi (string connectionId, string? syncType = null, string? direction = null)

Trigger sync for a connection

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
    public class TriggerSyncApiExample
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
            var apiInstance = new MarketplaceApiApi(httpClient, config, httpClientHandler);
            var connectionId = "connectionId_example";  // string | 
            var syncType = "syncType_example";  // string? |  (optional) 
            var direction = "direction_example";  // string? |  (optional) 

            try
            {
                // Trigger sync for a connection
                SyncSummary result = apiInstance.TriggerSyncApi(connectionId, syncType, direction);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MarketplaceApiApi.TriggerSyncApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TriggerSyncApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Trigger sync for a connection
    ApiResponse<SyncSummary> response = apiInstance.TriggerSyncApiWithHttpInfo(connectionId, syncType, direction);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MarketplaceApiApi.TriggerSyncApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectionId** | **string** |  |  |
| **syncType** | **string?** |  | [optional]  |
| **direction** | **string?** |  | [optional]  |

### Return type

[**SyncSummary**](SyncSummary.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sync triggered |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateconnectionapi"></a>
# **UpdateConnectionApi**
> MarketplaceConnection UpdateConnectionApi (string connectionId, UpdateConnectionRequest updateConnectionRequest)

Update a connection

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
    public class UpdateConnectionApiExample
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
            var apiInstance = new MarketplaceApiApi(httpClient, config, httpClientHandler);
            var connectionId = "connectionId_example";  // string | 
            var updateConnectionRequest = new UpdateConnectionRequest(); // UpdateConnectionRequest | 

            try
            {
                // Update a connection
                MarketplaceConnection result = apiInstance.UpdateConnectionApi(connectionId, updateConnectionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MarketplaceApiApi.UpdateConnectionApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateConnectionApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a connection
    ApiResponse<MarketplaceConnection> response = apiInstance.UpdateConnectionApiWithHttpInfo(connectionId, updateConnectionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MarketplaceApiApi.UpdateConnectionApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectionId** | **string** |  |  |
| **updateConnectionRequest** | [**UpdateConnectionRequest**](UpdateConnectionRequest.md) |  |  |

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatesyncdirectionapi"></a>
# **UpdateSyncDirectionApi**
> void UpdateSyncDirectionApi (string connectionId, UpdateSyncDirectionRequest updateSyncDirectionRequest)

Update per-entity sync direction configuration for a connection

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
    public class UpdateSyncDirectionApiExample
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
            var apiInstance = new MarketplaceApiApi(httpClient, config, httpClientHandler);
            var connectionId = "connectionId_example";  // string | 
            var updateSyncDirectionRequest = new UpdateSyncDirectionRequest(); // UpdateSyncDirectionRequest | 

            try
            {
                // Update per-entity sync direction configuration for a connection
                apiInstance.UpdateSyncDirectionApi(connectionId, updateSyncDirectionRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MarketplaceApiApi.UpdateSyncDirectionApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateSyncDirectionApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update per-entity sync direction configuration for a connection
    apiInstance.UpdateSyncDirectionApiWithHttpInfo(connectionId, updateSyncDirectionRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MarketplaceApiApi.UpdateSyncDirectionApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectionId** | **string** |  |  |
| **updateSyncDirectionRequest** | [**UpdateSyncDirectionRequest**](UpdateSyncDirectionRequest.md) |  |  |

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
| **200** | Sync directions updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="webhookreceiverapi"></a>
# **WebhookReceiverApi**
> void WebhookReceiverApi (string platform, string connectionId)

Webhook receiver

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
    public class WebhookReceiverApiExample
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
            var apiInstance = new MarketplaceApiApi(httpClient, config, httpClientHandler);
            var platform = "platform_example";  // string | 
            var connectionId = "connectionId_example";  // string | 

            try
            {
                // Webhook receiver
                apiInstance.WebhookReceiverApi(platform, connectionId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MarketplaceApiApi.WebhookReceiverApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WebhookReceiverApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Webhook receiver
    apiInstance.WebhookReceiverApiWithHttpInfo(platform, connectionId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MarketplaceApiApi.WebhookReceiverApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **platform** | **string** |  |  |
| **connectionId** | **string** |  |  |

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
| **200** | Webhook received |  -  |
| **401** | Invalid signature |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

