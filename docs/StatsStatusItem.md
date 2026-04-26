# StatsStatusItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count** | **int** |  | 
**status** | **str** |  | 

## Example

```python
from gethook.models.stats_status_item import StatsStatusItem

# TODO update the JSON string below
json = "{}"
# create an instance of StatsStatusItem from a JSON string
stats_status_item_instance = StatsStatusItem.from_json(json)
# print the JSON string representation of the object
print(StatsStatusItem.to_json())

# convert the object into a dict
stats_status_item_dict = stats_status_item_instance.to_dict()
# create an instance of StatsStatusItem from a dict
stats_status_item_from_dict = StatsStatusItem.from_dict(stats_status_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


