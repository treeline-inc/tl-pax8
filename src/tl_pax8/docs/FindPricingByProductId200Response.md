# FindPricingByProductId200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | [**List[Pricing]**](Pricing.md) |  | [optional] 

## Example

```python
from tl_pax8.models.find_pricing_by_product_id200_response import FindPricingByProductId200Response

# TODO update the JSON string below
json = "{}"
# create an instance of FindPricingByProductId200Response from a JSON string
find_pricing_by_product_id200_response_instance = FindPricingByProductId200Response.from_json(json)
# print the JSON string representation of the object
print(FindPricingByProductId200Response.to_json())

# convert the object into a dict
find_pricing_by_product_id200_response_dict = find_pricing_by_product_id200_response_instance.to_dict()
# create an instance of FindPricingByProductId200Response from a dict
find_pricing_by_product_id200_response_from_dict = FindPricingByProductId200Response.from_dict(find_pricing_by_product_id200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


