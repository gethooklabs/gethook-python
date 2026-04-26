# PublishOutboundData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**status** | **str** |  | 

## Example

```python
from gethook.models.publish_outbound_data import PublishOutboundData

# TODO update the JSON string below
json = "{}"
# create an instance of PublishOutboundData from a JSON string
publish_outbound_data_instance = PublishOutboundData.from_json(json)
# print the JSON string representation of the object
print(PublishOutboundData.to_json())

# convert the object into a dict
publish_outbound_data_dict = publish_outbound_data_instance.to_dict()
# create an instance of PublishOutboundData from a dict
publish_outbound_data_from_dict = PublishOutboundData.from_dict(publish_outbound_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


