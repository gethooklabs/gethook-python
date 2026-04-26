# IngestAcceptedData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**status** | **str** |  | 

## Example

```python
from gethook.models.ingest_accepted_data import IngestAcceptedData

# TODO update the JSON string below
json = "{}"
# create an instance of IngestAcceptedData from a JSON string
ingest_accepted_data_instance = IngestAcceptedData.from_json(json)
# print the JSON string representation of the object
print(IngestAcceptedData.to_json())

# convert the object into a dict
ingest_accepted_data_dict = ingest_accepted_data_instance.to_dict()
# create an instance of IngestAcceptedData from a dict
ingest_accepted_data_from_dict = IngestAcceptedData.from_dict(ingest_accepted_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


