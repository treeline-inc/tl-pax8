# Rate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**partner_buy_rate** | **float** | The partner cost | [optional] 
**suggested_retail_price** | **float** | The suggested customer cost | [optional] 
**start_quantity_range** | **float** | The start of the quantity range. If not set 0 is the default | [optional] 
**end_quantity_range** | **float** | The end of the quantity range. If &#x60;&#x60;&#x60;null&#x60;&#x60;&#x60; there is no end of range | [optional] 
**charge_type** | **str** | Rate Charge Type:   * &#x60;Per Unit&#x60; - The rate is multiplied directly by the quantity based on the start and end quantity range   * &#x60;Flat Rate&#x60; - The rate is flat for the quantity based on the start and end quantity range  | [optional] 

## Example

```python
from tl_pax8.models.rate import Rate

# TODO update the JSON string below
json = "{}"
# create an instance of Rate from a JSON string
rate_instance = Rate.from_json(json)
# print the JSON string representation of the object
print(Rate.to_json())

# convert the object into a dict
rate_dict = rate_instance.to_dict()
# create an instance of Rate from a dict
rate_from_dict = Rate.from_dict(rate_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


