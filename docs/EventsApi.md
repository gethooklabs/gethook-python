# gethook.EventsApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_event**](EventsApi.md#get_event) | **GET** /v1/events/{id} | Get inbound event
[**list_events**](EventsApi.md#list_events) | **GET** /v1/events | List inbound events
[**replay_event**](EventsApi.md#replay_event) | **POST** /v1/events/{id}/replay | Replay inbound event


# **get_event**
> EventDetailData get_event(id)

Get inbound event

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.event_detail_data import EventDetailData
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
    api_instance = gethook.EventsApi(api_client)
    id = 'id_example' # str | Event UUID

    try:
        # Get inbound event
        api_response = api_instance.get_event(id)
        print("The response of EventsApi->get_event:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EventsApi->get_event: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Event UUID | 

### Return type

[**EventDetailData**](EventDetailData.md)

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

# **list_events**
> EventListData list_events(limit=limit, offset=offset)

List inbound events

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.event_list_data import EventListData
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
    api_instance = gethook.EventsApi(api_client)
    limit = 56 # int | Max results (default 25, max 200) (optional)
    offset = 56 # int | Pagination offset (optional)

    try:
        # List inbound events
        api_response = api_instance.list_events(limit=limit, offset=offset)
        print("The response of EventsApi->list_events:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EventsApi->list_events: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Max results (default 25, max 200) | [optional] 
 **offset** | **int**| Pagination offset | [optional] 

### Return type

[**EventListData**](EventListData.md)

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

# **replay_event**
> ReplayEventData replay_event(id)

Replay inbound event

Creates a new queued copy of the event for re-delivery.

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.replay_event_data import ReplayEventData
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
    api_instance = gethook.EventsApi(api_client)
    id = 'id_example' # str | Event UUID

    try:
        # Replay inbound event
        api_response = api_instance.replay_event(id)
        print("The response of EventsApi->replay_event:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EventsApi->replay_event: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Event UUID | 

### Return type

[**ReplayEventData**](ReplayEventData.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Accepted |  -  |
**400** | Bad Request |  -  |
**404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

