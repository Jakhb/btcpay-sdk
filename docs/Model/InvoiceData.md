# # InvoiceData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metadata** | [**\OpenAPI\Client\Model\InvoiceMetadata**](InvoiceMetadata.md) |  | [optional]
**checkout** | [**\OpenAPI\Client\Model\CheckoutOptions**](CheckoutOptions.md) | Additional settings to customize the checkout flow | [optional]
**receipt** | [**\OpenAPI\Client\Model\ReceiptOptions**](ReceiptOptions.md) | Additional settings to customize the public receipt | [optional]
**id** | **string** | The identifier of the invoice | [optional]
**store_id** | **string** | The store identifier that the invoice belongs to | [optional]
**amount** | **float** | The amount of the invoice. Note that the amount will be zero for a top-up invoice that is paid after invoice expiry. | [optional]
**paid_amount** | **float** | The actual amount paid by the customer/buyer. | [optional]
**currency** | **string** | The currency of the invoice | [optional]
**type** | [**\OpenAPI\Client\Model\InvoiceType**](InvoiceType.md) |  | [optional]
**checkout_link** | **string** | The link to the checkout page, where you can redirect the customer | [optional]
**created_time** | **float** | The creation time of the invoice | [optional]
**expiration_time** | **float** | The expiration time of the invoice | [optional]
**monitoring_expiration** | **float** | Expiration time for monitoring of the invoice for any changes | [optional]
**status** | [**\OpenAPI\Client\Model\InvoiceStatus**](InvoiceStatus.md) |  | [optional]
**additional_status** | [**\OpenAPI\Client\Model\InvoiceAdditionalStatus**](InvoiceAdditionalStatus.md) |  | [optional]
**available_statuses_for_manual_marking** | [**\OpenAPI\Client\Model\InvoiceStatus[]**](InvoiceStatus.md) | The statuses the invoice can be manually marked as | [optional]
**archived** | **bool** | true if the invoice is archived | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
