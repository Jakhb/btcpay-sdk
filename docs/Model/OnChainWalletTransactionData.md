# # OnChainWalletTransactionData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transaction_hash** | **string** | The transaction id | [optional]
**comment** | **string** | A comment linked to the transaction | [optional]
**amount** | **float** | The amount the wallet balance changed with this transaction | [optional]
**block_hash** | **string** | The hash of the block that confirmed this transaction. Null if still unconfirmed. | [optional]
**block_height** | **string** | The height of the block that confirmed this transaction. Null if still unconfirmed. | [optional]
**confirmations** | **string** | The number of confirmations for this transaction | [optional]
**timestamp** | **float** | The time of the transaction | [optional]
**status** | [**\OpenAPI\Client\Model\TransactionStatus**](TransactionStatus.md) | The status of this transaction | [optional]
**labels** | [**\OpenAPI\Client\Model\LabelData[]**](LabelData.md) | Labels linked to this transaction | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
