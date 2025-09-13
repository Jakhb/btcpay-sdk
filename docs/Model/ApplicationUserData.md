# # ApplicationUserData

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

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
