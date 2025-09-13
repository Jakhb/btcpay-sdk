# # GenerateOnChainWalletRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label** | **string** | A label that will be shown in the UI | [optional]
**existing_mnemonic** | **string** | A BIP39 mnemonic | [optional]
**passphrase** | **string** | A passphrase for the BIP39 mnemonic seed | [optional]
**account_number** | **float** | The account to derive from the BIP39 mnemonic seed | [optional] [default to 0]
**save_private_keys** | **bool** | Whether to store the seed inside BTCPay Server to enable some additional services. IF &#x60;false&#x60; AND &#x60;existingMnemonic&#x60; IS NOT SPECIFIED, BE SURE TO SECURELY STORE THE SEED IN THE RESPONSE! | [optional] [default to false]
**import_keys_to_rpc** | **bool** | Whether to import all addresses generated via BTCPay Server into the underlying node wallet. (Private keys will also be imported if &#x60;savePrivateKeys&#x60; is set to true. | [optional] [default to false]
**word_list** | **string** | If &#x60;existingMnemonic&#x60; is not set, a mnemonic is generated using the specified wordList. | [optional] [default to 'English']
**word_count** | **float** | If &#x60;existingMnemonic&#x60; is not set, a mnemonic is generated using the specified wordCount. | [optional] [default to self::WORD_COUNT_NUMBER_12]
**script_pub_key_type** | **string** | the type of wallet to generate | [optional] [default to 'Segwit']

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
