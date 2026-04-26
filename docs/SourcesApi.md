# gethook.SourcesApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_source**](SourcesApi.md#create_source) | **POST** /v1/sources | Create source
[**delete_source**](SourcesApi.md#delete_source) | **DELETE** /v1/sources/{id} | Delete source
[**get_source**](SourcesApi.md#get_source) | **GET** /v1/sources/{id} | Get source
[**list_providers**](SourcesApi.md#list_providers) | **GET** /v1/provider-presets | List provider presets
[**list_sources**](SourcesApi.md#list_sources) | **GET** /v1/sources | List sources


# **create_source**
> Source create_source(create_source_request)

Create source

Creates a new webhook source endpoint. Returns an ingest_url to share with the event sender.

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.create_source_request import CreateSourceRequest
from gethook.models.source import Source
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
    api_instance = gethook.SourcesApi(api_client)
    create_source_request = gethook.CreateSourceRequest() # CreateSourceRequest | Source config

    try:
        # Create source
        api_response = api_instance.create_source(create_source_request)
        print("The response of SourcesApi->create_source:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SourcesApi->create_source: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_source_request** | [**CreateSourceRequest**](CreateSourceRequest.md)| Source config | 

### Return type

[**Source**](Source.md)

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

# **delete_source**
> delete_source(id)

Delete source

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
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
    api_instance = gethook.SourcesApi(api_client)
    id = 'id_example' # str | Source UUID

    try:
        # Delete source
        api_instance.delete_source(id)
    except Exception as e:
        print("Exception when calling SourcesApi->delete_source: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Source UUID | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | No Content |  -  |
**400** | Bad Request |  -  |
**404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_source**
> Source get_source(id)

Get source

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.source import Source
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
    api_instance = gethook.SourcesApi(api_client)
    id = 'id_example' # str | Source UUID

    try:
        # Get source
        api_response = api_instance.get_source(id)
        print("The response of SourcesApi->get_source:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SourcesApi->get_source: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Source UUID | 

### Return type

[**Source**](Source.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**400** | Bad Request |  -  |
**404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_providers**
> List[ProviderPreset] list_providers()

List provider presets

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.provider_preset import ProviderPreset
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
    api_instance = gethook.SourcesApi(api_client)

    try:
        # List provider presets
        api_response = api_instance.list_providers()
        print("The response of SourcesApi->list_providers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SourcesApi->list_providers: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[ProviderPreset]**](ProviderPreset.md)

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

# **list_sources**
> List[Source] list_sources()

List sources

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.source import Source
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
    api_instance = gethook.SourcesApi(api_client)

    try:
        # List sources
        api_response = api_instance.list_sources()
        print("The response of SourcesApi->list_sources:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SourcesApi->list_sources: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[Source]**](Source.md)

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

