# tl_pax8.InvoicesApi

All URIs are relative to *https://api.pax8.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**find_partner_invoice_items**](InvoicesApi.md#find_partner_invoice_items) | **GET** /invoices/{invoiceId}/items | Fetch a paginated list of items for an invoice
[**find_partner_invoices**](InvoicesApi.md#find_partner_invoices) | **GET** /invoices | Fetch a paginated list of invoices
[**get_partner_invoice**](InvoicesApi.md#get_partner_invoice) | **GET** /invoices/{invoiceId} | Fetch an invoice by invoiceId


# **find_partner_invoice_items**
> FindPartnerInvoiceItems200Response find_partner_invoice_items(invoice_id, page=page, size=size)

Fetch a paginated list of items for an invoice

Fetch a paginated list of invoice items. Default page is 0 and default size is 10. The maximum page size is 200

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.find_partner_invoice_items200_response import FindPartnerInvoiceItems200Response
from tl_pax8.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.pax8.com/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = tl_pax8.Configuration(
    host = "https://api.pax8.com/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

configuration.access_token = os.environ["ACCESS_TOKEN"]

# Enter a context with an instance of the API client
with tl_pax8.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = tl_pax8.InvoicesApi(api_client)
    invoice_id = '57328a3c-6e95-493c-ad2f-e33b896378c7' # str | The invoice id
    page = 0 # float | The page number to request in the invoices items list (optional) (default to 0)
    size = 10 # float | Returns _this_ number of invoices items per page (optional) (default to 10)

    try:
        # Fetch a paginated list of items for an invoice
        api_response = api_instance.find_partner_invoice_items(invoice_id, page=page, size=size)
        print("The response of InvoicesApi->find_partner_invoice_items:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InvoicesApi->find_partner_invoice_items: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **invoice_id** | **str**| The invoice id | 
 **page** | **float**| The page number to request in the invoices items list | [optional] [default to 0]
 **size** | **float**| Returns _this_ number of invoices items per page | [optional] [default to 10]

### Return type

[**FindPartnerInvoiceItems200Response**](FindPartnerInvoiceItems200Response.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Invalid invoice id |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **find_partner_invoices**
> FindPartnerInvoices200Response find_partner_invoices(page=page, size=size, sort=sort, status=status, invoice_date=invoice_date, invoice_date_range_start=invoice_date_range_start, invoice_date_range_end=invoice_date_range_end, due_date=due_date, total=total, balance=balance, carried_balance=carried_balance, company_id=company_id)

Fetch a paginated list of invoices

Fetch a paginated list of invoices. Default page is 0 and default size is 10. The maximum page size is 200

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.find_partner_invoices200_response import FindPartnerInvoices200Response
from tl_pax8.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.pax8.com/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = tl_pax8.Configuration(
    host = "https://api.pax8.com/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

configuration.access_token = os.environ["ACCESS_TOKEN"]

# Enter a context with an instance of the API client
with tl_pax8.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = tl_pax8.InvoicesApi(api_client)
    page = 0 # float | The page number to request in the invoices list (optional) (default to 0)
    size = 10 # float | Returns _this_ number of invoices per page (optional) (default to 10)
    sort = 'sort_example' # str | Return invoices sorted by this field and direction Formatted as fieldName,direction - ex. sort=invoiceDate,desc (optional)
    status = 'status_example' # str | Return only invoices matching this ```status``` value (optional)
    invoice_date = '2000-10-31' # str | Return only invoices matching this ```invoiceDate``` value (optional)
    invoice_date_range_start = '2000-10-31' # str | Return only invoices with an ```invoiceDate``` greater than or equal to this date (optional)
    invoice_date_range_end = '2001-10-31' # str | Return only invoices with an ```invoiceDate``` less than or equal to this date (optional)
    due_date = '2000-10-31' # str | Return only invoices matching this ```dueDate``` value (optional)
    total = 100.00 # float | Return only invoices matching this ```total``` value (optional)
    balance = 1000.00 # float | Return only invoices matching this ```balance``` value (optional)
    carried_balance = 2000.00 # float | Return only invoices matching this ```carriedBalance``` value (optional)
    company_id = 'f7fc273a-8d86-45c9-a26f-ffd42416adda' # str | Return only invoices matching this ```companyId``` value (optional)

    try:
        # Fetch a paginated list of invoices
        api_response = api_instance.find_partner_invoices(page=page, size=size, sort=sort, status=status, invoice_date=invoice_date, invoice_date_range_start=invoice_date_range_start, invoice_date_range_end=invoice_date_range_end, due_date=due_date, total=total, balance=balance, carried_balance=carried_balance, company_id=company_id)
        print("The response of InvoicesApi->find_partner_invoices:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InvoicesApi->find_partner_invoices: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float**| The page number to request in the invoices list | [optional] [default to 0]
 **size** | **float**| Returns _this_ number of invoices per page | [optional] [default to 10]
 **sort** | **str**| Return invoices sorted by this field and direction Formatted as fieldName,direction - ex. sort&#x3D;invoiceDate,desc | [optional] 
 **status** | **str**| Return only invoices matching this &#x60;&#x60;&#x60;status&#x60;&#x60;&#x60; value | [optional] 
 **invoice_date** | **str**| Return only invoices matching this &#x60;&#x60;&#x60;invoiceDate&#x60;&#x60;&#x60; value | [optional] 
 **invoice_date_range_start** | **str**| Return only invoices with an &#x60;&#x60;&#x60;invoiceDate&#x60;&#x60;&#x60; greater than or equal to this date | [optional] 
 **invoice_date_range_end** | **str**| Return only invoices with an &#x60;&#x60;&#x60;invoiceDate&#x60;&#x60;&#x60; less than or equal to this date | [optional] 
 **due_date** | **str**| Return only invoices matching this &#x60;&#x60;&#x60;dueDate&#x60;&#x60;&#x60; value | [optional] 
 **total** | **float**| Return only invoices matching this &#x60;&#x60;&#x60;total&#x60;&#x60;&#x60; value | [optional] 
 **balance** | **float**| Return only invoices matching this &#x60;&#x60;&#x60;balance&#x60;&#x60;&#x60; value | [optional] 
 **carried_balance** | **float**| Return only invoices matching this &#x60;&#x60;&#x60;carriedBalance&#x60;&#x60;&#x60; value | [optional] 
 **company_id** | **str**| Return only invoices matching this &#x60;&#x60;&#x60;companyId&#x60;&#x60;&#x60; value | [optional] 

### Return type

[**FindPartnerInvoices200Response**](FindPartnerInvoices200Response.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Invalid companyId or productId |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_partner_invoice**
> Invoice get_partner_invoice(invoice_id)

Fetch an invoice by invoiceId

Fetch a paginated list of invoices. Default page is 0 and default size is 10. The maximum page size is 200

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.invoice import Invoice
from tl_pax8.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.pax8.com/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = tl_pax8.Configuration(
    host = "https://api.pax8.com/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

configuration.access_token = os.environ["ACCESS_TOKEN"]

# Enter a context with an instance of the API client
with tl_pax8.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = tl_pax8.InvoicesApi(api_client)
    invoice_id = '57328a3c-6e95-493c-ad2f-e33b896378c7' # str | The invoice id

    try:
        # Fetch an invoice by invoiceId
        api_response = api_instance.get_partner_invoice(invoice_id)
        print("The response of InvoicesApi->get_partner_invoice:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InvoicesApi->get_partner_invoice: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **invoice_id** | **str**| The invoice id | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

