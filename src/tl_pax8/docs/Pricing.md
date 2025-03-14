# Pricing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**billing_term** | **str** |  | [optional] 
**commitment_term** | **str** | Duration of the commitment | [optional] 
**commitment_term_in_months** | **float** | Commitment in months | [optional] 
**type** | **str** |  | [optional] 
**unit_of_measurement** | **str** | The unit of measurement | [optional] 
**rates** | [**List[Rate]**](Rate.md) | A list of rates | [optional] 

## Example

```python
from tl_pax8.models.pricing import Pricing

# TODO update the JSON string below
json = "{}"
# create an instance of Pricing from a JSON string
pricing_instance = Pricing.from_json(json)
# print the JSON string representation of the object
print(Pricing.to_json())

# convert the object into a dict
pricing_dict = pricing_instance.to_dict()
# create an instance of Pricing from a dict
pricing_from_dict = Pricing.from_dict(pricing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


