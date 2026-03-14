# ProviderPreset


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**auth_mode** | **str** |  | [optional] 
**category** | **str** |  | [optional] 
**color** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**docs_url** | **str** |  | [optional] 
**header** | **str** |  | [optional] 
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 

## Example

```python
from gethook.models.provider_preset import ProviderPreset

# TODO update the JSON string below
json = "{}"
# create an instance of ProviderPreset from a JSON string
provider_preset_instance = ProviderPreset.from_json(json)
# print the JSON string representation of the object
print(ProviderPreset.to_json())

# convert the object into a dict
provider_preset_dict = provider_preset_instance.to_dict()
# create an instance of ProviderPreset from a dict
provider_preset_from_dict = ProviderPreset.from_dict(provider_preset_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


