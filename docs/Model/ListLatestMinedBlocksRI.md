# # ListLatestMinedBlocksRI

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hash** | **string** | Represents the same as transactionId for account-based protocols like Ethereum, while it could be different in UTXO-based protocols like Bitcoin. E.g., in UTXO-based protocols hash is different from transactionId for SegWit transactions. |
**height** | **int** | Represents the hight of the block where this transaction was mined/confirmed for first time. The height is defined as the number of blocks in the blockchain preceding this specific block. |
**previous_block_hash** | **string** | Represents the hash of the previous block, also known as the parent block. |
**timestamp** | **int** | Defines the exact date/time when this block was mined in Unix Timestamp. |
**transactions_count** | **int** | Represents the total number of all transactions as part of this block. |
**blockchain_specific** | [**\com.cryptoapis.rest_apis.sdk\Model\ListLatestMinedBlocksRIBS**](ListLatestMinedBlocksRIBS.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
