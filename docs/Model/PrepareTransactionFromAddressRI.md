# # PrepareTransactionFromAddressRI

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **string** | Representation of the transacted amount |
**data_hex** | **string** | Representation of the data in hex value | [optional]
**nonce** | **string** | Represents the sequential running number for an address, starting from 0 for the first transaction. E.g., if the nonce of a transaction is 10, it would be the 11th transaction sent from the sender&#39;s address. | [optional]
**recipient** | **string** | The address which receives this transaction. In UTXO-based protocols like Bitcoin there could be several senders while in account-based protocols like Ethereum there is always only one recipient. |
**sender** | **string** | Represents the address which sends this transaction. In UTXO-based protocols like Bitcoin there could be several senders while in account-based protocols like Ethereum there is always only one sender. |
**sighash** | **string** | Representation of the hash that should be signed |
**blockchain_specific** | [**\com.cryptoapis.rest_apis.sdk\Model\PrepareTransactionFromAddressRIBS**](PrepareTransactionFromAddressRIBS.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
