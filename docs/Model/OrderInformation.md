# # OrderInformation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**order_id** | **string** | Refers to the order ID from an external system, such as an e-commerce platform like WooCommerce. This property is indexed, allowing for efficient invoice searches using the &#x60;orderId&#x60;. | [optional]
**order_url** | **string** | Refers to a URL linking back to the order page of the external system. This link is displayed in the invoice details view. | [optional]
**tax_included** | **float** | Represents the tax amount in the invoice currency. This information will appear in the invoice details view. During invoice creation, the value is automatically rounded to significant digits and ensured not to be greater than the invoice&#39;s price. | [optional]
**physical** | **string** | Indicates if this is a physical good; displayed in the invoice details view and in the BitPay API-compatible endpoints. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
