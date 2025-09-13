# # InvoiceMetadata

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**buyer_name** | **string** | Visible in the invoice details view and in the BitPay API-compatible endpoints. | [optional]
**buyer_email** | **string** | Visible in the invoice details view and in the BitPay API-compatible endpoints. | [optional]
**buyer_country** | **string** | Visible in the invoice details view and in the BitPay API-compatible endpoints. | [optional]
**buyer_zip** | **string** | Visible in the invoice details view and in the BitPay API-compatible endpoints. | [optional]
**buyer_state** | **string** | Visible in the invoice details view and in the BitPay API-compatible endpoints. | [optional]
**buyer_city** | **string** | Visible in the invoice details view and in the BitPay API-compatible endpoints. | [optional]
**buyer_address1** | **string** | Visible in the invoice details view and in the BitPay API-compatible endpoints. | [optional]
**buyer_address2** | **string** | Visible in the invoice details view and in the BitPay API-compatible endpoints. | [optional]
**buyer_phone** | **string** | Visible in the invoice details view and in the BitPay API-compatible endpoints. | [optional]
**item_desc** | **string** | When using the Point of Sale (except in keypad or cart view), this field is set to the item description of the purchased item. This information is included in the CSV invoice export feature and appears in the invoice details view. | [optional]
**item_code** | **string** | When using the Point of Sale (except in keypad or cart view), this field is set to the item code of the purchased item. This information is included in the CSV invoice export feature and appears in the invoice details view. | [optional]
**order_id** | **string** | Refers to the order ID from an external system, such as an e-commerce platform like WooCommerce. This property is indexed, allowing for efficient invoice searches using the &#x60;orderId&#x60;. | [optional]
**order_url** | **string** | Refers to a URL linking back to the order page of the external system. This link is displayed in the invoice details view. | [optional]
**tax_included** | **float** | Represents the tax amount in the invoice currency. This information will appear in the invoice details view. During invoice creation, the value is automatically rounded to significant digits and ensured not to be greater than the invoice&#39;s price. | [optional]
**physical** | **string** | Indicates if this is a physical good; displayed in the invoice details view and in the BitPay API-compatible endpoints. | [optional]
**payment_request_id** | **string** | In the invoice details view, a link is provided for navigating to the payment request page associated with the invoice. | [optional]
**pos_data** | **object** | A custom JSON object that represents information displayed in the invoice details view. | [optional]
**receipt_data** | **object** | A custom JSON object that represents information displayed on the receipt page of an invoice. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
