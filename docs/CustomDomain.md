# CustomDomain


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | 
**created_at** | **str** |  | 
**domain** | **str** |  | 
**id** | **str** |  | 
**status** | **str** |  | 
**tls_status** | **str** |  | 
**type** | **str** |  | 
**verification_token** | **str** |  | 

## Example

```python
from gethook.models.custom_domain import CustomDomain

# TODO update the JSON string below
json = "{}"
# create an instance of CustomDomain from a JSON string
custom_domain_instance = CustomDomain.from_json(json)
# print the JSON string representation of the object
print(CustomDomain.to_json())

# convert the object into a dict
custom_domain_dict = custom_domain_instance.to_dict()
# create an instance of CustomDomain from a dict
custom_domain_from_dict = CustomDomain.from_dict(custom_domain_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


