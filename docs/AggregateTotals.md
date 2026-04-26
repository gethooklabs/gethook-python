# AggregateTotals

Authoritative event totals derived from event_daily_stats (past days) plus live events (today). Accurate even after events are purged by the retention cleaner. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** |  | 
**delivered** | **int** |  | 
**failed** | **int** |  | 

## Example

```python
from gethook.models.aggregate_totals import AggregateTotals

# TODO update the JSON string below
json = "{}"
# create an instance of AggregateTotals from a JSON string
aggregate_totals_instance = AggregateTotals.from_json(json)
# print the JSON string representation of the object
print(AggregateTotals.to_json())

# convert the object into a dict
aggregate_totals_dict = aggregate_totals_instance.to_dict()
# create an instance of AggregateTotals from a dict
aggregate_totals_from_dict = AggregateTotals.from_dict(aggregate_totals_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


