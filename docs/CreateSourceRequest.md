# CreateSourceRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**auth_mode** | **str** |  | [optional] 
**name** | **str** |  | 
**verification_config** | **object** |  | [optional] 

## Example

```python
from gethook.models.create_source_request import CreateSourceRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateSourceRequest from a JSON string
create_source_request_instance = CreateSourceRequest.from_json(json)
# print the JSON string representation of the object
print(CreateSourceRequest.to_json())

# convert the object into a dict
create_source_request_dict = create_source_request_instance.to_dict()
# create an instance of CreateSourceRequest from a dict
create_source_request_from_dict = CreateSourceRequest.from_dict(create_source_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


