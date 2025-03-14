# SubscriptionCommitment


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique identifier for the commitment record | [optional] 
**term** | **str** | Duration of the commitment | [optional] 
**end_date** | **datetime** |  | [optional] 

## Example

```python
from tl_pax8.models.subscription_commitment import SubscriptionCommitment

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionCommitment from a JSON string
subscription_commitment_instance = SubscriptionCommitment.from_json(json)
# print the JSON string representation of the object
print(SubscriptionCommitment.to_json())

# convert the object into a dict
subscription_commitment_dict = subscription_commitment_instance.to_dict()
# create an instance of SubscriptionCommitment from a dict
subscription_commitment_from_dict = SubscriptionCommitment.from_dict(subscription_commitment_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


