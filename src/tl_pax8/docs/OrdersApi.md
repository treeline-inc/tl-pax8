# tl_pax8.OrdersApi

All URIs are relative to *https://api.pax8.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_order**](OrdersApi.md#create_order) | **POST** /orders | Create a new order for a specified company
[**find_orders**](OrdersApi.md#find_orders) | **GET** /orders | Fetch a paginated list of orders associated with your partner
[**find_orders_by_order_id**](OrdersApi.md#find_orders_by_order_id) | **GET** /orders/{orderId} | Fetch order details by orderId


# **create_order**
> Order create_order(is_mock=is_mock, create_order=create_order)

Create a new order for a specified company

Create a new order. Currently NOT supported for scheduled orders(orders with a future date).

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.create_order import CreateOrder
from tl_pax8.models.order import Order
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
    api_instance = tl_pax8.OrdersApi(api_client)
    is_mock = True # bool | Perform validations only. Skip any interactions with the database. (optional)
    create_order = tl_pax8.CreateOrder() # CreateOrder | Order object (optional)

    try:
        # Create a new order for a specified company
        api_response = api_instance.create_order(is_mock=is_mock, create_order=create_order)
        print("The response of OrdersApi->create_order:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrdersApi->create_order: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **is_mock** | **bool**| Perform validations only. Skip any interactions with the database. | [optional] 
 **create_order** | [**CreateOrder**](CreateOrder.md)| Order object | [optional] 

### Return type

[**Order**](Order.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**422** | Invalid order |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **find_orders**
> FindOrders200Response find_orders(page=page, size=size, company_id=company_id)

Fetch a paginated list of orders associated with your partner

Returns a paginated list of orders. Currently NOT supported for scheduled orders(orders with a future date).

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.find_orders200_response import FindOrders200Response
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
    api_instance = tl_pax8.OrdersApi(api_client)
    page = 0 # float | The page number to request for in the orders list (optional) (default to 0)
    size = 10 # float |  (optional) (default to 10)
    company_id = 'f7fc273a-8d86-45c9-a26f-ffd42416adda' # str | The company id to filter on (optional)

    try:
        # Fetch a paginated list of orders associated with your partner
        api_response = api_instance.find_orders(page=page, size=size, company_id=company_id)
        print("The response of OrdersApi->find_orders:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrdersApi->find_orders: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float**| The page number to request for in the orders list | [optional] [default to 0]
 **size** | **float**|  | [optional] [default to 10]
 **company_id** | **str**| The company id to filter on | [optional] 

### Return type

[**FindOrders200Response**](FindOrders200Response.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Order not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **find_orders_by_order_id**
> Order find_orders_by_order_id(order_id)

Fetch order details by orderId

Returns the Order record specified by OrderId. Currently NOT supported for scheduled orders

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.order import Order
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
    api_instance = tl_pax8.OrdersApi(api_client)
    order_id = '8f72220b-2a13-4856-a647-b80448722bbb' # str | The unique identifier for an order record

    try:
        # Fetch order details by orderId
        api_response = api_instance.find_orders_by_order_id(order_id)
        print("The response of OrdersApi->find_orders_by_order_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrdersApi->find_orders_by_order_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **str**| The unique identifier for an order record | 

### Return type

[**Order**](Order.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Invalid order id |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

