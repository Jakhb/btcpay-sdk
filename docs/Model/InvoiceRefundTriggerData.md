# # InvoiceRefundTriggerData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment_amount_then** | **float** | The amount in crypto at the time the invoice was paid. | [optional]
**payment_amount_now** | **float** | The current amount in crypto. | [optional]
**invoice_amount** | **float** | The fiat amount at the rate when the refund will be sent. | [optional]
**payment_currency** | **string** | The crypto currency of the invoice | [optional]
**payment_currency_divisibility** | **float** | The maximum divisibility supported by the crypto currency of the invoice | [optional]
**invoice_currency_divisibility** | **float** | The maximum divisibility supported by the fiat currency of the invoice | [optional]
**invoice_currency** | **string** | The fiat currency of the invoice | [optional]
**overpaid_payment_amount** | **float** | The amount by which the invoice is overpaid | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
