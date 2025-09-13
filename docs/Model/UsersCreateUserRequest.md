# # UsersCreateUserRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **string** | The email of the new user | [optional]
**name** | **string** | The name of the new user | [optional]
**image_url** | **string** | The profile picture URL of the new user | [optional]
**password** | **string** | The password of the new user (if no password is set, an email will be sent to the user requiring him to set the password) | [optional]
**is_administrator** | **bool** | Make this user administrator (only if you have the &#x60;unrestricted&#x60; permission of a server administrator) | [optional] [default to false]
**send_invitation_email** | **bool** | Flag to specify if an email invitation should be sent to the user | [optional] [default to true]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
