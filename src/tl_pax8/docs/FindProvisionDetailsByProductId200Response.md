# FindProvisionDetailsByProductId200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | [**List[ProvisioningDetail]**](ProvisioningDetail.md) |  | [optional] 

## Example

```python
from tl_pax8.models.find_provision_details_by_product_id200_response import FindProvisionDetailsByProductId200Response

# TODO update the JSON string below
json = "{}"
# create an instance of FindProvisionDetailsByProductId200Response from a JSON string
find_provision_details_by_product_id200_response_instance = FindProvisionDetailsByProductId200Response.from_json(json)
# print the JSON string representation of the object
print(FindProvisionDetailsByProductId200Response.to_json())

# convert the object into a dict
find_provision_details_by_product_id200_response_dict = find_provision_details_by_product_id200_response_instance.to_dict()
# create an instance of FindProvisionDetailsByProductId200Response from a dict
find_provision_details_by_product_id200_response_from_dict = FindProvisionDetailsByProductId200Response.from_dict(find_provision_details_by_product_id200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


