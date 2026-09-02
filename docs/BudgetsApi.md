# Org.OpenAPITools.Api.BudgetsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BudgetsApi**](BudgetsApi.md#budgetsapi) | **GET** /api/v1/bookkeeping/budgets |  |
| [**UpsertBudgetGoalApi**](BudgetsApi.md#upsertbudgetgoalapi) | **PUT** /api/v1/bookkeeping/budgets/goals/{category} |  |

<a id="budgetsapi"></a>
# **BudgetsApi**
> BudgetErgebnis BudgetsApi (int year, int month)



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
    public class BudgetsApiExample
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
            var apiInstance = new BudgetsApi(httpClient, config, httpClientHandler);
            var year = 56;  // int | 
            var month = 56;  // int | 

            try
            {
                BudgetErgebnis result = apiInstance.BudgetsApi(year, month);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BudgetsApi.BudgetsApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BudgetsApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<BudgetErgebnis> response = apiInstance.BudgetsApiWithHttpInfo(year, month);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BudgetsApi.BudgetsApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **year** | **int** |  |  |
| **month** | **int** |  |  |

### Return type

[**BudgetErgebnis**](BudgetErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Monats-Budget + Prognose |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="upsertbudgetgoalapi"></a>
# **UpsertBudgetGoalApi**
> Budget UpsertBudgetGoalApi (string category, BudgetGoalRequest budgetGoalRequest)



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
    public class UpsertBudgetGoalApiExample
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
            var apiInstance = new BudgetsApi(httpClient, config, httpClientHandler);
            var category = "category_example";  // string | 
            var budgetGoalRequest = new BudgetGoalRequest(); // BudgetGoalRequest | 

            try
            {
                Budget result = apiInstance.UpsertBudgetGoalApi(category, budgetGoalRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BudgetsApi.UpsertBudgetGoalApi: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpsertBudgetGoalApiWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<Budget> response = apiInstance.UpsertBudgetGoalApiWithHttpInfo(category, budgetGoalRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BudgetsApi.UpsertBudgetGoalApiWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **category** | **string** |  |  |
| **budgetGoalRequest** | [**BudgetGoalRequest**](BudgetGoalRequest.md) |  |  |

### Return type

[**Budget**](Budget.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Budget goal saved (upsert) |  -  |
| **400** | Negative goal |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

