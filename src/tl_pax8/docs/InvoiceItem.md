# InvoiceItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The unique id for this invoice item | [optional] 
**purchase_order_number** | **str** | The purchase order number | [optional] 
**type** | **str** | The item type | [optional] 
**company_id** | **str** | The company id | [optional] 
**external_id** | **str** | The company external id | [optional] 
**company_name** | **str** | The name of the company | [optional] 
**start_period** | **str** | The start period | [optional] 
**end_period** | **str** | The end period | [optional] 
**quantity** | **float** | The quantity of this SKU | [optional] 
**unit_of_measure** | **str** | The unit of measure | [optional] 
**term** | **str** | The billing term | [optional] 
**sku** | **str** | The product sku | [optional] 
**description** | **str** | The description | [optional] 
**details** | **str** | The details | [optional] 
**rate_type** | **str** | The rate type | [optional] 
**charge_type** | **str** | The charge type | [optional] 
**price** | **float** | The customer unit price | [optional] 
**sub_total** | **float** | The customer sub total. Represents cost of services plus billing fees. | [optional] 
**cost** | **float** | The partner unit cost | [optional] 
**cost_total** | **float** | The partner total cost of the services | [optional] 
**offered_by** | **str** | The account who offers this product | [optional] 
**billed_by_pax8** | **bool** | Is the item billed directly by Pax8 | [optional] 
**total** | **float** | The customer total including all services and fees | [optional] 
**product_id** | **str** | The product id | [optional] 
**product_name** | **str** | The product name | [optional] 
**billing_fee** | **float** | The fee for Pax8 billing a bill on behalf of company | [optional] 
**billing_fee_rate** | **float** | The fee rate for Pax8 billing a bill on behalf of company | [optional] 
**amount_due** | **float** | The final total due for the item for this invoice | [optional] 
**currency_code** | **str** | The currency ISO 4217 code | [optional] 
**subscription_id** | **str** | If the type is &#39;subscription&#39; or &#39;prorate&#39; this field will contain the subscription identifier. Otherwise this field will be null. | [optional] 

## Example

```python
from tl_pax8.models.invoice_item import InvoiceItem

# TODO update the JSON string below
json = "{}"
# create an instance of InvoiceItem from a JSON string
invoice_item_instance = InvoiceItem.from_json(json)
# print the JSON string representation of the object
print(InvoiceItem.to_json())

# convert the object into a dict
invoice_item_dict = invoice_item_instance.to_dict()
# create an instance of InvoiceItem from a dict
invoice_item_from_dict = InvoiceItem.from_dict(invoice_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


