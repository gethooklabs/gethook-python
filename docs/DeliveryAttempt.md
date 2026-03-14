# DeliveryAttempt


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attempt_number** | **int** |  | 
**destination_id** | **str** |  | 
**error_message** | **str** |  | [optional] 
**event_id** | **str** |  | 
**finished_at** | **str** |  | [optional] 
**id** | **str** |  | 
**latency_ms** | **int** |  | [optional] 
**outcome** | [**AttemptOutcome**](AttemptOutcome.md) |  | 
**response_body** | **str** |  | [optional] 
**response_status** | **int** |  | [optional] 
**started_at** | **str** |  | 

## Example

```python
from gethook.models.delivery_attempt import DeliveryAttempt

# TODO update the JSON string below
json = "{}"
# create an instance of DeliveryAttempt from a JSON string
delivery_attempt_instance = DeliveryAttempt.from_json(json)
# print the JSON string representation of the object
print(DeliveryAttempt.to_json())

# convert the object into a dict
delivery_attempt_dict = delivery_attempt_instance.to_dict()
# create an instance of DeliveryAttempt from a dict
delivery_attempt_from_dict = DeliveryAttempt.from_dict(delivery_attempt_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


