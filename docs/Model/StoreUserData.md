# # StoreUserData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The id of the user | [optional]
**email** | **string** | The email of the user | [optional]
**name** | **string** | The name of the user | [optional]
**image_url** | **string** | The profile picture URL of the user | [optional]
**invitation_url** | **string** | The pending invitation URL of the user | [optional]
**email_confirmed** | **bool** | True if the email has been confirmed by the user | [optional]
**requires_email_confirmation** | **bool** | True if the email requires confirmation to log in | [optional]
**approved** | **bool** | True if an admin has approved the user | [optional]
**requires_approval** | **bool** | True if the instance requires approval to log in | [optional]
**created** | **float** | The creation date of the user as a unix timestamp. Null if created before v1.0.5.6 | [optional]
**disabled** | **bool** | True if an admin has disabled the user | [optional]
**roles** | **string[]** | The roles of the user | [optional]
**user_id** | **string** | The id of the user (Deprecated, use &#x60;id&#x60; instead) | [optional]
**role** | **string** | The role of the user. Default roles are &#x60;Owner&#x60;, &#x60;Manager&#x60;, &#x60;Employee&#x60; and &#x60;Guest&#x60; (Deprecated, use &#x60;storeRole&#x60; instead) | [optional]
**store_role** | **string** | The role of the user. Default roles are &#x60;Owner&#x60;, &#x60;Manager&#x60;, &#x60;Employee&#x60; and &#x60;Guest&#x60; | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
