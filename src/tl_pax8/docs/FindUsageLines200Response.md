# FindUsageLines200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | [**List[UsageLine]**](UsageLine.md) |  | [optional] 
**page** | [**Page**](Page.md) |  | [optional] 

## Example

```python
from tl_pax8.models.find_usage_lines200_response import FindUsageLines200Response

# TODO update the JSON string below
json = "{}"
# create an instance of FindUsageLines200Response from a JSON string
find_usage_lines200_response_instance = FindUsageLines200Response.from_json(json)
# print the JSON string representation of the object
print(FindUsageLines200Response.to_json())

# convert the object into a dict
find_usage_lines200_response_dict = find_usage_lines200_response_instance.to_dict()
# create an instance of FindUsageLines200Response from a dict
find_usage_lines200_response_from_dict = FindUsageLines200Response.from_dict(find_usage_lines200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


