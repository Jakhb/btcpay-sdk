# # PaymentMethodCriteriaData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment_method_id** | **string** | Payment method IDs. Available payment method IDs for Bitcoin are:   - &#x60;\&quot;BTC-CHAIN\&quot;&#x60;: Onchain    -&#x60;\&quot;BTC-LN\&quot;&#x60;: Lightning    - &#x60;\&quot;BTC-LNURL\&quot;&#x60;: LNURL | [optional]
**currency_code** | **string** | The currency | [optional] [default to 'USD']
**amount** | **float** | The amount | [optional]
**above** | **bool** | If the criterion is for above or below the amount | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
