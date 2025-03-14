# Page


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**size** | **float** | The size of the page | [optional] [default to 10]
**total_elements** | **object** | The total number of elements able to be paged over | [optional] 
**total_pages** | **object** | The total number of pages based on the &#x60;&#x60;&#x60;size&#x60;&#x60;&#x60; and &#x60;&#x60;&#x60;totalElements&#x60;&#x60;&#x60; | [optional] 
**number** | **object** | The current page | [optional] 

## Example

```python
from tl_pax8.models.page import Page

# TODO update the JSON string below
json = "{}"
# create an instance of Page from a JSON string
page_instance = Page.from_json(json)
# print the JSON string representation of the object
print(Page.to_json())

# convert the object into a dict
page_dict = page_instance.to_dict()
# create an instance of Page from a dict
page_from_dict = Page.from_dict(page_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


