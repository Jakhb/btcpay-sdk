# # CreateLightningInvoiceRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **string** | Amount wrapped in a string, represented in a millistatoshi string. (1000 millisatoshi &#x3D; 1 satoshi) | [optional]
**description** | **string** | Description of the invoice in the BOLT11 | [optional]
**description_hash_only** | **bool** | If &#x60;descriptionHashOnly&#x60; is &#x60;true&#x60; (default is &#x60;false&#x60;), then the BOLT11 returned contains a hash of the &#x60;description&#x60;, rather than the &#x60;description&#x60;, itself. This allows for much longer descriptions, but they must be communicated via some other mechanism. | [optional] [default to false]
**expiry** | **mixed** | Expiration time in seconds | [optional]
**private_route_hints** | **bool** | True if the invoice should include private route hints | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
