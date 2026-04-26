# DestinationPreset


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**auth_header** | **str** | for api_key type | [optional] 
**auth_label** | **str** | e.g. \&quot;Bot Token\&quot;, \&quot;API Key\&quot; | [optional] 
**auth_type** | **str** | \&quot;none\&quot;, \&quot;bearer\&quot;, \&quot;api_key\&quot; | [optional] 
**category** | **str** |  | [optional] 
**color** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**docs_url** | **str** |  | [optional] 
**extra_headers** | **Dict[str, str]** |  | [optional] 
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**url_hint** | **str** |  | [optional] 

## Example

```python
from gethook.models.destination_preset import DestinationPreset

# TODO update the JSON string below
json = "{}"
# create an instance of DestinationPreset from a JSON string
destination_preset_instance = DestinationPreset.from_json(json)
# print the JSON string representation of the object
print(DestinationPreset.to_json())

# convert the object into a dict
destination_preset_dict = destination_preset_instance.to_dict()
# create an instance of DestinationPreset from a dict
destination_preset_from_dict = DestinationPreset.from_dict(destination_preset_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


