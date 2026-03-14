# APIKeyWithSecret


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | 
**created_at** | **str** |  | 
**id** | **str** |  | 
**key** | **str** |  | 
**key_prefix** | **str** |  | 
**name** | **str** |  | 
**revoked_at** | **str** |  | [optional] 

## Example

```python
from gethook.models.api_key_with_secret import APIKeyWithSecret

# TODO update the JSON string below
json = "{}"
# create an instance of APIKeyWithSecret from a JSON string
api_key_with_secret_instance = APIKeyWithSecret.from_json(json)
# print the JSON string representation of the object
print(APIKeyWithSecret.to_json())

# convert the object into a dict
api_key_with_secret_dict = api_key_with_secret_instance.to_dict()
# create an instance of APIKeyWithSecret from a dict
api_key_with_secret_from_dict = APIKeyWithSecret.from_dict(api_key_with_secret_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


