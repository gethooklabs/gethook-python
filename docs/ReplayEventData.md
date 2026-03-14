# ReplayEventData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**original_event_id** | **str** |  | 
**replay_event_id** | **str** |  | 
**status** | **str** |  | 

## Example

```python
from gethook.models.replay_event_data import ReplayEventData

# TODO update the JSON string below
json = "{}"
# create an instance of ReplayEventData from a JSON string
replay_event_data_instance = ReplayEventData.from_json(json)
# print the JSON string representation of the object
print(ReplayEventData.to_json())

# convert the object into a dict
replay_event_data_dict = replay_event_data_instance.to_dict()
# create an instance of ReplayEventData from a dict
replay_event_data_from_dict = ReplayEventData.from_dict(replay_event_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


