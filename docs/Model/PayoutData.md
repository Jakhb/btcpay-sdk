# # PayoutData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The id of the payout | [optional]
**revision** | **int** | The revision number of the payout. This revision number is incremented when the payout amount or destination is modified before the approval. | [optional]
**pull_payment_id** | **string** | The id of the pull payment this payout belongs to | [optional]
**date** | **string** | The creation date of the payout as a unix timestamp | [optional]
**destination** | **string** | The destination of the payout (can be an address or a BIP21 url) | [optional]
**original_currency** | **string** | The currency before being converted into the payout&#39;s currency | [optional]
**original_amount** | **float** | The amount in originalCurrency before being converted into the payout&#39;s currency | [optional]
**payout_currency** | **string** | The currency of the payout after conversion. | [optional]
**payout_amount** | **float** | The amount in payoutCurrency after conversion. (This property is set after the payout has been Approved) | [optional]
**payout_method_id** | **string** | Payout method IDs. Available payment method IDs for Bitcoin are:   - &#x60;\&quot;BTC-CHAIN\&quot;&#x60;: Onchain    -&#x60;\&quot;BTC-LN\&quot;&#x60;: Lightning | [optional]
**state** | [**\OpenAPI\Client\Model\PayoutState**](PayoutState.md) |  | [optional]
**payment_proof** | [**\OpenAPI\Client\Model\PayoutPaymentProof**](PayoutPaymentProof.md) |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\GeneralInformation**](GeneralInformation.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
