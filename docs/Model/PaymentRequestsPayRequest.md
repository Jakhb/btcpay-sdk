# # PaymentRequestsPayRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **float** | The amount of the invoice. If &#x60;null&#x60; or &#x60;unspecified&#x60;, it will be set to the payment request&#39;s due amount. Note that the payment&#39;s request &#x60;allowCustomPaymentAmounts&#x60; must be &#x60;true&#x60;, or a 422 error will be sent back.&#39; | [optional]
**allow_pending_invoice_reuse** | **bool** | If &#x60;true&#x60;, this endpoint will not necessarily create a new invoice, and instead attempt to give back a pending one for this payment request. | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
