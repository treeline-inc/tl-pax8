# ProductDependency


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | The name of the product constraint | [optional] 
**products** | [**List[Product]**](Product.md) | A list of products that satisfy the constraint | [optional] 

## Example

```python
from tl_pax8.models.product_dependency import ProductDependency

# TODO update the JSON string below
json = "{}"
# create an instance of ProductDependency from a JSON string
product_dependency_instance = ProductDependency.from_json(json)
# print the JSON string representation of the object
print(ProductDependency.to_json())

# convert the object into a dict
product_dependency_dict = product_dependency_instance.to_dict()
# create an instance of ProductDependency from a dict
product_dependency_from_dict = ProductDependency.from_dict(product_dependency_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


