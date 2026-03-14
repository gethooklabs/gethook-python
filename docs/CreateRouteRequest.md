# CreateRouteRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**destination_id** | **str** |  | 
**event_type_pattern** | **str** |  | [optional] 
**source_id** | **str** |  | [optional] 

## Example

```python
from gethook.models.create_route_request import CreateRouteRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateRouteRequest from a JSON string
create_route_request_instance = CreateRouteRequest.from_json(json)
# print the JSON string representation of the object
print(CreateRouteRequest.to_json())

# convert the object into a dict
create_route_request_dict = create_route_request_instance.to_dict()
# create an instance of CreateRouteRequest from a dict
create_route_request_from_dict = CreateRouteRequest.from_dict(create_route_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


