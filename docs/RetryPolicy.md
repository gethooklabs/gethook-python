# RetryPolicy


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**max_attempts** | **int** |  | [optional] 
**backoff** | **str** |  | [optional] 

## Example

```python
from gethook.models.retry_policy import RetryPolicy

# TODO update the JSON string below
json = "{}"
# create an instance of RetryPolicy from a JSON string
retry_policy_instance = RetryPolicy.from_json(json)
# print the JSON string representation of the object
print(RetryPolicy.to_json())

# convert the object into a dict
retry_policy_dict = retry_policy_instance.to_dict()
# create an instance of RetryPolicy from a dict
retry_policy_from_dict = RetryPolicy.from_dict(retry_policy_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


