# gethook.IngestApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ingest**](IngestApi.md#ingest) | **POST** /ingest/{token} | Ingest webhook event


# **ingest**
> IngestAcceptedData ingest(token)

Ingest webhook event

Accepts an inbound webhook. The path token authenticates the source — no Bearer header required.

### Example


```python
import gethook
from gethook.models.ingest_accepted_data import IngestAcceptedData
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
    api_instance = gethook.IngestApi(api_client)
    token = 'token_example' # str | Source path token (src_...)

    try:
        # Ingest webhook event
        api_response = api_instance.ingest(token)
        print("The response of IngestApi->ingest:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IngestApi->ingest: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **str**| Source path token (src_...) | 

### Return type

[**IngestAcceptedData**](IngestAcceptedData.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Accepted |  -  |
**404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

