# Subscription


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] [readonly] 
**parent_subscription_id** | **str** |  | [optional] [readonly] 
**company_id** | **str** |  | [optional] [readonly] 
**product_id** | **str** |  | [optional] [readonly] 
**quantity** | **float** |  | 
**start_date** | **datetime** |  | 
**end_date** | **datetime** |  | [optional] 
**created_date** | **datetime** |  | [optional] [readonly] 
**updated_date** | **datetime** |  | [optional] [readonly] 
**billing_start** | **date** |  | [optional] [readonly] 
**status** | **str** | Subscription Status :  * &#x60;Active&#x60; - Provisioning request complete  * &#x60;Cancelled&#x60; - Deprovisioning request complete  * &#x60;PendingManual&#x60; -  An associated manual provisioning task isn&#39;t started/completed  * &#x60;PendingAutomated&#x60; - An associated automated provisioning task isn&#39;t started/completed  * &#x60;PendingCancel&#x60; - Deprovisioning request pending  * &#x60;WaitingForDetails&#x60; - Provisioning details are missing  * &#x60;Trial&#x60; - Trial subscriptions offer free or discounted access for a limited time.  * &#x60;Converted&#x60; - Converted from trial  * &#x60;PendingActivation&#x60; - Requires Activation but has not yet been activated  * &#x60;Activated&#x60; - Requires Activation and has been activated  Activation is required for a small subset of products.  Billing services do not begin for these products until \&quot;activation\&quot; is complete.  | [optional] [readonly] 
**price** | **float** | The price for the customer. | [optional] 
**currency_code** | **str** | The currency ISO 4217 code | [optional] 
**partner_cost** | **float** | The price for the Partner. | [optional] 
**billing_term** | **str** |  | 
**provisioning_details** | [**List[ProvisioningDetail]**](ProvisioningDetail.md) |  | [optional] 
**commitment_term** | [**SubscriptionCommitment**](SubscriptionCommitment.md) |  | [optional] [readonly] 

## Example

```python
from tl_pax8.models.subscription import Subscription

# TODO update the JSON string below
json = "{}"
# create an instance of Subscription from a JSON string
subscription_instance = Subscription.from_json(json)
# print the JSON string representation of the object
print(Subscription.to_json())

# convert the object into a dict
subscription_dict = subscription_instance.to_dict()
# create an instance of Subscription from a dict
subscription_from_dict = Subscription.from_dict(subscription_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


