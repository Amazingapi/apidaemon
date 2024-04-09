# # ListXRPRippleTransactionsByAddressRI

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**destination_tag** | **int** |  | [optional]
**index** | **int** | Represents the index position of the transaction in the block. |
**mined_in_block_hash** | **string** | Represents the hash of the block where this transaction was mined/confirmed for first time. The hash is defined as a cryptographic digital fingerprint made by hashing the block header twice through the SHA256 algorithm. |
**mined_in_block_height** | **int** | Represents the hight of the block where this transaction was mined/confirmed for first time. The height is defined as the number of blocks in the blockchain preceding this specific block. |
**recipients** | [**\com.cryptoapis.rest_apis.sdk\Model\GetXRPRippleTransactionDetailsByTransactionIDRIRecipientsInner[]**](GetXRPRippleTransactionDetailsByTransactionIDRIRecipientsInner.md) | Represents an object of addresses that receive the transactions. |
**senders** | [**\com.cryptoapis.rest_apis.sdk\Model\GetXRPRippleTransactionDetailsByTransactionIDRISendersInner[]**](GetXRPRippleTransactionDetailsByTransactionIDRISendersInner.md) | Represents an object of addresses that provide the funds. |
**sequence** | **int** | Defines the transaction input&#39;s sequence as an integer, which is is used when transactions are replaced with newer versions before LockTime. |
**status** | **string** | Defines the status of the transaction. |
**timestamp** | **int** | Defines the exact date/time in Unix Timestamp when this transaction was mined, confirmed or first seen in Mempool, if it is unconfirmed. |
**transaction_hash** | **string** | Represents the hash of the XRP transaction. |
**type** | **string** | Specifies the type of the transaction. |
**fee** | [**\com.cryptoapis.rest_apis.sdk\Model\ListXRPRippleTransactionsByAddressRIFee**](ListXRPRippleTransactionsByAddressRIFee.md) |  |
**offer** | [**\com.cryptoapis.rest_apis.sdk\Model\ListXRPRippleTransactionsByAddressRIOffer**](ListXRPRippleTransactionsByAddressRIOffer.md) |  |
**receive** | [**\com.cryptoapis.rest_apis.sdk\Model\ListXRPRippleTransactionsByAddressRIReceive**](ListXRPRippleTransactionsByAddressRIReceive.md) |  |
**value** | [**\com.cryptoapis.rest_apis.sdk\Model\ListXRPRippleTransactionsByAddressRIValue**](ListXRPRippleTransactionsByAddressRIValue.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
