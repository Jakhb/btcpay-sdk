# # LightningPaymentData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The payment&#39;s ID | [optional]
**status** | [**\OpenAPI\Client\Model\LightningPaymentStatus**](LightningPaymentStatus.md) |  | [optional]
**bolt11** | **string** | The BOLT11 representation of the payment | [optional]
**payment_hash** | **string** | The payment hash | [optional]
**preimage** | **string** | The payment preimage (available when status is complete) | [optional]
**created_at** | **float** | The unix timestamp when the payment got created | [optional]
**total_amount** | **string** | The total amount (including fees) in millisatoshi | [optional]
**fee_amount** | **string** | The total fees in millisatoshi | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
