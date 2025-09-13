# # OnChainAutomatedTransferSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payout_method_id** | **string** | Payout method IDs. Available payment method IDs for Bitcoin are:   - &#x60;\&quot;BTC-CHAIN\&quot;&#x60;: Onchain    -&#x60;\&quot;BTC-LN\&quot;&#x60;: Lightning | [optional]
**fee_target_block** | **float** | How many blocks should the fee rate calculation target to confirm in. | [optional]
**interval_seconds** | **mixed** | How often should the processor run | [optional]
**threshold** | **float** | Only process payouts when this payout sum is reached. | [optional]
**process_new_payouts_instantly** | **bool** | Skip the interval when ane eligible payout has been approved (or created with pre-approval) | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
