# # ListConfirmedTokensTransfersByAddressRI

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contract_address** | **string** | Represents the contract address of the token, which controls its logic. It is not the address that holds the tokens. |
**mined_in_block_height** | **int** | Defines the block height in which this transaction was confirmed/mined. |
**recipient_address** | **string** | Defines the address to which the recipient receives the transferred tokens. |
**sender_address** | **string** | Defines the address from which the sender transfers tokens. |
**token_type** | **string** | Defines the specific token type. |
**tokens_amount** | **string** | Defines the token amount of the transfer. | [optional]
**transaction_hash** | **string** | Represents the hash of the transaction, which is its unique identifier. It represents a cryptographic digital fingerprint made by hashing the block header twice through the SHA256 algorithm. |
**transaction_timestamp** | **int** | Defines the specific time/date when the transaction was created in Unix Timestamp. |
**transaction_fee** | [**\com.cryptoapis.rest_apis.sdk\Model\ListConfirmedTokensTransfersByAddressRITransactionFee**](ListConfirmedTokensTransfersByAddressRITransactionFee.md) |  |
**token_decimals** | **int** | Representation of the decimals of the token | [optional]
**token_id** | **string** | Representation of the tokens&#39; identifier | [optional]
**token_name** | **string** | Representation of the name of the token | [optional]
**token_symbol** | **string** | Representation of the tokens&#39; symbol | [optional]
**transaction_id** | **string** | Representation of the transactionId in which the token transfer appears | [optional]
**blockchain_specific** | [**\com.cryptoapis.rest_apis.sdk\Model\ListConfirmedTokensTransfersByAddressRIBS**](ListConfirmedTokensTransfersByAddressRIBS.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
