# BrandSettings


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | 
**company_name** | **str** |  | [optional] 
**created_at** | **str** |  | 
**docs_title** | **str** |  | [optional] 
**id** | **str** |  | 
**logo_url** | **str** |  | [optional] 
**primary_color** | **str** |  | [optional] 
**support_email** | **str** |  | [optional] 
**updated_at** | **str** |  | 

## Example

```python
from gethook.models.brand_settings import BrandSettings

# TODO update the JSON string below
json = "{}"
# create an instance of BrandSettings from a JSON string
brand_settings_instance = BrandSettings.from_json(json)
# print the JSON string representation of the object
print(BrandSettings.to_json())

# convert the object into a dict
brand_settings_dict = brand_settings_instance.to_dict()
# create an instance of BrandSettings from a dict
brand_settings_from_dict = BrandSettings.from_dict(brand_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


