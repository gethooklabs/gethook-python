# gethook.PlatformApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_platform_stats**](PlatformApi.md#get_platform_stats) | **GET** /v1/platform-stats | Public platform statistics


# **get_platform_stats**
> PlatformStats get_platform_stats()

Public platform statistics

### Example


```python
import gethook
from gethook.models.platform_stats import PlatformStats
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
    api_instance = gethook.PlatformApi(api_client)

    try:
        # Public platform statistics
        api_response = api_instance.get_platform_stats()
        print("The response of PlatformApi->get_platform_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PlatformApi->get_platform_stats: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**PlatformStats**](PlatformStats.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

