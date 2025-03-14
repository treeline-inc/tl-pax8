# CompanyUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The unique id of the company | [optional] [readonly] 
**name** | **str** | The company name | [optional] 
**address** | [**Address**](Address.md) |  | [optional] 
**phone** | **str** | The primary phone number of the company | [optional] 
**website** | **str** | The full URL of the company website | [optional] 
**external_id** | **str** | An external ID that can be assigned to the company for reference | [optional] 
**bill_on_behalf_of_enabled** | **bool** | Value is &#x60;&#x60;&#x60;true&#x60;&#x60;&#x60; if Pax8 handles billing transactions, value is &#x60;&#x60;&#x60;false&#x60;&#x60;&#x60; if partner handles billing transactions | [optional] 
**self_service_allowed** | **bool** | Value is &#x60;&#x60;&#x60;true&#x60;&#x60;&#x60; if self-service privileges are available to the company, otherwise value is &#x60;&#x60;&#x60;false&#x60;&#x60;&#x60; | [optional] 
**order_approval_required** | **bool** | Value is &#x60;&#x60;&#x60;true&#x60;&#x60;&#x60; if the company&#39;s self-service orders require approval, otherwise value is &#x60;&#x60;&#x60;false&#x60;&#x60;&#x60; | [optional] 
**status** | **str** | Company Status:   * &#x60;Active&#x60; - The company is active   * &#x60;Inactive&#x60; - The company is inactive due to missing contacts   * &#x60;Deleted&#x60; - The company has been deleted  | [optional] [readonly] 

## Example

```python
from tl_pax8.models.company_update import CompanyUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of CompanyUpdate from a JSON string
company_update_instance = CompanyUpdate.from_json(json)
# print the JSON string representation of the object
print(CompanyUpdate.to_json())

# convert the object into a dict
company_update_dict = company_update_instance.to_dict()
# create an instance of CompanyUpdate from a dict
company_update_from_dict = CompanyUpdate.from_dict(company_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


