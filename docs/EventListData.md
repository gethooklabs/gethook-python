# EventListData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Event]**](Event.md) |  | 
**total** | **int** |  | 

## Example

```python
from gethook.models.event_list_data import EventListData

# TODO update the JSON string below
json = "{}"
# create an instance of EventListData from a JSON string
event_list_data_instance = EventListData.from_json(json)
# print the JSON string representation of the object
print(EventListData.to_json())

# convert the object into a dict
event_list_data_dict = event_list_data_instance.to_dict()
# create an instance of EventListData from a dict
event_list_data_from_dict = EventListData.from_dict(event_list_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


