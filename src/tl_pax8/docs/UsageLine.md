# UsageLine


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**usage_summary_id** | **str** | The associated usage summary id | [optional] 
**usage_date** | **str** | The date the usage was recorded | [optional] 
**product_name** | **str** | The usage product name | [optional] 
**product_id** | **str** | The usage product id | [optional] 
**unit_of_measure** | **str** | The product unit of measure | [optional] 
**quantity** | **float** | The usage quantity | [optional] 
**current_charges** | **float** | Charges for the usage line | [optional] 
**current_profit** | **float** | Profit for the usage line | [optional] 
**partner_total** | **float** | The partner total for the usage line | [optional] 
**unit_price** | **float** | The unit price of the usage product | [optional] 
**currency_code** | **str** | The currency ISO 4217 code | [optional] 
**is_trial** | **bool** | Indicates if the usage line is for a trial | [optional] 

## Example

```python
from tl_pax8.models.usage_line import UsageLine

# TODO update the JSON string below
json = "{}"
# create an instance of UsageLine from a JSON string
usage_line_instance = UsageLine.from_json(json)
# print the JSON string representation of the object
print(UsageLine.to_json())

# convert the object into a dict
usage_line_dict = usage_line_instance.to_dict()
# create an instance of UsageLine from a dict
usage_line_from_dict = UsageLine.from_dict(usage_line_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


