# gethook.StatsApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_stats**](StatsApi.md#get_stats) | **GET** /v1/stats | Get dashboard stats


# **get_stats**
> StatsData get_stats()

Get dashboard stats

### Example

* Api Key Authentication (ApiKeyAuth):

```python
import gethook
from gethook.models.stats_data import StatsData
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
    api_instance = gethook.StatsApi(api_client)

    try:
        # Get dashboard stats
        api_response = api_instance.get_stats()
        print("The response of StatsApi->get_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatsApi->get_stats: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**StatsData**](StatsData.md)

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

