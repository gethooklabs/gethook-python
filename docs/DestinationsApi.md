# gethook.DestinationsApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_destination**](DestinationsApi.md#create_destination) | **POST** /v1/destinations | Create destination
[**get_destination**](DestinationsApi.md#get_destination) | **GET** /v1/destinations/{id} | Get destination
[**list_destinations**](DestinationsApi.md#list_destinations) | **GET** /v1/destinations | List destinations
[**update_destination**](DestinationsApi.md#update_destination) | **PATCH** /v1/destinations/{id} | Update destination


# **create_destination**
> Destination create_destination(create_destination_request)

Create destination

Creates a new webhook delivery destination. The signing_secret is encrypted at rest and never returned.

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.create_destination_request import CreateDestinationRequest
from gethook.models.destination import Destination
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
    api_instance = gethook.DestinationsApi(api_client)
    create_destination_request = gethook.CreateDestinationRequest() # CreateDestinationRequest | Destination config

    try:
        # Create destination
        api_response = api_instance.create_destination(create_destination_request)
        print("The response of DestinationsApi->create_destination:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DestinationsApi->create_destination: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_destination_request** | [**CreateDestinationRequest**](CreateDestinationRequest.md)| Destination config | 

### Return type

[**Destination**](Destination.md)

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

# **get_destination**
> Destination get_destination(id)

Get destination

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.destination import Destination
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
    api_instance = gethook.DestinationsApi(api_client)
    id = 'id_example' # str | Destination UUID

    try:
        # Get destination
        api_response = api_instance.get_destination(id)
        print("The response of DestinationsApi->get_destination:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DestinationsApi->get_destination: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Destination UUID | 

### Return type

[**Destination**](Destination.md)

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

# **list_destinations**
> List[Destination] list_destinations()

List destinations

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.destination import Destination
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
    api_instance = gethook.DestinationsApi(api_client)

    try:
        # List destinations
        api_response = api_instance.list_destinations()
        print("The response of DestinationsApi->list_destinations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DestinationsApi->list_destinations: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[Destination]**](Destination.md)

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

# **update_destination**
> Destination update_destination(id, update_destination_request)

Update destination

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.destination import Destination
from gethook.models.update_destination_request import UpdateDestinationRequest
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
    api_instance = gethook.DestinationsApi(api_client)
    id = 'id_example' # str | Destination UUID
    update_destination_request = gethook.UpdateDestinationRequest() # UpdateDestinationRequest | Fields to update

    try:
        # Update destination
        api_response = api_instance.update_destination(id, update_destination_request)
        print("The response of DestinationsApi->update_destination:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DestinationsApi->update_destination: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Destination UUID | 
 **update_destination_request** | [**UpdateDestinationRequest**](UpdateDestinationRequest.md)| Fields to update | 

### Return type

[**Destination**](Destination.md)

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
**404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

