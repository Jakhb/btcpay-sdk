# # PullPaymentData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Id of the pull payment | [optional]
**name** | **string** | Name given to pull payment when it was created | [optional]
**description** | **string** | Description given to pull payment when it was created | [optional]
**currency** | **string** | The currency of the pull payment&#39;s amount | [optional]
**amount** | **float** | The amount in the currency of this pull payment as a decimal string | [optional]
**bolt11_expiration** | **string** | If lightning is activated, do not accept BOLT11 invoices with expiration less than … days | [optional]
**auto_approve_claims** | **bool** | Any payouts created for this pull payment will skip the approval phase upon creation | [optional] [default to false]
**archived** | **bool** | Whether this pull payment is archived | [optional]
**view_link** | **string** | The link to a page to claim payouts to this pull payment | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
