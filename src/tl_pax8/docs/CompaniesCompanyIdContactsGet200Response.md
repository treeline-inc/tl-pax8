# CompaniesCompanyIdContactsGet200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | [**List[Contact]**](Contact.md) |  | [optional] 
**page** | [**Page**](Page.md) |  | [optional] 

## Example

```python
from tl_pax8.models.companies_company_id_contacts_get200_response import CompaniesCompanyIdContactsGet200Response

# TODO update the JSON string below
json = "{}"
# create an instance of CompaniesCompanyIdContactsGet200Response from a JSON string
companies_company_id_contacts_get200_response_instance = CompaniesCompanyIdContactsGet200Response.from_json(json)
# print the JSON string representation of the object
print(CompaniesCompanyIdContactsGet200Response.to_json())

# convert the object into a dict
companies_company_id_contacts_get200_response_dict = companies_company_id_contacts_get200_response_instance.to_dict()
# create an instance of CompaniesCompanyIdContactsGet200Response from a dict
companies_company_id_contacts_get200_response_from_dict = CompaniesCompanyIdContactsGet200Response.from_dict(companies_company_id_contacts_get200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


