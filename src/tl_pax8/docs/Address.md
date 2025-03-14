# Address


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**street** | **str** | The primary street information | [optional] 
**street2** | **str** | The secondary street information | [optional] 
**city** | **str** | The city | [optional] 
**state_or_province** | **str** | The state or province | [optional] 
**postal_code** | **str** | The postal code | [optional] 
**country** | **str** | The country | [optional] 

## Example

```python
from tl_pax8.models.address import Address

# TODO update the JSON string below
json = "{}"
# create an instance of Address from a JSON string
address_instance = Address.from_json(json)
# print the JSON string representation of the object
print(Address.to_json())

# convert the object into a dict
address_dict = address_instance.to_dict()
# create an instance of Address from a dict
address_from_dict = Address.from_dict(address_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


