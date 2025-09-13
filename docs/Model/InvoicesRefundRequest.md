# # InvoicesRefundRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the pull payment (Default: &#39;Refund&#39; followed by the invoice id) | [optional]
**description** | **string** | Description of the pull payment | [optional]
**payout_method_id** | **string** | Payout method IDs. Available payment method IDs for Bitcoin are:   - &#x60;\&quot;BTC-CHAIN\&quot;&#x60;: Onchain    -&#x60;\&quot;BTC-LN\&quot;&#x60;: Lightning | [optional]
**refund_variant** | **string** | * &#x60;RateThen&#x60;: Refund the crypto currency price, at the rate the invoice got paid.  * &#x60;CurrentRate&#x60;: Refund the crypto currency price, at the current rate.  *&#x60;Fiat&#x60;: Refund the invoice currency, at the rate when the refund will be sent.  *&#x60;OverpaidAmount&#x60;: Refund the crypto currency amount that was overpaid.  *&#x60;Custom&#x60;: Specify the amount, currency, and rate of the refund. (see &#x60;customAmount&#x60; and &#x60;customCurrency&#x60;) | [optional]
**subtract_percentage** | **float** | Optional percentage by which to reduce the refund, e.g. as processing charge or to compensate for the mining fee. | [optional]
**custom_amount** | **float** | The amount to refund if the &#x60;refundVariant&#x60; is &#x60;Custom&#x60;. | [optional]
**custom_currency** | **string** | The currency to refund if the &#x60;refundVariant&#x60; is &#x60;Custom&#x60; | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
