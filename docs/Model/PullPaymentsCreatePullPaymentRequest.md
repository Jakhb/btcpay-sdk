# # PullPaymentsCreatePullPaymentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The name of the pull payment | [optional]
**description** | **string** | The description of the pull payment | [optional]
**amount** | **float** | The amount in &#x60;currency&#x60; of this pull payment as a decimal string | [optional]
**currency** | **string** | The currency of the amount. | [optional]
**bolt11_expiration** | **string** | If lightning is activated, do not accept BOLT11 invoices with expiration less than … days | [optional] [default to '30']
**auto_approve_claims** | **bool** | Any payouts created for this pull payment will skip the approval phase upon creation | [optional] [default to false]
**starts_at** | **int** | When this pull payment is effective. Already started if null or unspecified. | [optional]
**expires_at** | **int** | When this pull payment expires. Never expires if null or unspecified. | [optional]
**payout_methods** | **string[]** | The list of supported payout methods supported by this pull payment. Available options can be queried from the &#x60;StorePaymentMethods_GetStorePaymentMethods&#x60; endpoint. If &#x60;null&#x60;, all available payout methods will be supported. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
