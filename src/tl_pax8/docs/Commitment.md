# Commitment


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique identifier for the commitment record | [optional] [readonly] 
**term** | **str** | Duration of the commitment | [optional] 
**auto_renew** | **bool** | Renews without manual intervention at the end of the term | [optional] 
**renewal_window_days_before_term_end** | **float** | Number of days _before_ term end-date when renewal window opens | [optional] 
**renewal_window_days_after_term_end** | **float** | Number of days after the term end-date that renewal window closes | [optional] 
**allow_for_quantity_increase** | **bool** | Is &#x60;&#x60;&#x60;true&#x60;&#x60;&#x60; if quantity can be increased during commitment term | [optional] 
**allow_for_quantity_decrease** | **bool** | Is &#x60;&#x60;&#x60;true&#x60;&#x60;&#x60; if quantity can be decreased during commitment term | [optional] 
**allow_for_early_cancellation** | **bool** | Is &#x60;&#x60;&#x60;true&#x60;&#x60;&#x60; if commitment can be cancelled prior to end of term | [optional] 
**cancellation_fee_applied** | **bool** | Is &#x60;&#x60;&#x60;true&#x60;&#x60;&#x60; if canceling subscription entails a fee | [optional] 
**is_transferable** | **bool** | Is &#x60;&#x60;&#x60;true&#x60;&#x60;&#x60; if commitment can be transferred to another company | [optional] 

## Example

```python
from tl_pax8.models.commitment import Commitment

# TODO update the JSON string below
json = "{}"
# create an instance of Commitment from a JSON string
commitment_instance = Commitment.from_json(json)
# print the JSON string representation of the object
print(Commitment.to_json())

# convert the object into a dict
commitment_dict = commitment_instance.to_dict()
# create an instance of Commitment from a dict
commitment_from_dict = Commitment.from_dict(commitment_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


