# UsageSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The id | [optional] 
**company_id** | **str** | The company id | [optional] 
**product_id** | **str** | The product id | [optional] 
**resource_group** | **str** | Resource group assigned to the usage summary | [optional] 
**vendor_name** | **str** | Vendor Name | [optional] 
**current_charges** | **float** | Charges for the current month | [optional] 
**currency_code** | **str** | The currency ISO 4217 code | [optional] 
**partner_total** | **float** | The partner total for the current month | [optional] 
**is_trial** | **bool** | Indicates whether the usage summary is for a trial | [optional] 

## Example

```python
from tl_pax8.models.usage_summary import UsageSummary

# TODO update the JSON string below
json = "{}"
# create an instance of UsageSummary from a JSON string
usage_summary_instance = UsageSummary.from_json(json)
# print the JSON string representation of the object
print(UsageSummary.to_json())

# convert the object into a dict
usage_summary_dict = usage_summary_instance.to_dict()
# create an instance of UsageSummary from a dict
usage_summary_from_dict = UsageSummary.from_dict(usage_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


