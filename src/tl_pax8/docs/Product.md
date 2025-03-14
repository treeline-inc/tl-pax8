# Product


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] [readonly] 
**name** | **str** | The name of a product | [optional] 
**vendor_name** | **str** | The name of the vendor | [optional] 
**short_description** | **str** | A short description of the product | [optional] 
**sku** | **str** | The product sku | [optional] 
**vendor_sku** | **str** | The product vendor sku | [optional] 
**alt_vendor_sku** | **str** | The Microsoft legacy sku has been deprecated. Please transition to vendorSku | [optional] 
**requires_commitment** | **bool** | Whether the product requires a commitment | [optional] 

## Example

```python
from tl_pax8.models.product import Product

# TODO update the JSON string below
json = "{}"
# create an instance of Product from a JSON string
product_instance = Product.from_json(json)
# print the JSON string representation of the object
print(Product.to_json())

# convert the object into a dict
product_dict = product_instance.to_dict()
# create an instance of Product from a dict
product_from_dict = Product.from_dict(product_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


