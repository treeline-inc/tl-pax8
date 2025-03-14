# FindPartnerInvoiceItems200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | [**List[InvoiceItem]**](InvoiceItem.md) |  | [optional] 
**page** | [**Page**](Page.md) |  | [optional] 

## Example

```python
from tl_pax8.models.find_partner_invoice_items200_response import FindPartnerInvoiceItems200Response

# TODO update the JSON string below
json = "{}"
# create an instance of FindPartnerInvoiceItems200Response from a JSON string
find_partner_invoice_items200_response_instance = FindPartnerInvoiceItems200Response.from_json(json)
# print the JSON string representation of the object
print(FindPartnerInvoiceItems200Response.to_json())

# convert the object into a dict
find_partner_invoice_items200_response_dict = find_partner_invoice_items200_response_instance.to_dict()
# create an instance of FindPartnerInvoiceItems200Response from a dict
find_partner_invoice_items200_response_from_dict = FindPartnerInvoiceItems200Response.from_dict(find_partner_invoice_items200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


