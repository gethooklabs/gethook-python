# PlatformStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**delivery_attempts** | **int** |  | [optional] 
**events_delivered** | **int** |  | [optional] 
**events_processed** | **int** |  | [optional] 
**success_rate_pct** | **float** |  | [optional] 

## Example

```python
from gethook.models.platform_stats import PlatformStats

# TODO update the JSON string below
json = "{}"
# create an instance of PlatformStats from a JSON string
platform_stats_instance = PlatformStats.from_json(json)
# print the JSON string representation of the object
print(PlatformStats.to_json())

# convert the object into a dict
platform_stats_dict = platform_stats_instance.to_dict()
# create an instance of PlatformStats from a dict
platform_stats_from_dict = PlatformStats.from_dict(platform_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


