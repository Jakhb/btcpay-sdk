# # UpdatePaymentMethodConfigConfig

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**use_bech32_scheme** | **bool** | Whether to use [LUD-01](https://github.com/fiatjaf/lnurl-rfc/blob/luds/01.md)&#39;s bech32 format or to use [LUD-17](https://github.com/fiatjaf/lnurl-rfc/blob/luds/17.md) url formatting. | [optional]
**lud12_enabled** | **bool** | Allow comments to be passed on via lnurl. | [optional]
**connection_string** | **string** | The lightning connection string. Set to &#39;Internal Node&#39; to use the internal node. (See [this doc](https://github.com/btcpayserver/BTCPayServer.Lightning/blob/master/README.md#examples) for some example) | [optional]
**derivation_scheme** | **string** | The derivation scheme | [optional]
**label** | **string** | A label that will be shown in the UI | [optional]
**account_key_path** | **string** | The wallet fingerprint followed by the keypath to derive the account key used for signing operation or creating PSBTs | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
