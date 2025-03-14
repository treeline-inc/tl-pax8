# tl_pax8.ContactsApi

All URIs are relative to *https://api.pax8.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**companies_company_id_contacts_contact_id_delete**](ContactsApi.md#companies_company_id_contacts_contact_id_delete) | **DELETE** /companies/{companyId}/contacts/{contactId} | Delete a contact
[**companies_company_id_contacts_contact_id_get**](ContactsApi.md#companies_company_id_contacts_contact_id_get) | **GET** /companies/{companyId}/contacts/{contactId} | Fetch a contact
[**companies_company_id_contacts_contact_id_put**](ContactsApi.md#companies_company_id_contacts_contact_id_put) | **PUT** /companies/{companyId}/contacts/{contactId} | Update a contact
[**companies_company_id_contacts_get**](ContactsApi.md#companies_company_id_contacts_get) | **GET** /companies/{companyId}/contacts | Fetch a paginated list of contacts
[**companies_company_id_contacts_post**](ContactsApi.md#companies_company_id_contacts_post) | **POST** /companies/{companyId}/contacts | Create a new Contact


# **companies_company_id_contacts_contact_id_delete**
> companies_company_id_contacts_contact_id_delete(company_id, contact_id)

Delete a contact

Deletes a contact

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
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
    api_instance = tl_pax8.ContactsApi(api_client)
    company_id = 'f7fc273a-8d86-45c9-a26f-ffd42416adda' # str | 
    contact_id = '5ba26319-00e4-4a8f-986b-02a1170af269' # str | 

    try:
        # Delete a contact
        api_instance.companies_company_id_contacts_contact_id_delete(company_id, contact_id)
    except Exception as e:
        print("Exception when calling ContactsApi->companies_company_id_contacts_contact_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **company_id** | **str**|  | 
 **contact_id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful operation |  -  |
**404** | Contact or company not found |  -  |
**422** | Invalid contact delete |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **companies_company_id_contacts_contact_id_get**
> Contact companies_company_id_contacts_contact_id_get(company_id, contact_id)

Fetch a contact

Returns a contact

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.contact import Contact
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
    api_instance = tl_pax8.ContactsApi(api_client)
    company_id = 'f7fc273a-8d86-45c9-a26f-ffd42416adda' # str | 
    contact_id = '5ba26319-00e4-4a8f-986b-02a1170af269' # str | 

    try:
        # Fetch a contact
        api_response = api_instance.companies_company_id_contacts_contact_id_get(company_id, contact_id)
        print("The response of ContactsApi->companies_company_id_contacts_contact_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactsApi->companies_company_id_contacts_contact_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **company_id** | **str**|  | 
 **contact_id** | **str**|  | 

### Return type

[**Contact**](Contact.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Contact or company not found |  -  |
**422** | Invalid contact update |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **companies_company_id_contacts_contact_id_put**
> Contact companies_company_id_contacts_contact_id_put(company_id, contact_id, contact)

Update a contact

Update a contacts information

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.contact import Contact
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
    api_instance = tl_pax8.ContactsApi(api_client)
    company_id = 'f7fc273a-8d86-45c9-a26f-ffd42416adda' # str | 
    contact_id = '5ba26319-00e4-4a8f-986b-02a1170af269' # str | 
    contact = tl_pax8.Contact() # Contact | Updated contact

    try:
        # Update a contact
        api_response = api_instance.companies_company_id_contacts_contact_id_put(company_id, contact_id, contact)
        print("The response of ContactsApi->companies_company_id_contacts_contact_id_put:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactsApi->companies_company_id_contacts_contact_id_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **company_id** | **str**|  | 
 **contact_id** | **str**|  | 
 **contact** | [**Contact**](Contact.md)| Updated contact | 

### Return type

[**Contact**](Contact.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Contact or company not found |  -  |
**422** | Invalid contact update |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **companies_company_id_contacts_get**
> CompaniesCompanyIdContactsGet200Response companies_company_id_contacts_get(company_id, page=page, size=size)

Fetch a paginated list of contacts

Returns a paginated list of contacts ordered by ```createDate``` descending

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.companies_company_id_contacts_get200_response import CompaniesCompanyIdContactsGet200Response
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
    api_instance = tl_pax8.ContactsApi(api_client)
    company_id = 'f7fc273a-8d86-45c9-a26f-ffd42416adda' # str | 
    page = 0 # float | The page number to request for in the contacts list (optional) (default to 0)
    size = 10 # float | Return this number of company records per page (optional) (default to 10)

    try:
        # Fetch a paginated list of contacts
        api_response = api_instance.companies_company_id_contacts_get(company_id, page=page, size=size)
        print("The response of ContactsApi->companies_company_id_contacts_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactsApi->companies_company_id_contacts_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **company_id** | **str**|  | 
 **page** | **float**| The page number to request for in the contacts list | [optional] [default to 0]
 **size** | **float**| Return this number of company records per page | [optional] [default to 10]

### Return type

[**CompaniesCompanyIdContactsGet200Response**](CompaniesCompanyIdContactsGet200Response.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Company not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **companies_company_id_contacts_post**
> Contact companies_company_id_contacts_post(company_id, contact=contact)

Create a new Contact

Creates a new Contact

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.contact import Contact
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
    api_instance = tl_pax8.ContactsApi(api_client)
    company_id = 'f7fc273a-8d86-45c9-a26f-ffd42416adda' # str | 
    contact = tl_pax8.Contact() # Contact | Contact object (optional)

    try:
        # Create a new Contact
        api_response = api_instance.companies_company_id_contacts_post(company_id, contact=contact)
        print("The response of ContactsApi->companies_company_id_contacts_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactsApi->companies_company_id_contacts_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **company_id** | **str**|  | 
 **contact** | [**Contact**](Contact.md)| Contact object | [optional] 

### Return type

[**Contact**](Contact.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Company not found |  -  |
**422** | Invalid contact create |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

