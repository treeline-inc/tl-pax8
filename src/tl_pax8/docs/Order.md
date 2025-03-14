# Order


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | unique id of the order | [optional] [readonly] 
**company_id** | **str** | unique id of the purchasing company ie. end-user | 
**created_date** | **date** | the date the order was created | [optional] [readonly] 
**ordered_by** | **str** | the type of user who created the order | [optional] 
**ordered_by_user_id** | **str** | unique id of the user who created this order | [optional] [readonly] 
**ordered_by_user_email** | **str** | the email address of the user who created this order | [optional] 
**is_scheduled** | **bool** | is &#x60;&#x60;&#x60;true&#x60;&#x60;&#x60; if order is future dated | [optional] [readonly] 
**line_items** | [**List[LineItem]**](LineItem.md) |  | 

## Example

```python
from tl_pax8.models.order import Order

# TODO update the JSON string below
json = "{}"
# create an instance of Order from a JSON string
order_instance = Order.from_json(json)
# print the JSON string representation of the object
print(Order.to_json())

# convert the object into a dict
order_dict = order_instance.to_dict()
# create an instance of Order from a dict
order_from_dict = Order.from_dict(order_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


