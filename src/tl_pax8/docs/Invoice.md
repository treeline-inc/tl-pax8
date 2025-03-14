# Invoice


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The id | [optional] 
**invoice_date** | **str** | The date the invoice is generated for | [optional] 
**due_date** | **str** | The date on which payment is due | [optional] 
**balance** | **float** | The current invoice balance | [optional] 
**carried_balance** | **float** | The outstanding balance until current invoiceDate | [optional] 
**total** | **float** | The total amount due | [optional] 
**currency_code** | **str** | The currency ISO 4217 code | [optional] 
**partner_name** | **str** | The name of the invoiced partner | [optional] 
**company_id** | **str** | The company id | [optional] 
**external_id** | **str** | The company external id | [optional] 

## Example

```python
from tl_pax8.models.invoice import Invoice

# TODO update the JSON string below
json = "{}"
# create an instance of Invoice from a JSON string
invoice_instance = Invoice.from_json(json)
# print the JSON string representation of the object
print(Invoice.to_json())

# convert the object into a dict
invoice_dict = invoice_instance.to_dict()
# create an instance of Invoice from a dict
invoice_from_dict = Invoice.from_dict(invoice_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


