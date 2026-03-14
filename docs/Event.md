# Event


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | 
**attempts_count** | **int** |  | 
**body** | **str** |  | 
**created_at** | **str** |  | 
**created_by** | **str** |  | [optional] 
**direction** | [**Direction**](Direction.md) |  | 
**event_type** | **str** |  | [optional] 
**external_event_id** | **str** |  | [optional] 
**final_state** | **str** |  | [optional] 
**headers** | **Dict[str, object]** |  | 
**id** | **str** |  | 
**next_attempt_at** | **str** |  | [optional] 
**payload_hash** | **str** |  | [optional] 
**received_at** | **str** |  | 
**source_id** | **str** |  | [optional] 
**status** | [**EventStatus**](EventStatus.md) |  | 

## Example

```python
from gethook.models.event import Event

# TODO update the JSON string below
json = "{}"
# create an instance of Event from a JSON string
event_instance = Event.from_json(json)
# print the JSON string representation of the object
print(Event.to_json())

# convert the object into a dict
event_dict = event_instance.to_dict()
# create an instance of Event from a dict
event_from_dict = Event.from_dict(event_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


