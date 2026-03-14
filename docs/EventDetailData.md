# EventDetailData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attempts** | [**List[DeliveryAttempt]**](DeliveryAttempt.md) |  | 
**event** | [**Event**](Event.md) |  | 

## Example

```python
from gethook.models.event_detail_data import EventDetailData

# TODO update the JSON string below
json = "{}"
# create an instance of EventDetailData from a JSON string
event_detail_data_instance = EventDetailData.from_json(json)
# print the JSON string representation of the object
print(EventDetailData.to_json())

# convert the object into a dict
event_detail_data_dict = event_detail_data_instance.to_dict()
# create an instance of EventDetailData from a dict
event_detail_data_from_dict = EventDetailData.from_dict(event_detail_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


