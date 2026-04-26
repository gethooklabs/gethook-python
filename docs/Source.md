# Source


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | 
**auth_mode** | **str** |  | 
**created_at** | **str** |  | 
**custom_domain_id** | **str** |  | [optional] 
**id** | **str** |  | 
**ingest_url** | **str** |  | 
**name** | **str** |  | 
**path_token** | **str** |  | 
**provider** | **str** |  | [optional] 
**status** | **str** |  | 
**verification_config** | **object** |  | [optional] 

## Example

```python
from gethook.models.source import Source

# TODO update the JSON string below
json = "{}"
# create an instance of Source from a JSON string
source_instance = Source.from_json(json)
# print the JSON string representation of the object
print(Source.to_json())

# convert the object into a dict
source_dict = source_instance.to_dict()
# create an instance of Source from a dict
source_from_dict = Source.from_dict(source_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


