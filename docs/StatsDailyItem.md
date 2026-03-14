# StatsDailyItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **str** |  | 
**delivered** | **int** |  | 
**failed** | **int** |  | 
**inbound** | **int** |  | 
**outbound** | **int** |  | 

## Example

```python
from gethook.models.stats_daily_item import StatsDailyItem

# TODO update the JSON string below
json = "{}"
# create an instance of StatsDailyItem from a JSON string
stats_daily_item_instance = StatsDailyItem.from_json(json)
# print the JSON string representation of the object
print(StatsDailyItem.to_json())

# convert the object into a dict
stats_daily_item_dict = stats_daily_item_instance.to_dict()
# create an instance of StatsDailyItem from a dict
stats_daily_item_from_dict = StatsDailyItem.from_dict(stats_daily_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


