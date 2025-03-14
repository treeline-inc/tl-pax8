# tl_pax8.SubscriptionsApi

All URIs are relative to *https://api.pax8.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**find_subscription_by_subscription_id**](SubscriptionsApi.md#find_subscription_by_subscription_id) | **GET** /subscriptions/{subscriptionId} | Fetch a subscription by subscriptionId
[**find_subscription_history_by_subscription_id**](SubscriptionsApi.md#find_subscription_history_by_subscription_id) | **GET** /subscriptions/{subscriptionId}/history | Fetch the history of a subscription
[**find_subscriptions**](SubscriptionsApi.md#find_subscriptions) | **GET** /subscriptions | Fetch a paginated list of subscriptions
[**subscriptions_subscription_id_delete**](SubscriptionsApi.md#subscriptions_subscription_id_delete) | **DELETE** /subscriptions/{subscriptionId} | Cancel a subscription
[**update_subscription**](SubscriptionsApi.md#update_subscription) | **PUT** /subscriptions/{subscriptionId} | Update a specified subscription


# **find_subscription_by_subscription_id**
> Subscription find_subscription_by_subscription_id(subscription_id)

Fetch a subscription by subscriptionId

Returns the Subscription record specified by the subscriptionId

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.subscription import Subscription
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
    api_instance = tl_pax8.SubscriptionsApi(api_client)
    subscription_id = '04814f37-bef0-48b7-b388-c04a1e31f889' # str | 

    try:
        # Fetch a subscription by subscriptionId
        api_response = api_instance.find_subscription_by_subscription_id(subscription_id)
        print("The response of SubscriptionsApi->find_subscription_by_subscription_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->find_subscription_by_subscription_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subscription_id** | **str**|  | 

### Return type

[**Subscription**](Subscription.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Subscription not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **find_subscription_history_by_subscription_id**
> FindSubscriptionHistoryBySubscriptionId200Response find_subscription_history_by_subscription_id(subscription_id)

Fetch the history of a subscription

Returns a list of changes for a subscription

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.find_subscription_history_by_subscription_id200_response import FindSubscriptionHistoryBySubscriptionId200Response
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
    api_instance = tl_pax8.SubscriptionsApi(api_client)
    subscription_id = '04814f37-bef0-48b7-b388-c04a1e31f889' # str | 

    try:
        # Fetch the history of a subscription
        api_response = api_instance.find_subscription_history_by_subscription_id(subscription_id)
        print("The response of SubscriptionsApi->find_subscription_history_by_subscription_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->find_subscription_history_by_subscription_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subscription_id** | **str**|  | 

### Return type

[**FindSubscriptionHistoryBySubscriptionId200Response**](FindSubscriptionHistoryBySubscriptionId200Response.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | successful operation |  -  |
**404** | Subscription not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **find_subscriptions**
> FindSubscriptions200Response find_subscriptions(page=page, size=size, sort=sort, status=status, billing_term=billing_term, company_id=company_id, product_id=product_id)

Fetch a paginated list of subscriptions

Fetch a paginated list of subscriptions. Default page is 0 and default size is 10. The maximum page size is 200

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.find_subscriptions200_response import FindSubscriptions200Response
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
    api_instance = tl_pax8.SubscriptionsApi(api_client)
    page = 0 # float | The page number to request in the subscriptions list (optional) (default to 0)
    size = 10 # float | Returns _this_ number of subscriptions per page (optional) (default to 10)
    sort = 'sort_example' # str | Return subscriptions sorted by this field and direction Formatted as fieldName,direction - ex. sort=createdDate,desc (optional)
    status = 'status_example' # str | Return only subscriptions matching this ```status``` value (optional)
    billing_term = 'billing_term_example' # str | Return only subscriptions matching this ```billingTerm``` value (optional)
    company_id = 'f7fc273a-8d86-45c9-a26f-ffd42416adda' # str | Return only subscriptions matching this ```companyId``` value (optional)
    product_id = '0aaaee3f-262c-47a4-b0e6-f9ce8b54fcd7' # str | Return only subscriptions matching this ```productId``` value (optional)

    try:
        # Fetch a paginated list of subscriptions
        api_response = api_instance.find_subscriptions(page=page, size=size, sort=sort, status=status, billing_term=billing_term, company_id=company_id, product_id=product_id)
        print("The response of SubscriptionsApi->find_subscriptions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->find_subscriptions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float**| The page number to request in the subscriptions list | [optional] [default to 0]
 **size** | **float**| Returns _this_ number of subscriptions per page | [optional] [default to 10]
 **sort** | **str**| Return subscriptions sorted by this field and direction Formatted as fieldName,direction - ex. sort&#x3D;createdDate,desc | [optional] 
 **status** | **str**| Return only subscriptions matching this &#x60;&#x60;&#x60;status&#x60;&#x60;&#x60; value | [optional] 
 **billing_term** | **str**| Return only subscriptions matching this &#x60;&#x60;&#x60;billingTerm&#x60;&#x60;&#x60; value | [optional] 
 **company_id** | **str**| Return only subscriptions matching this &#x60;&#x60;&#x60;companyId&#x60;&#x60;&#x60; value | [optional] 
 **product_id** | **str**| Return only subscriptions matching this &#x60;&#x60;&#x60;productId&#x60;&#x60;&#x60; value | [optional] 

### Return type

[**FindSubscriptions200Response**](FindSubscriptions200Response.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**403** | Invalid companyId |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **subscriptions_subscription_id_delete**
> subscriptions_subscription_id_delete(subscription_id, cancel_date=cancel_date)

Cancel a subscription

Cancels the Subscription specified by subscriptionId

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
    api_instance = tl_pax8.SubscriptionsApi(api_client)
    subscription_id = '04814f37-bef0-48b7-b388-c04a1e31f889' # str | subscription to be updated
    cancel_date = '2000-10-31T01:30-05:00' # datetime | The date to cancel the subscription on (optional)

    try:
        # Cancel a subscription
        api_instance.subscriptions_subscription_id_delete(subscription_id, cancel_date=cancel_date)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->subscriptions_subscription_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subscription_id** | **str**| subscription to be updated | 
 **cancel_date** | **datetime**| The date to cancel the subscription on | [optional] 

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
**404** | Subscription not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_subscription**
> Subscription update_subscription(subscription_id, subscription=subscription)

Update a specified subscription

Updates a subscription. Currently NOT supported for subscriptions with a future date.

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.subscription import Subscription
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
    api_instance = tl_pax8.SubscriptionsApi(api_client)
    subscription_id = '04814f37-bef0-48b7-b388-c04a1e31f889' # str | subscription to be updated
    subscription = tl_pax8.Subscription() # Subscription | Updated Subscription (optional)

    try:
        # Update a specified subscription
        api_response = api_instance.update_subscription(subscription_id, subscription=subscription)
        print("The response of SubscriptionsApi->update_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->update_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subscription_id** | **str**| subscription to be updated | 
 **subscription** | [**Subscription**](Subscription.md)| Updated Subscription | [optional] 

### Return type

[**Subscription**](Subscription.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Subscription not found |  -  |
**422** | Invalid Subscription Update |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

