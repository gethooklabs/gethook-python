# AccountBootstrapData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account** | [**Account**](Account.md) |  | 
**api_key** | [**APIKeyWithSecret**](APIKeyWithSecret.md) |  | 

## Example

```python
from gethook.models.account_bootstrap_data import AccountBootstrapData

# TODO update the JSON string below
json = "{}"
# create an instance of AccountBootstrapData from a JSON string
account_bootstrap_data_instance = AccountBootstrapData.from_json(json)
# print the JSON string representation of the object
print(AccountBootstrapData.to_json())

# convert the object into a dict
account_bootstrap_data_dict = account_bootstrap_data_instance.to_dict()
# create an instance of AccountBootstrapData from a dict
account_bootstrap_data_from_dict = AccountBootstrapData.from_dict(account_bootstrap_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


