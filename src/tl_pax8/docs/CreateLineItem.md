# CreateLineItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] [readonly] 
**product_id** | **str** |  | 
**commitment_term_id** | **str** | This field is required when the product associated with the order has requiresCommitment field set to true. To pick the correct commitment term, use the https://devx.pax8.com/reference/findproductdependenciesbyproductid endpoint and chose a commitment term whose term field represents an equal or greater time than the desired billingTerm. For example, when the order billingTerm is annual, pass the identifier of the commitment term that matches an annual commitment, or if desired and available, pass a commitment term id of 2-year, or 3-year | [optional] 
**provision_start_date** | **datetime** |  | [optional] 
**line_item_number** | **float** | Required. Number used as a reference to the line item for parent line items | 
**billing_term** | **str** |  | 
**parent_subscription_id** | **str** | Reference to the subscription this item depends on | [optional] 
**parent_line_item_number** | **float** | Reference to the required parent line item in this same order | [optional] 
**quantity** | **float** | Whole Number | 
**provisioning_details** | [**List[ProvisioningDetail]**](ProvisioningDetail.md) |  | [optional] 

## Example

```python
from tl_pax8.models.create_line_item import CreateLineItem

# TODO update the JSON string below
json = "{}"
# create an instance of CreateLineItem from a JSON string
create_line_item_instance = CreateLineItem.from_json(json)
# print the JSON string representation of the object
print(CreateLineItem.to_json())

# convert the object into a dict
create_line_item_dict = create_line_item_instance.to_dict()
# create an instance of CreateLineItem from a dict
create_line_item_from_dict = CreateLineItem.from_dict(create_line_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


