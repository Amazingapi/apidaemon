# # PrepareATransactionFromAnAddressInHDWalletXPubYPubZPubRBDataItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**additional_data** | **string** | Representation of the additional data. | [optional]
**amount** | **string** | Representation of the amount of the transaction |
**recipient** | **string** | Represents a list of recipient addresses with the respective amounts. In account-based protocols like Ethereum there is only one address in this list. |
**sender** | **string** | Represents a  sender address with the respective amount. In account-based protocols like Ethereum there is only one address in this list. |
**xpub** | **string** | Defines the account extended publicly known key which is used to derive all child public keys. |
**fee** | [**\com.cryptoapis.rest_apis.sdk\Model\PrepareATransactionFromAnAddressInHDWalletXPubYPubZPubRBDataItemFee**](PrepareATransactionFromAnAddressInHDWalletXPubYPubZPubRBDataItemFee.md) |  |
**nonce** | **string** | Representation of the nonce value | [optional]
**transaction_type** | **string** | Representation of the transaction type. For Ethereum-Classic and Binance Smart Chain there is no need to provide \&quot;transactionType\&quot; in the request. | [optional] [default to 'gas-fee-market-transaction']
**sequence** | **string** | String representation of the sequence |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
