# # ApplicationServerInfoSyncStatusData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment_method_id** | **string** | Payment method IDs. Available payment method IDs for Bitcoin are:   - &#x60;\&quot;BTC-CHAIN\&quot;&#x60;: Onchain    -&#x60;\&quot;BTC-LN\&quot;&#x60;: Lightning    - &#x60;\&quot;BTC-LNURL\&quot;&#x60;: LNURL | [optional]
**node_information** | [**\OpenAPI\Client\Model\ApplicationServerInfoNodeStatusData**](ApplicationServerInfoNodeStatusData.md) |  | [optional]
**chain_height** | **int** | The height of the chain of header of the internal indexer | [optional]
**sync_height** | **float** | The height of the latest indexed block of the internal indexer | [optional]
**available** | **bool** | True if the full node and the indexer are fully synchronized | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
