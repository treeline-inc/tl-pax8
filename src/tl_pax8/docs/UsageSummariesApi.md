# tl_pax8.UsageSummariesApi

All URIs are relative to *https://api.pax8.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**find_subscription_usage_summaries**](UsageSummariesApi.md#find_subscription_usage_summaries) | **GET** /subscriptions/{subscriptionId}/usage-summaries | Fetch a paginated list of usage summaries
[**find_subscription_usage_summary**](UsageSummariesApi.md#find_subscription_usage_summary) | **GET** /usage-summaries/{usageSummaryId} | Fetch a usage summary by usageSummaryId
[**find_usage_lines**](UsageSummariesApi.md#find_usage_lines) | **GET** /usage-summaries/{usageSummaryId}/usage-lines | Fetch a paginated list of usage lines for a usage summary


# **find_subscription_usage_summaries**
> FindSubscriptionUsageSummaries200Response find_subscription_usage_summaries(subscription_id, page=page, size=size, sort=sort, resource_group=resource_group, company_id=company_id)

Fetch a paginated list of usage summaries

Fetch a paginated list of usage summaries. Default page is 0 and default size is 10. The maximum page size is 200

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.find_subscription_usage_summaries200_response import FindSubscriptionUsageSummaries200Response
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
    api_instance = tl_pax8.UsageSummariesApi(api_client)
    subscription_id = '04814f37-bef0-48b7-b388-c04a1e31f889' # str | 
    page = 0 # float | The page number to request in the usage summaries list (optional) (default to 0)
    size = 10 # float | Returns _this_ number of usage summaries per page (optional) (default to 10)
    sort = 'sort_example' # str | Return usage summaries sorted by this field and direction Formatted as fieldName,direction - ex. sort=resourceGroup,desc (optional)
    resource_group = 'IronCloud Technologies' # str | Return only usage summaries matching this ```resourceGroup``` value (optional)
    company_id = 'f7fc273a-8d86-45c9-a26f-ffd42416adda' # str | Return only usage summaries with this ```companyId``` value (optional)

    try:
        # Fetch a paginated list of usage summaries
        api_response = api_instance.find_subscription_usage_summaries(subscription_id, page=page, size=size, sort=sort, resource_group=resource_group, company_id=company_id)
        print("The response of UsageSummariesApi->find_subscription_usage_summaries:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsageSummariesApi->find_subscription_usage_summaries: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subscription_id** | **str**|  | 
 **page** | **float**| The page number to request in the usage summaries list | [optional] [default to 0]
 **size** | **float**| Returns _this_ number of usage summaries per page | [optional] [default to 10]
 **sort** | **str**| Return usage summaries sorted by this field and direction Formatted as fieldName,direction - ex. sort&#x3D;resourceGroup,desc | [optional] 
 **resource_group** | **str**| Return only usage summaries matching this &#x60;&#x60;&#x60;resourceGroup&#x60;&#x60;&#x60; value | [optional] 
 **company_id** | **str**| Return only usage summaries with this &#x60;&#x60;&#x60;companyId&#x60;&#x60;&#x60; value | [optional] 

### Return type

[**FindSubscriptionUsageSummaries200Response**](FindSubscriptionUsageSummaries200Response.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Invalid subscriptionId or companyId |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **find_subscription_usage_summary**
> UsageSummary find_subscription_usage_summary(usage_summary_id)

Fetch a usage summary by usageSummaryId

Fetch a paginated list of usage summaries. Default page is 0 and default size is 10. The maximum page size is 200

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.usage_summary import UsageSummary
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
    api_instance = tl_pax8.UsageSummariesApi(api_client)
    usage_summary_id = 'f5e4cefe-09ff-46a0-b3b0-4f392cfae44c' # str | The usage summary id

    try:
        # Fetch a usage summary by usageSummaryId
        api_response = api_instance.find_subscription_usage_summary(usage_summary_id)
        print("The response of UsageSummariesApi->find_subscription_usage_summary:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsageSummariesApi->find_subscription_usage_summary: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **usage_summary_id** | **str**| The usage summary id | 

### Return type

[**UsageSummary**](UsageSummary.md)

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

# **find_usage_lines**
> FindUsageLines200Response find_usage_lines(usage_summary_id, usage_date, product_id=product_id)

Fetch a paginated list of usage lines for a usage summary

Fetch a paginated list of usage lines. Default page is 0 and default size is 10. The maximum page size is 200

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.find_usage_lines200_response import FindUsageLines200Response
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
    api_instance = tl_pax8.UsageSummariesApi(api_client)
    usage_summary_id = 'f5e4cefe-09ff-46a0-b3b0-4f392cfae44c' # str | The usage summary id
    usage_date = '2020-01-01' # str | The date usage was recorded
    product_id = '0aaaee3f-262c-47a4-b0e6-f9ce8b54fcd7' # str | Return only usage summaries with this ```productId``` value (optional)

    try:
        # Fetch a paginated list of usage lines for a usage summary
        api_response = api_instance.find_usage_lines(usage_summary_id, usage_date, product_id=product_id)
        print("The response of UsageSummariesApi->find_usage_lines:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsageSummariesApi->find_usage_lines: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **usage_summary_id** | **str**| The usage summary id | 
 **usage_date** | **str**| The date usage was recorded | 
 **product_id** | **str**| Return only usage summaries with this &#x60;&#x60;&#x60;productId&#x60;&#x60;&#x60; value | [optional] 

### Return type

[**FindUsageLines200Response**](FindUsageLines200Response.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  -  |
**404** | Invalid usage summary id |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

