# gethook.AuthApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**login**](AuthApi.md#login) | **POST** /v1/auth/login | Login with email and password
[**register**](AuthApi.md#register) | **POST** /v1/auth/register | Register with email and password


# **login**
> AccountBootstrapData login(login_request)

Login with email and password

Authenticates with email/password and returns a fresh API key on success.

### Example


```python
import gethook
from gethook.models.account_bootstrap_data import AccountBootstrapData
from gethook.models.login_request import LoginRequest
from gethook.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:8080
# See configuration.py for a list of all supported configuration parameters.
configuration = gethook.Configuration(
    host = "http://localhost:8080"
)


# Enter a context with an instance of the API client
with gethook.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = gethook.AuthApi(api_client)
    login_request = gethook.LoginRequest() # LoginRequest | Login credentials

    try:
        # Login with email and password
        api_response = api_instance.login(login_request)
        print("The response of AuthApi->login:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->login: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **login_request** | [**LoginRequest**](LoginRequest.md)| Login credentials | 

### Return type

[**AccountBootstrapData**](AccountBootstrapData.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**400** | Bad Request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register**
> AccountBootstrapData register(register_request)

Register with email and password

Creates a new account with email/password credentials and returns a bootstrap API key.

### Example


```python
import gethook
from gethook.models.account_bootstrap_data import AccountBootstrapData
from gethook.models.register_request import RegisterRequest
from gethook.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:8080
# See configuration.py for a list of all supported configuration parameters.
configuration = gethook.Configuration(
    host = "http://localhost:8080"
)


# Enter a context with an instance of the API client
with gethook.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = gethook.AuthApi(api_client)
    register_request = gethook.RegisterRequest() # RegisterRequest | Registration details

    try:
        # Register with email and password
        api_response = api_instance.register(register_request)
        print("The response of AuthApi->register:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->register: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **register_request** | [**RegisterRequest**](RegisterRequest.md)| Registration details | 

### Return type

[**AccountBootstrapData**](AccountBootstrapData.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created |  -  |
**400** | Bad Request |  -  |
**409** | Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

