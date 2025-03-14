# ContactType


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | A company must have a primary contact for each contact type. A single contact can be marked as a primary contact for all types Contact Type:   * &#x60;Admin&#x60; - Administrative contact   * &#x60;Billing&#x60; - Billing contact   * &#x60;Technical&#x60; - Technical contact  | [optional] 
**primary** | **bool** | Is this contact the primary contact for this Contact Type | [optional] 

## Example

```python
from tl_pax8.models.contact_type import ContactType

# TODO update the JSON string below
json = "{}"
# create an instance of ContactType from a JSON string
contact_type_instance = ContactType.from_json(json)
# print the JSON string representation of the object
print(ContactType.to_json())

# convert the object into a dict
contact_type_dict = contact_type_instance.to_dict()
# create an instance of ContactType from a dict
contact_type_from_dict = ContactType.from_dict(contact_type_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


