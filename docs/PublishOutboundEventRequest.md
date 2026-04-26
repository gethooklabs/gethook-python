# PublishOutboundEventRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_type** | **str** |  | [optional] 
**external_event_id** | **str** |  | [optional] 
**payload** | **str** |  | 

## Example

```python
from gethook.models.publish_outbound_event_request import PublishOutboundEventRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PublishOutboundEventRequest from a JSON string
publish_outbound_event_request_instance = PublishOutboundEventRequest.from_json(json)
# print the JSON string representation of the object
print(PublishOutboundEventRequest.to_json())

# convert the object into a dict
publish_outbound_event_request_dict = publish_outbound_event_request_instance.to_dict()
# create an instance of PublishOutboundEventRequest from a dict
publish_outbound_event_request_from_dict = PublishOutboundEventRequest.from_dict(publish_outbound_event_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


