# gethook.OutboundEventsApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_outbound_event**](OutboundEventsApi.md#get_outbound_event) | **GET** /v1/outbound-events/{id} | Get outbound event
[**list_outbound_events**](OutboundEventsApi.md#list_outbound_events) | **GET** /v1/outbound-events | List outbound events
[**publish_outbound_event**](OutboundEventsApi.md#publish_outbound_event) | **POST** /v1/outbound-events | Publish outbound event
[**replay_outbound_event**](OutboundEventsApi.md#replay_outbound_event) | **POST** /v1/outbound-events/{id}/replay | Replay outbound event


# **get_outbound_event**
> EventDetailData get_outbound_event(id)

Get outbound event

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
    api_instance = gethook.OutboundEventsApi(api_client)
    id = 'id_example' # str | Event UUID

    try:
        # Get outbound event
        api_response = api_instance.get_outbound_event(id)
        print("The response of OutboundEventsApi->get_outbound_event:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OutboundEventsApi->get_outbound_event: %s\n" % e)
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

# **list_outbound_events**
> EventListData list_outbound_events(limit=limit, offset=offset)

List outbound events

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
    api_instance = gethook.OutboundEventsApi(api_client)
    limit = 56 # int | Max results (default 25, max 200) (optional)
    offset = 56 # int | Pagination offset (optional)

    try:
        # List outbound events
        api_response = api_instance.list_outbound_events(limit=limit, offset=offset)
        print("The response of OutboundEventsApi->list_outbound_events:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OutboundEventsApi->list_outbound_events: %s\n" % e)
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

# **publish_outbound_event**
> PublishOutboundData publish_outbound_event(publish_outbound_event_request)

Publish outbound event

Queues a new outbound event for delivery to all matching route destinations.

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.publish_outbound_data import PublishOutboundData
from gethook.models.publish_outbound_event_request import PublishOutboundEventRequest
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
    api_instance = gethook.OutboundEventsApi(api_client)
    publish_outbound_event_request = gethook.PublishOutboundEventRequest() # PublishOutboundEventRequest | Event payload

    try:
        # Publish outbound event
        api_response = api_instance.publish_outbound_event(publish_outbound_event_request)
        print("The response of OutboundEventsApi->publish_outbound_event:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OutboundEventsApi->publish_outbound_event: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **publish_outbound_event_request** | [**PublishOutboundEventRequest**](PublishOutboundEventRequest.md)| Event payload | 

### Return type

[**PublishOutboundData**](PublishOutboundData.md)

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

# **replay_outbound_event**
> ReplayEventData replay_outbound_event(id)

Replay outbound event

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
    api_instance = gethook.OutboundEventsApi(api_client)
    id = 'id_example' # str | Event UUID

    try:
        # Replay outbound event
        api_response = api_instance.replay_outbound_event(id)
        print("The response of OutboundEventsApi->replay_outbound_event:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OutboundEventsApi->replay_outbound_event: %s\n" % e)
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

