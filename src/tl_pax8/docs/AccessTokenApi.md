# tl_pax8.AccessTokenApi

All URIs are relative to *https://api.pax8.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_access_token**](AccessTokenApi.md#create_access_token) | **POST** /token | Create a new Access Token


# **create_access_token**
> TokenResponse create_access_token(token_request=token_request)

Create a new Access Token

Create a new Access Token. Use the code examples to create an Access token on your local machine. Then copy the `access_token` into the Authorization header of any endpoint in the documentation to start making calls. The audience should be set to `https://api.pax8.com` for the partner endpoints.

### Example

* OAuth Authentication (OAuth2):

```python
import tl_pax8
from tl_pax8.models.token_request import TokenRequest
from tl_pax8.models.token_response import TokenResponse
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
    api_instance = tl_pax8.AccessTokenApi(api_client)
    token_request = tl_pax8.TokenRequest() # TokenRequest | Token Request (optional)

    try:
        # Create a new Access Token
        api_response = api_instance.create_access_token(token_request=token_request)
        print("The response of AccessTokenApi->create_access_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccessTokenApi->create_access_token: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token_request** | [**TokenRequest**](TokenRequest.md)| Token Request | [optional] 

### Return type

[**TokenResponse**](TokenResponse.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | successful operation |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

