# UpsertBrandSettingsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**company_name** | **str** |  | [optional] 
**docs_title** | **str** |  | [optional] 
**logo_url** | **str** |  | [optional] 
**primary_color** | **str** |  | [optional] 
**support_email** | **str** |  | [optional] 

## Example

```python
from gethook.models.upsert_brand_settings_request import UpsertBrandSettingsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpsertBrandSettingsRequest from a JSON string
upsert_brand_settings_request_instance = UpsertBrandSettingsRequest.from_json(json)
# print the JSON string representation of the object
print(UpsertBrandSettingsRequest.to_json())

# convert the object into a dict
upsert_brand_settings_request_dict = upsert_brand_settings_request_instance.to_dict()
# create an instance of UpsertBrandSettingsRequest from a dict
upsert_brand_settings_request_from_dict = UpsertBrandSettingsRequest.from_dict(upsert_brand_settings_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


