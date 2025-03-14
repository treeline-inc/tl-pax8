# tl_pax8.ProductsApi

All URIs are relative to *https://api.pax8.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**find_all_products**](ProductsApi.md#find_all_products) | **GET** /products | Fetch a paginated list of Pax8 products
[**find_pricing_by_product_id**](ProductsApi.md#find_pricing_by_product_id) | **GET** /products/{productId}/pricing | Fetch pricing information for a particular product
[**find_product_by_product_id**](ProductsApi.md#find_product_by_product_id) | **GET** /products/{productId} | Fetch a product by its productId
[**find_product_dependencies_by_product_id**](ProductsApi.md#find_product_dependencies_by_product_id) | **GET** /products/{productId}/dependencies | Fetch a list of product dependencies for a specified product
[**find_provision_details_by_product_id**](ProductsApi.md#find_provision_details_by_product_id) | **GET** /products/{productId}/provision-details | Fetch provisioning details for a specific product


# **find_all_products**
> FindAllProducts200Response find_all_products(page=page, size=size, sort=sort, vendor_name=vendor_name)

Fetch a paginated list of Pax8 products

Returns a paginated list of Pax8 products filtered by optional query parameters

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.find_all_products200_response import FindAllProducts200Response
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
    api_instance = tl_pax8.ProductsApi(api_client)
    page = 0 # float | The page number to request for in the products list (optional) (default to 0)
    size = 10 # float | Return this number of products per page (optional) (default to 10)
    sort = 'sort_example' # str | Return products sorted by the field and direction specified. Formatted as fieldName, direction - ex. sort=name,desc (optional)
    vendor_name = 'Microsoft' # str | Return only products matching the specified vendor name (optional)

    try:
        # Fetch a paginated list of Pax8 products
        api_response = api_instance.find_all_products(page=page, size=size, sort=sort, vendor_name=vendor_name)
        print("The response of ProductsApi->find_all_products:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProductsApi->find_all_products: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float**| The page number to request for in the products list | [optional] [default to 0]
 **size** | **float**| Return this number of products per page | [optional] [default to 10]
 **sort** | **str**| Return products sorted by the field and direction specified. Formatted as fieldName, direction - ex. sort&#x3D;name,desc | [optional] 
 **vendor_name** | **str**| Return only products matching the specified vendor name | [optional] 

### Return type

[**FindAllProducts200Response**](FindAllProducts200Response.md)

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

# **find_pricing_by_product_id**
> FindPricingByProductId200Response find_pricing_by_product_id(product_id, company_id=company_id)

Fetch pricing information for a particular product

Returns recommended pricing and partner cost for the specified productId. A products pricing is dynamic data.

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.find_pricing_by_product_id200_response import FindPricingByProductId200Response
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
    api_instance = tl_pax8.ProductsApi(api_client)
    product_id = 'aaaee3f-262c-47a4-b0e6-f9ce8b54fcd7' # str | The product id
    company_id = 'f7fc273a-8d86-45c9-a26f-ffd42416adda' # str | Use the companyId in the query to see company-specific pricing (optional)

    try:
        # Fetch pricing information for a particular product
        api_response = api_instance.find_pricing_by_product_id(product_id, company_id=company_id)
        print("The response of ProductsApi->find_pricing_by_product_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProductsApi->find_pricing_by_product_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_id** | **str**| The product id | 
 **company_id** | **str**| Use the companyId in the query to see company-specific pricing | [optional] 

### Return type

[**FindPricingByProductId200Response**](FindPricingByProductId200Response.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | successful operation |  -  |
**404** | Product not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **find_product_by_product_id**
> Product find_product_by_product_id(product_id)

Fetch a product by its productId

Returns only the product record for the productId you specify

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.product import Product
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
    api_instance = tl_pax8.ProductsApi(api_client)
    product_id = 'aaaee3f-262c-47a4-b0e6-f9ce8b54fcd7' # str | 

    try:
        # Fetch a product by its productId
        api_response = api_instance.find_product_by_product_id(product_id)
        print("The response of ProductsApi->find_product_by_product_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProductsApi->find_product_by_product_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_id** | **str**|  | 

### Return type

[**Product**](Product.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Product not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **find_product_dependencies_by_product_id**
> Dependencies find_product_dependencies_by_product_id(product_id)

Fetch a list of product dependencies for a specified product

Returns associated dependencies for the specified ```productId```. A products dependencies are dynamic data.

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.dependencies import Dependencies
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
    api_instance = tl_pax8.ProductsApi(api_client)
    product_id = 'aaaee3f-262c-47a4-b0e6-f9ce8b54fcd7' # str | 

    try:
        # Fetch a list of product dependencies for a specified product
        api_response = api_instance.find_product_dependencies_by_product_id(product_id)
        print("The response of ProductsApi->find_product_dependencies_by_product_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProductsApi->find_product_dependencies_by_product_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_id** | **str**|  | 

### Return type

[**Dependencies**](Dependencies.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Product not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **find_provision_details_by_product_id**
> FindProvisionDetailsByProductId200Response find_provision_details_by_product_id(product_id)

Fetch provisioning details for a specific product

Returns provisioning details for the specified productId. Provisioning details for a product are dynamic data.

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.find_provision_details_by_product_id200_response import FindProvisionDetailsByProductId200Response
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
    api_instance = tl_pax8.ProductsApi(api_client)
    product_id = 'aaaee3f-262c-47a4-b0e6-f9ce8b54fcd7' # str | 

    try:
        # Fetch provisioning details for a specific product
        api_response = api_instance.find_provision_details_by_product_id(product_id)
        print("The response of ProductsApi->find_provision_details_by_product_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProductsApi->find_provision_details_by_product_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_id** | **str**|  | 

### Return type

[**FindProvisionDetailsByProductId200Response**](FindProvisionDetailsByProductId200Response.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Product not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

