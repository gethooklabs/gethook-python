# gethook.AccountsApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_account**](AccountsApi.md#create_account) | **POST** /v1/accounts | Create account


# **create_account**
> AccountBootstrapData create_account(create_account_request)

Create account

Creates a new account and returns a bootstrap API key. No authentication required.

### Example


```python
import gethook
from gethook.models.account_bootstrap_data import AccountBootstrapData
from gethook.models.create_account_request import CreateAccountRequest
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
    api_instance = gethook.AccountsApi(api_client)
    create_account_request = gethook.CreateAccountRequest() # CreateAccountRequest | Account name

    try:
        # Create account
        api_response = api_instance.create_account(create_account_request)
        print("The response of AccountsApi->create_account:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountsApi->create_account: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_account_request** | [**CreateAccountRequest**](CreateAccountRequest.md)| Account name | 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

