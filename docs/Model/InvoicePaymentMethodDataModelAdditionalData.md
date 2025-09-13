# # InvoicePaymentMethodDataModelAdditionalData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key_path** | **string** | The key path relative to the account derviation key. | [optional]
**payjoin_enabled** | **bool** | If the payjoin feature is enabled for this payment method. | [optional]
**account_derivation** | **string** | The derivation scheme used to derive addresses (null if &#x60;includeSensitive&#x60; is &#x60;false&#x60;) | [optional]
**recommended_fee_rate** | **float** | The recommended fee rate for this payment method. | [optional]
**payment_method_fee_rate** | **float** | The fee rate charged to the user as &#x60;PaymentMethodFee&#x60;. | [optional]
**provided_comment** | **string** | The provided comment to a LNUrl payment with comments enabled | [optional]
**consumed_lightning_address** | **string** | The consumed lightning address of a LN Address payment | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
