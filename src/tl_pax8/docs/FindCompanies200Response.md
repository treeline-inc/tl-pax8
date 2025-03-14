# FindCompanies200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | [**List[Company]**](Company.md) |  | [optional] 
**page** | [**Page**](Page.md) |  | [optional] 

## Example

```python
from tl_pax8.models.find_companies200_response import FindCompanies200Response

# TODO update the JSON string below
json = "{}"
# create an instance of FindCompanies200Response from a JSON string
find_companies200_response_instance = FindCompanies200Response.from_json(json)
# print the JSON string representation of the object
print(FindCompanies200Response.to_json())

# convert the object into a dict
find_companies200_response_dict = find_companies200_response_instance.to_dict()
# create an instance of FindCompanies200Response from a dict
find_companies200_response_from_dict = FindCompanies200Response.from_dict(find_companies200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


