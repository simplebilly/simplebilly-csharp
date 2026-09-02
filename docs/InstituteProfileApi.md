# Org.OpenAPITools.Api.InstituteProfileApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetInstituteProfile**](InstituteProfileApi.md#getinstituteprofile) | **GET** /api/v1/institute-profile | Current institute profile (created with defaults when missing). |
| [**UpdateInstituteProfile**](InstituteProfileApi.md#updateinstituteprofile) | **PUT** /api/v1/institute-profile | Update the institute profile (institute_type and/or kapitalmarktorientiert). |

<a id="getinstituteprofile"></a>
# **GetInstituteProfile**
> InstituteProfile GetInstituteProfile ()

Current institute profile (created with defaults when missing).

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
    public class GetInstituteProfileExample
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
            var apiInstance = new InstituteProfileApi(httpClient, config, httpClientHandler);

            try
            {
                // Current institute profile (created with defaults when missing).
                InstituteProfile result = apiInstance.GetInstituteProfile();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstituteProfileApi.GetInstituteProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInstituteProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Current institute profile (created with defaults when missing).
    ApiResponse<InstituteProfile> response = apiInstance.GetInstituteProfileWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstituteProfileApi.GetInstituteProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**InstituteProfile**](InstituteProfile.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Institute profile |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateinstituteprofile"></a>
# **UpdateInstituteProfile**
> InstituteProfile UpdateInstituteProfile (InstituteProfileUpdate instituteProfileUpdate)

Update the institute profile (institute_type and/or kapitalmarktorientiert).

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
    public class UpdateInstituteProfileExample
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
            var apiInstance = new InstituteProfileApi(httpClient, config, httpClientHandler);
            var instituteProfileUpdate = new InstituteProfileUpdate(); // InstituteProfileUpdate | 

            try
            {
                // Update the institute profile (institute_type and/or kapitalmarktorientiert).
                InstituteProfile result = apiInstance.UpdateInstituteProfile(instituteProfileUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstituteProfileApi.UpdateInstituteProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateInstituteProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update the institute profile (institute_type and/or kapitalmarktorientiert).
    ApiResponse<InstituteProfile> response = apiInstance.UpdateInstituteProfileWithHttpInfo(instituteProfileUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstituteProfileApi.UpdateInstituteProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **instituteProfileUpdate** | [**InstituteProfileUpdate**](InstituteProfileUpdate.md) |  |  |

### Return type

[**InstituteProfile**](InstituteProfile.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated institute profile |  -  |
| **400** | Invalid institute_type |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

