# gethook.BrandApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_brand_settings**](BrandApi.md#get_brand_settings) | **GET** /v1/brand-settings | Get brand settings
[**upsert_brand_settings**](BrandApi.md#upsert_brand_settings) | **POST** /v1/brand-settings | Upsert brand settings


# **get_brand_settings**
> BrandSettings get_brand_settings()

Get brand settings

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.brand_settings import BrandSettings
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
    api_instance = gethook.BrandApi(api_client)

    try:
        # Get brand settings
        api_response = api_instance.get_brand_settings()
        print("The response of BrandApi->get_brand_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BrandApi->get_brand_settings: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**BrandSettings**](BrandSettings.md)

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

# **upsert_brand_settings**
> BrandSettings upsert_brand_settings(upsert_brand_settings_request)

Upsert brand settings

Creates or replaces white-label brand settings for the account.

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.brand_settings import BrandSettings
from gethook.models.upsert_brand_settings_request import UpsertBrandSettingsRequest
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
    api_instance = gethook.BrandApi(api_client)
    upsert_brand_settings_request = gethook.UpsertBrandSettingsRequest() # UpsertBrandSettingsRequest | Brand settings

    try:
        # Upsert brand settings
        api_response = api_instance.upsert_brand_settings(upsert_brand_settings_request)
        print("The response of BrandApi->upsert_brand_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BrandApi->upsert_brand_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **upsert_brand_settings_request** | [**UpsertBrandSettingsRequest**](UpsertBrandSettingsRequest.md)| Brand settings | 

### Return type

[**BrandSettings**](BrandSettings.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

