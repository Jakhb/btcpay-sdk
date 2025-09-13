# # CheckoutOptions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**speed_policy** | [**\OpenAPI\Client\Model\SpeedPolicy**](SpeedPolicy.md) |  | [optional]
**payment_methods** | **string[]** | A specific set of payment methods to use for this invoice (ie. BTC, BTC-LightningNetwork). By default, select all payment methods enabled in the store. | [optional]
**default_payment_method** | **string** | Default payment type for the invoice (e.g., BTC, BTC-LightningNetwork). Default payment method set for the store is used if this parameter is not specified. | [optional]
**lazy_payment_methods** | **bool** | If true, payment methods are enabled individually upon user interaction in the invoice. Default to store&#39;s settings&#39; | [optional]
**expiration_minutes** | **mixed** | The number of minutes after which an invoice becomes expired. Defaults to the store&#39;s settings. (The default store settings is 15) | [optional]
**monitoring_minutes** | **mixed** | The number of minutes after an invoice expired after which we are still monitoring for incoming payments. Defaults to the store&#39;s settings. (The default store settings is 1440, 1 day) | [optional]
**payment_tolerance** | **float** | A percentage determining whether to count the invoice as paid when the invoice is paid within the specified margin of error. Defaults to the store&#39;s settings. (The default store settings is 0) | [optional] [default to 0.0]
**redirect_url** | **string** | When the customer has paid the invoice, the URL where the customer will be redirected when clicking on the &#x60;return to store&#x60; button. You can use placeholders &#x60;{InvoiceId}&#x60; or &#x60;{OrderId}&#x60; in the URL, BTCPay Server will replace those with this invoice &#x60;id&#x60; or &#x60;metadata.orderId&#x60; respectively. | [optional]
**redirect_automatically** | **bool** | When the customer has paid the invoice, and a &#x60;redirectURL&#x60; is set, the checkout is redirected to &#x60;redirectURL&#x60; automatically if &#x60;redirectAutomatically&#x60; is true. Defaults to the store&#39;s settings. (The default store settings is false) | [optional]
**default_language** | **string** | The language code (eg. en-US, en, fr-FR...) of the language presented to your customer in the checkout page. BTCPay Server tries to match the best language available. If null or not set, will fallback on the store&#39;s default language. You can see the list of language codes with [this operation](#operation/langCodes). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
