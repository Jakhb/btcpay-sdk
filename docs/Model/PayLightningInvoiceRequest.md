# # PayLightningInvoiceRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bolt11** | **string** | The BOLT11 of the invoice to pay | [optional]
**amount** | **string** | Optional explicit payment amount in millisatoshi (if specified, it overrides the BOLT11 amount) | [optional]
**max_fee_percent** | **float** | The fee limit expressed as a percentage of the payment amount | [optional]
**max_fee_flat** | **string** | The fee limit expressed as a fixed amount in satoshi | [optional]
**send_timeout** | **mixed** | The number of seconds after which the payment times out | [optional] [default to 30]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
