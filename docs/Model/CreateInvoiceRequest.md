# # CreateInvoiceRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metadata** | [**\OpenAPI\Client\Model\InvoiceMetadata**](InvoiceMetadata.md) |  | [optional]
**checkout** | [**\OpenAPI\Client\Model\CheckoutOptions**](CheckoutOptions.md) | Additional settings to customize the checkout flow | [optional]
**receipt** | [**\OpenAPI\Client\Model\ReceiptOptions**](ReceiptOptions.md) | Additional settings to customize the public receipt | [optional]
**amount** | **float** | The amount of the invoice. If null or unspecified, the invoice will be a top-up invoice. (ie. The invoice will consider any payment as a full payment) | [optional]
**currency** | **string** | The currency of the invoice (if null, empty or unspecified, the currency will be the store&#39;s settings default)&#39; | [optional]
**additional_search_terms** | **string[]** | Additional search term to help you find this invoice via text search | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
