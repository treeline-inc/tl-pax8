# LineItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] [readonly] 
**product_id** | **str** |  | 
**subscription_id** | **str** |  | [optional] 
**commitment_term_id** | **str** |  | [optional] 
**provision_start_date** | **datetime** |  | [optional] 
**line_item_number** | **float** | Required. Number used as a reference to the line item for parent line items | 
**billing_term** | **str** |  | [optional] 
**parent_subscription_id** | **str** | Reference to the subscription this item depends on | [optional] 
**parent_line_item_number** | **float** | Reference to the required parent line item in this same order | [optional] 
**quantity** | **float** | Whole Number | 
**provisioning_details** | [**List[ProvisioningDetail]**](ProvisioningDetail.md) |  | [optional] 

## Example

```python
from tl_pax8.models.line_item import LineItem

# TODO update the JSON string below
json = "{}"
# create an instance of LineItem from a JSON string
line_item_instance = LineItem.from_json(json)
# print the JSON string representation of the object
print(LineItem.to_json())

# convert the object into a dict
line_item_dict = line_item_instance.to_dict()
# create an instance of LineItem from a dict
line_item_from_dict = LineItem.from_dict(line_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


