# tl_pax8.CompaniesApi

All URIs are relative to *https://api.pax8.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**companies_company_id_get**](CompaniesApi.md#companies_company_id_get) | **GET** /companies/{companyId} | Fetch a single company record by companyId
[**create_company**](CompaniesApi.md#create_company) | **POST** /companies | Create a new Company
[**find_companies**](CompaniesApi.md#find_companies) | **GET** /companies | Fetch a paginated list of your companies
[**update_company**](CompaniesApi.md#update_company) | **PATCH** /companies/{companyId} | Update an existing Company


# **companies_company_id_get**
> Company companies_company_id_get(company_id)

Fetch a single company record by companyId

Returns a single company record matching the ```companyId``` you specify

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.company import Company
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
    api_instance = tl_pax8.CompaniesApi(api_client)
    company_id = 'f7fc273a-8d86-45c9-a26f-ffd42416adda' # str | 

    try:
        # Fetch a single company record by companyId
        api_response = api_instance.companies_company_id_get(company_id)
        print("The response of CompaniesApi->companies_company_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompaniesApi->companies_company_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **company_id** | **str**|  | 

### Return type

[**Company**](Company.md)

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

# **create_company**
> Company create_company(company=company)

Create a new Company

Creates a new Company. ATTENTION - The Company will be placed in an “inactive” status until the [Company has primary Contacts added](#tag/Contacts). Once contacts are added, the company will move to “active”.

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.company import Company
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
    api_instance = tl_pax8.CompaniesApi(api_client)
    company = tl_pax8.Company() # Company | Company object (optional)

    try:
        # Create a new Company
        api_response = api_instance.create_company(company=company)
        print("The response of CompaniesApi->create_company:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompaniesApi->create_company: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **company** | [**Company**](Company.md)| Company object | [optional] 

### Return type

[**Company**](Company.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Company create |  -  |
**422** | Invalid Company |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **find_companies**
> FindCompanies200Response find_companies(page=page, size=size, sort=sort, city=city, country=country, state_or_province=state_or_province, postal_code=postal_code, self_service_allowed=self_service_allowed, bill_on_behalf_of_enabled=bill_on_behalf_of_enabled, order_approval_required=order_approval_required, status=status)

Fetch a paginated list of your companies

Returns a paginated list of all your companies filtered by optional parameters

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.find_companies200_response import FindCompanies200Response
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
    api_instance = tl_pax8.CompaniesApi(api_client)
    page = 0 # float | The page number to request for in the companies list (optional) (default to 0)
    size = 10 # float | Return this number of company records per page (optional) (default to 10)
    sort = 'sort_example' # str | Return companies sorted by this field and direction. Formatted as fieldName,direction - ex. sort=name,desc (optional)
    city = 'Greenwood Village' # str | Return only companies matching this ```city``` value (optional)
    country = 'United States' # str | Return only companies matching this ```country``` value (optional)
    state_or_province = 'Colorado' # str | Return only companies matching this ```stateOrProvince``` value (optional)
    postal_code = '80111' # str | Return only companies matching this ```postalCode``` value (optional)
    self_service_allowed = True # bool | Return only companies matching this ```selfServiceAllowed``` value (optional)
    bill_on_behalf_of_enabled = True # bool | Return only companies matching this ```billOnBehalfOfEnabled``` value (optional)
    order_approval_required = True # bool | Return only companies matching this ```orderApprovalRequired``` value (optional)
    status = 'status_example' # str | Return only companies matching this ```status``` value (optional)

    try:
        # Fetch a paginated list of your companies
        api_response = api_instance.find_companies(page=page, size=size, sort=sort, city=city, country=country, state_or_province=state_or_province, postal_code=postal_code, self_service_allowed=self_service_allowed, bill_on_behalf_of_enabled=bill_on_behalf_of_enabled, order_approval_required=order_approval_required, status=status)
        print("The response of CompaniesApi->find_companies:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompaniesApi->find_companies: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float**| The page number to request for in the companies list | [optional] [default to 0]
 **size** | **float**| Return this number of company records per page | [optional] [default to 10]
 **sort** | **str**| Return companies sorted by this field and direction. Formatted as fieldName,direction - ex. sort&#x3D;name,desc | [optional] 
 **city** | **str**| Return only companies matching this &#x60;&#x60;&#x60;city&#x60;&#x60;&#x60; value | [optional] 
 **country** | **str**| Return only companies matching this &#x60;&#x60;&#x60;country&#x60;&#x60;&#x60; value | [optional] 
 **state_or_province** | **str**| Return only companies matching this &#x60;&#x60;&#x60;stateOrProvince&#x60;&#x60;&#x60; value | [optional] 
 **postal_code** | **str**| Return only companies matching this &#x60;&#x60;&#x60;postalCode&#x60;&#x60;&#x60; value | [optional] 
 **self_service_allowed** | **bool**| Return only companies matching this &#x60;&#x60;&#x60;selfServiceAllowed&#x60;&#x60;&#x60; value | [optional] 
 **bill_on_behalf_of_enabled** | **bool**| Return only companies matching this &#x60;&#x60;&#x60;billOnBehalfOfEnabled&#x60;&#x60;&#x60; value | [optional] 
 **order_approval_required** | **bool**| Return only companies matching this &#x60;&#x60;&#x60;orderApprovalRequired&#x60;&#x60;&#x60; value | [optional] 
 **status** | **str**| Return only companies matching this &#x60;&#x60;&#x60;status&#x60;&#x60;&#x60; value | [optional] 

### Return type

[**FindCompanies200Response**](FindCompanies200Response.md)

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

# **update_company**
> Company update_company(company_id, company_update=company_update)

Update an existing Company

Updates an existing Company. ATTENTION - at least one parameter has to be modified.

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.company import Company
from tl_pax8.models.company_update import CompanyUpdate
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
    api_instance = tl_pax8.CompaniesApi(api_client)
    company_id = 'f7fc273a-8d86-45c9-a26f-ffd42416adda' # str | 
    company_update = tl_pax8.CompanyUpdate() # CompanyUpdate | Company object (optional)

    try:
        # Update an existing Company
        api_response = api_instance.update_company(company_id, company_update=company_update)
        print("The response of CompaniesApi->update_company:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompaniesApi->update_company: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **company_id** | **str**|  | 
 **company_update** | [**CompanyUpdate**](CompanyUpdate.md)| Company object | [optional] 

### Return type

[**Company**](Company.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Company update |  -  |
**422** | Invalid Company |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

