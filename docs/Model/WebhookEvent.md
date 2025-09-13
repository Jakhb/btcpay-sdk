# # WebhookEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**delivery_id** | **string** | The delivery id of the webhook | [optional]
**webhook_id** | **string** | The id of the webhook | [optional]
**original_delivery_id** | **string** | If this delivery is a redelivery, the is the delivery id of the original delivery. | [optional]
**is_redelivery** | **bool** | True if this delivery is a redelivery | [optional]
**type** | **string** | The type of this event, current available are &#x60;InvoiceCreated&#x60;, &#x60;InvoiceReceivedPayment&#x60;, &#x60;InvoiceProcessing&#x60;, &#x60;InvoiceExpired&#x60;, &#x60;InvoiceSettled&#x60;, &#x60;InvoiceInvalid&#x60;, and &#x60;InvoicePaymentSettled&#x60;. | [optional]
**timestamp** | **float** | The timestamp when this delivery has been created | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
