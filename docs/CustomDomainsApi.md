# gethook.CustomDomainsApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_custom_domain**](CustomDomainsApi.md#create_custom_domain) | **POST** /v1/custom-domains | Create custom domain
[**list_custom_domains**](CustomDomainsApi.md#list_custom_domains) | **GET** /v1/custom-domains | List custom domains


# **create_custom_domain**
> CustomDomain create_custom_domain(create_custom_domain_request)

Create custom domain

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.create_custom_domain_request import CreateCustomDomainRequest
from gethook.models.custom_domain import CustomDomain
from gethook.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:8080
# See configuration.py for a list of all supported configuration parameters.
configuration = gethook.Configuration(
    host = "http://localhost:8080"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with gethook.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = gethook.CustomDomainsApi(api_client)
    create_custom_domain_request = gethook.CreateCustomDomainRequest() # CreateCustomDomainRequest | Domain details

    try:
        # Create custom domain
        api_response = api_instance.create_custom_domain(create_custom_domain_request)
        print("The response of CustomDomainsApi->create_custom_domain:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CustomDomainsApi->create_custom_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_custom_domain_request** | [**CreateCustomDomainRequest**](CreateCustomDomainRequest.md)| Domain details | 

### Return type

[**CustomDomain**](CustomDomain.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created |  -  |
**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_custom_domains**
> List[CustomDomain] list_custom_domains()

List custom domains

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.custom_domain import CustomDomain
from gethook.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:8080
# See configuration.py for a list of all supported configuration parameters.
configuration = gethook.Configuration(
    host = "http://localhost:8080"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with gethook.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = gethook.CustomDomainsApi(api_client)

    try:
        # List custom domains
        api_response = api_instance.list_custom_domains()
        print("The response of CustomDomainsApi->list_custom_domains:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CustomDomainsApi->list_custom_domains: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[CustomDomain]**](CustomDomain.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

