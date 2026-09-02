# Org.OpenAPITools.Api.AuthApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AcceptInvite**](AuthApi.md#acceptinvite) | **POST** /auth/accept-invite | Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox. |
| [**ForgotPassword**](AuthApi.md#forgotpassword) | **POST** /auth/forgot-password | Send a password reset email to the user |
| [**Login**](AuthApi.md#login) | **POST** /auth/login | Authenticate a user with email + password (optional TOTP) |
| [**Logout**](AuthApi.md#logout) | **POST** /auth/logout | Log out the current user (kills the assay session) |
| [**MagicLinkLogin**](AuthApi.md#magiclinklogin) | **POST** /auth/magic-link | Request a magic link login (sends an email with a one-time link) |
| [**MagicLinkVerify**](AuthApi.md#magiclinkverify) | **POST** /auth/magic-link/verify | Verify a magic link token and log the user in |
| [**Register**](AuthApi.md#register) | **POST** /auth/register | Register a new user account |
| [**ResetPassword**](AuthApi.md#resetpassword) | **POST** /auth/reset-password | Reset the user&#39;s password using a reset token |
| [**TotpEnable**](AuthApi.md#totpenable) | **POST** /auth/totp/enable | Enable TOTP two-factor authentication by verifying a code |
| [**TotpSetup**](AuthApi.md#totpsetup) | **GET** /auth/totp/setup | Set up TOTP two-factor authentication (generates secret + backup codes) |
| [**VerifyEmail**](AuthApi.md#verifyemail) | **POST** /auth/verify-email | Verify a user&#39;s email address using a verification token |

<a id="acceptinvite"></a>
# **AcceptInvite**
> void AcceptInvite (AcceptInviteRequest acceptInviteRequest)

Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.

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
    public class AcceptInviteExample
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
            var apiInstance = new AuthApi(httpClient, config, httpClientHandler);
            var acceptInviteRequest = new AcceptInviteRequest(); // AcceptInviteRequest | 

            try
            {
                // Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.
                apiInstance.AcceptInvite(acceptInviteRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.AcceptInvite: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AcceptInviteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.
    apiInstance.AcceptInviteWithHttpInfo(acceptInviteRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.AcceptInviteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **acceptInviteRequest** | [**AcceptInviteRequest**](AcceptInviteRequest.md) |  |  |

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
| **200** | Invitation accepted |  -  |
| **400** | Weak password or privacy policy not accepted |  -  |
| **401** | Invalid or expired invite token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="forgotpassword"></a>
# **ForgotPassword**
> void ForgotPassword (ForgotPasswordRequest forgotPasswordRequest)

Send a password reset email to the user

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
    public class ForgotPasswordExample
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
            var apiInstance = new AuthApi(httpClient, config, httpClientHandler);
            var forgotPasswordRequest = new ForgotPasswordRequest(); // ForgotPasswordRequest | 

            try
            {
                // Send a password reset email to the user
                apiInstance.ForgotPassword(forgotPasswordRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.ForgotPassword: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ForgotPasswordWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send a password reset email to the user
    apiInstance.ForgotPasswordWithHttpInfo(forgotPasswordRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.ForgotPasswordWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **forgotPasswordRequest** | [**ForgotPasswordRequest**](ForgotPasswordRequest.md) |  |  |

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
| **200** | Password reset email sent if the account exists |  -  |
| **404** | User not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="login"></a>
# **Login**
> AuthResponse Login (LoginRequest loginRequest)

Authenticate a user with email + password (optional TOTP)

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
    public class LoginExample
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
            var apiInstance = new AuthApi(httpClient, config, httpClientHandler);
            var loginRequest = new LoginRequest(); // LoginRequest | 

            try
            {
                // Authenticate a user with email + password (optional TOTP)
                AuthResponse result = apiInstance.Login(loginRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.Login: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LoginWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Authenticate a user with email + password (optional TOTP)
    ApiResponse<AuthResponse> response = apiInstance.LoginWithHttpInfo(loginRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.LoginWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **loginRequest** | [**LoginRequest**](LoginRequest.md) |  |  |

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Login successful, returns JWT tokens |  -  |
| **401** | Invalid credentials |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="logout"></a>
# **Logout**
> void Logout ()

Log out the current user (kills the assay session)

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
    public class LogoutExample
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
            var apiInstance = new AuthApi(httpClient, config, httpClientHandler);

            try
            {
                // Log out the current user (kills the assay session)
                apiInstance.Logout();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.Logout: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LogoutWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Log out the current user (kills the assay session)
    apiInstance.LogoutWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.LogoutWithHttpInfo: " + e.Message);
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
| **200** | Logged out successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="magiclinklogin"></a>
# **MagicLinkLogin**
> void MagicLinkLogin (MagicLinkRequest magicLinkRequest)

Request a magic link login (sends an email with a one-time link)

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
    public class MagicLinkLoginExample
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
            var apiInstance = new AuthApi(httpClient, config, httpClientHandler);
            var magicLinkRequest = new MagicLinkRequest(); // MagicLinkRequest | 

            try
            {
                // Request a magic link login (sends an email with a one-time link)
                apiInstance.MagicLinkLogin(magicLinkRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.MagicLinkLogin: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MagicLinkLoginWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Request a magic link login (sends an email with a one-time link)
    apiInstance.MagicLinkLoginWithHttpInfo(magicLinkRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.MagicLinkLoginWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **magicLinkRequest** | [**MagicLinkRequest**](MagicLinkRequest.md) |  |  |

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
| **200** | Magic link email sent if the account exists |  -  |
| **404** | User not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="magiclinkverify"></a>
# **MagicLinkVerify**
> AuthResponse MagicLinkVerify (MagicLinkVerifyRequest magicLinkVerifyRequest)

Verify a magic link token and log the user in

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
    public class MagicLinkVerifyExample
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
            var apiInstance = new AuthApi(httpClient, config, httpClientHandler);
            var magicLinkVerifyRequest = new MagicLinkVerifyRequest(); // MagicLinkVerifyRequest | 

            try
            {
                // Verify a magic link token and log the user in
                AuthResponse result = apiInstance.MagicLinkVerify(magicLinkVerifyRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.MagicLinkVerify: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MagicLinkVerifyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Verify a magic link token and log the user in
    ApiResponse<AuthResponse> response = apiInstance.MagicLinkVerifyWithHttpInfo(magicLinkVerifyRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.MagicLinkVerifyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **magicLinkVerifyRequest** | [**MagicLinkVerifyRequest**](MagicLinkVerifyRequest.md) |  |  |

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Magic link verified, returns JWT tokens |  -  |
| **401** | Invalid or expired token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="register"></a>
# **Register**
> AuthResponse Register (RegisterRequest registerRequest)

Register a new user account

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
    public class RegisterExample
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
            var apiInstance = new AuthApi(httpClient, config, httpClientHandler);
            var registerRequest = new RegisterRequest(); // RegisterRequest | 

            try
            {
                // Register a new user account
                AuthResponse result = apiInstance.Register(registerRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.Register: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RegisterWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Register a new user account
    ApiResponse<AuthResponse> response = apiInstance.RegisterWithHttpInfo(registerRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.RegisterWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **registerRequest** | [**RegisterRequest**](RegisterRequest.md) |  |  |

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User registered, verification email sent |  -  |
| **409** | User already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="resetpassword"></a>
# **ResetPassword**
> void ResetPassword (ResetPasswordRequest resetPasswordRequest)

Reset the user's password using a reset token

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
    public class ResetPasswordExample
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
            var apiInstance = new AuthApi(httpClient, config, httpClientHandler);
            var resetPasswordRequest = new ResetPasswordRequest(); // ResetPasswordRequest | 

            try
            {
                // Reset the user's password using a reset token
                apiInstance.ResetPassword(resetPasswordRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.ResetPassword: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResetPasswordWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reset the user's password using a reset token
    apiInstance.ResetPasswordWithHttpInfo(resetPasswordRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.ResetPasswordWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **resetPasswordRequest** | [**ResetPasswordRequest**](ResetPasswordRequest.md) |  |  |

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
| **200** | Password reset successfully |  -  |
| **401** | Invalid or expired token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="totpenable"></a>
# **TotpEnable**
> void TotpEnable (TotpEnableRequest totpEnableRequest)

Enable TOTP two-factor authentication by verifying a code

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
    public class TotpEnableExample
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
            var apiInstance = new AuthApi(httpClient, config, httpClientHandler);
            var totpEnableRequest = new TotpEnableRequest(); // TotpEnableRequest | 

            try
            {
                // Enable TOTP two-factor authentication by verifying a code
                apiInstance.TotpEnable(totpEnableRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.TotpEnable: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TotpEnableWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Enable TOTP two-factor authentication by verifying a code
    apiInstance.TotpEnableWithHttpInfo(totpEnableRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.TotpEnableWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **totpEnableRequest** | [**TotpEnableRequest**](TotpEnableRequest.md) |  |  |

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
| **200** | TOTP enabled successfully |  -  |
| **401** | Invalid TOTP code |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="totpsetup"></a>
# **TotpSetup**
> TotpSetupResponse TotpSetup ()

Set up TOTP two-factor authentication (generates secret + backup codes)

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
    public class TotpSetupExample
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
            var apiInstance = new AuthApi(httpClient, config, httpClientHandler);

            try
            {
                // Set up TOTP two-factor authentication (generates secret + backup codes)
                TotpSetupResponse result = apiInstance.TotpSetup();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.TotpSetup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TotpSetupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set up TOTP two-factor authentication (generates secret + backup codes)
    ApiResponse<TotpSetupResponse> response = apiInstance.TotpSetupWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.TotpSetupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**TotpSetupResponse**](TotpSetupResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | TOTP setup data |  -  |
| **409** | TOTP already enabled |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="verifyemail"></a>
# **VerifyEmail**
> void VerifyEmail (VerifyEmailRequest verifyEmailRequest)

Verify a user's email address using a verification token

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
    public class VerifyEmailExample
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
            var apiInstance = new AuthApi(httpClient, config, httpClientHandler);
            var verifyEmailRequest = new VerifyEmailRequest(); // VerifyEmailRequest | 

            try
            {
                // Verify a user's email address using a verification token
                apiInstance.VerifyEmail(verifyEmailRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.VerifyEmail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VerifyEmailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Verify a user's email address using a verification token
    apiInstance.VerifyEmailWithHttpInfo(verifyEmailRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.VerifyEmailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **verifyEmailRequest** | [**VerifyEmailRequest**](VerifyEmailRequest.md) |  |  |

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
| **200** | Email verified successfully |  -  |
| **401** | Invalid or expired token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

