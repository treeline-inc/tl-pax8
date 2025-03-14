# ProvisioningDetail


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label** | **str** | The label to display | [optional] [readonly] 
**key** | **str** | The key | [optional] 
**values** | **List[str]** | A list of values based on the &#x60;&#x60;&#x60;valuetype&#x60;&#x60;&#x60; and &#x60;&#x60;&#x60;possibleValues&#x60;&#x60;&#x60; | [optional] 
**description** | **str** | Instructions and context to help enter the required provisioning information | [optional] [readonly] 
**value_type** | **str** | Provisioning Detail Value Type:  * &#x60;Input&#x60; - A value that is supplied by a user  * &#x60;Single-Value&#x60; - A single value that is picked from the &#x60;possibleValues&#x60; list  * &#x60;Multi-Value&#x60; - One or multiple values that are picked from the &#x60;possibleValues&#x60; list  | [optional] [readonly] 
**possible_values** | **List[str]** | A list of possible values. &#x60;possibleValues&#x60; will be null when &#x60;valueType&#x60; is &#x60;Input&#x60; | [optional] [readonly] 

## Example

```python
from tl_pax8.models.provisioning_detail import ProvisioningDetail

# TODO update the JSON string below
json = "{}"
# create an instance of ProvisioningDetail from a JSON string
provisioning_detail_instance = ProvisioningDetail.from_json(json)
# print the JSON string representation of the object
print(ProvisioningDetail.to_json())

# convert the object into a dict
provisioning_detail_dict = provisioning_detail_instance.to_dict()
# create an instance of ProvisioningDetail from a dict
provisioning_detail_from_dict = ProvisioningDetail.from_dict(provisioning_detail_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


