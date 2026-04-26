# CreateDestinationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**auth_config** | **object** |  | [optional] 
**custom_headers** | **object** |  | [optional] 
**name** | **str** |  | 
**signing_secret** | **str** |  | [optional] 
**timeout_seconds** | **int** |  | [optional] 
**url** | **str** |  | 

## Example

```python
from gethook.models.create_destination_request import CreateDestinationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateDestinationRequest from a JSON string
create_destination_request_instance = CreateDestinationRequest.from_json(json)
# print the JSON string representation of the object
print(CreateDestinationRequest.to_json())

# convert the object into a dict
create_destination_request_dict = create_destination_request_instance.to_dict()
# create an instance of CreateDestinationRequest from a dict
create_destination_request_from_dict = CreateDestinationRequest.from_dict(create_destination_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


