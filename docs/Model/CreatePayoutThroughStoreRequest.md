# # CreatePayoutThroughStoreRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**destination** | **string** | The destination of the payout (can be an address or a BIP21 url) | [optional]
**amount** | **float** | The amount of the payout in the currency of the pull payment (eg. USD). | [optional]
**payout_method_id** | **string** | Payout method IDs. Available payment method IDs for Bitcoin are:   - &#x60;\&quot;BTC-CHAIN\&quot;&#x60;: Onchain    -&#x60;\&quot;BTC-LN\&quot;&#x60;: Lightning | [optional]
**pull_payment_id** | **string** | The pull payment to create this for. Optional. | [optional]
**approved** | **bool** | Whether to approve this payout automatically upon creation | [optional]
**metadata** | **object** | Additional metadata to store with the payout | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
