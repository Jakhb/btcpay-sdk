# # InvoicePaymentMethodDataModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment_method_id** | **string** | Payment method IDs. Available payment method IDs for Bitcoin are:   - &#x60;\&quot;BTC-CHAIN\&quot;&#x60;: Onchain    -&#x60;\&quot;BTC-LN\&quot;&#x60;: Lightning    - &#x60;\&quot;BTC-LNURL\&quot;&#x60;: LNURL | [optional]
**currency** | **string** | The currency of the payment method (e.g., \&quot;BTC\&quot; or \&quot;LTC\&quot;) | [optional]
**destination** | **string** | The destination the payment must be made to | [optional]
**payment_link** | **string** | A payment link that helps pay to the payment destination | [optional]
**rate** | **float** | The rate between this payment method&#39;s currency and the invoice currency | [optional]
**payment_method_paid** | **float** | The amount paid by this payment method | [optional]
**total_paid** | **float** | The total amount paid by all payment methods to the invoice, converted to this payment method&#39;s currency | [optional]
**due** | **float** | The total amount left to be paid, converted to this payment method&#39;s currency (will be negative if overpaid) | [optional]
**amount** | **float** | The invoice amount, converted to this payment method&#39;s currency | [optional]
**payment_method_fee** | **float** | The added merchant fee to pay for additional costs incurred by this payment method. | [optional]
**payments** | [**\OpenAPI\Client\Model\Payment[]**](Payment.md) | Payments made with this payment method. | [optional]
**activated** | **bool** | If the payment method is activated (when lazy payments option is enabled | [optional]
**additional_data** | [**\OpenAPI\Client\Model\InvoicePaymentMethodDataModelAdditionalData**](InvoicePaymentMethodDataModelAdditionalData.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
