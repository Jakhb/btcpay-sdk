# # LightningInvoiceData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The invoice&#39;s ID | [optional]
**status** | [**\OpenAPI\Client\Model\LightningInvoiceStatus**](LightningInvoiceStatus.md) |  | [optional]
**bolt11** | **string** | The BOLT11 representation of the invoice | [optional]
**paid_at** | **float** | The unix timestamp when the invoice got paid | [optional]
**expires_at** | **float** | The unix timestamp when the invoice expires | [optional]
**amount** | **string** | The amount of the invoice in millisatoshi | [optional]
**amount_received** | **string** | The amount received in millisatoshi | [optional]
**payment_hash** | **string** | The payment hash | [optional]
**preimage** | **string** | The payment preimage (available when status is complete) | [optional]
**custom_records** | **object** | The custom TLV records attached to a keysend payment | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
