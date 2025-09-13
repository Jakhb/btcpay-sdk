# # PullPaymentsLinkBoltcardRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uid** | **string** | The &#x60;UID&#x60; of the NTag424 |
**on_existing** | **string** | What to do if the boltcard is already linked.  * &#x60;KeepVersion&#x60; will return the keys (K0-K4) that are already registered.  * &#x60;UpdateVersion&#x60; will increment the version of the key, and thus return different keys (K0-K4). (See [Deterministic Boltcard Key Generation](https://github.com/boltcard/boltcard/blob/main/docs/DETERMINISTIC.md)) | [optional] [default to 'UpdateVersion']

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
