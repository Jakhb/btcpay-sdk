# # WebhookDataUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | Whether this webhook is enabled or not | [optional] [default to true]
**automatic_redelivery** | **bool** | If true, BTCPay Server will retry to redeliver any failed delivery after 10 seconds, 1 minutes and up to 6 times after 10 minutes. | [optional] [default to true]
**url** | **string** | The endpoint where BTCPay Server will make the POST request with the webhook body | [optional]
**authorized_events** | [**\OpenAPI\Client\Model\WebhookDataBaseAuthorizedEvents**](WebhookDataBaseAuthorizedEvents.md) |  | [optional]
**secret** | **string** | Must be used by the callback receiver to ensure the delivery comes from BTCPay Server. BTCPay Server includes the &#x60;BTCPay-Sig&#x60; HTTP header, whose format is &#x60;sha256&#x3D;HMAC256(UTF8(webhook&#39;s secret), body)&#x60;. The pattern to authenticate the webhook is similar to [how to secure webhooks in Github](https://docs.github.com/webhooks/securing/). If left out, null, or empty, the secret will not be changed. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
