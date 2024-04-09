# # GetTransactionDetailsByTransactionIDRIBS

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**locktime** | **int** | Represents the locktime on the transaction on the specific blockchain, i.e. the blockheight at which the transaction is valid. |
**size** | **int** | Represents the total size of this transaction. |
**v_size** | **int** | Represents the virtual size of this transaction. |
**version** | **int** | Defines the version of the transaction. |
**vin** | [**\com.cryptoapis.rest_apis.sdk\Model\GetTransactionDetailsByTransactionIDRIBSZVinInner[]**](GetTransactionDetailsByTransactionIDRIBSZVinInner.md) | Object Array representation of transaction inputs |
**vout** | [**\com.cryptoapis.rest_apis.sdk\Model\GetTransactionDetailsByTransactionIDRIBSZVoutInner[]**](GetTransactionDetailsByTransactionIDRIBSZVoutInner.md) | Object Array representation of transaction outputs |
**contract** | **string** | Represents the specific transaction contract. | [optional]
**gas_limit** | **string** | Represents the amount of gas used by this specific transaction alone. |
**gas_price** | [**\com.cryptoapis.rest_apis.sdk\Model\GetTransactionDetailsByTransactionIDRIBSBSCGasPrice**](GetTransactionDetailsByTransactionIDRIBSBSCGasPrice.md) |  |
**gas_used** | **string** | Represents the exact unit of gas that was used for the transaction. |
**input_data** | **string** | Represents additional information that is required for the transaction. | [optional]
**nonce** | **int** | Represents the sequential running number for an address, starting from 0 for the first transaction. E.g., if the nonce of a transaction is 10, it would be the 11th transaction sent from the sender&#39;s address. |
**signature_data** | [**\com.cryptoapis.rest_apis.sdk\Model\GetTransactionDetailsByTransactionIDRIBSESignatureData**](GetTransactionDetailsByTransactionIDRIBSESignatureData.md) |  | [optional]
**transaction_status** | **string** | Represents the status of this transaction. |
**binding_sig** | **string** | It is used to enforce balance of Spend and Output transfers, in order to prevent their replay across transactions. |
**expiry_height** | **int** | Represents a block height after which the transaction will expire. |
**join_split_pub_key** | **string** | Represents an encoding of a JoinSplitSig public validating key. |
**join_split_sig** | **string** | Is used to sign transactions that contain at least one JoinSplit description. |
**overwintered** | **bool** | \&quot;Overwinter\&quot; is the network upgrade for the Zcash blockchain. |
**v_join_split** | [**\com.cryptoapis.rest_apis.sdk\Model\GetTransactionDetailsByTransactionIDRIBSZVJoinSplitInner[]**](GetTransactionDetailsByTransactionIDRIBSZVJoinSplitInner.md) | Represents a sequence of JoinSplit descriptions using BCTV14 proofs. |
**v_shielded_output** | [**\com.cryptoapis.rest_apis.sdk\Model\GetTransactionDetailsByTransactionIDRIBSZVShieldedOutputInner[]**](GetTransactionDetailsByTransactionIDRIBSZVShieldedOutputInner.md) | Object Array representation of transaction output descriptions |
**v_shielded_spend** | [**\com.cryptoapis.rest_apis.sdk\Model\GetTransactionDetailsByTransactionIDRIBSZVShieldedSpendInner[]**](GetTransactionDetailsByTransactionIDRIBSZVShieldedSpendInner.md) | Object Array representation of transaction spend descriptions |
**value_balance** | **string** | String representation of the transaction value balance |
**version_group_id** | **string** | Represents the transaction version group ID. |
**addresses** | **string[]** |  |
**memo** | **string** | Represents an additional information that can be attached to a payment transaction. It is an optional field that can be used to provide a message or a reference number along with the payment. | [optional]
**memo_type** | **string** | Represents a field that defines the format of the memo data. It specifies whether the memo field contains plaintext or encoded data, and how the data should be interpreted. |
**operations** | [**\com.cryptoapis.rest_apis.sdk\Model\GetTransactionDetailsByTransactionIDRIBSSOperationsInner[]**](GetTransactionDetailsByTransactionIDRIBSSOperationsInner.md) | Object Array representation of transaction operations |
**paging_token** | **string** | Represents the paging token used to retrieve data from the Stellar network in manageable chunks, rather than in a single large response. |
**counter** | **int** | Representation of the counter value |
**internal_transactions_count** | **int** | Representation of the internal transactions count, included in the transaction |
**operations_count** | **int** | Representation of the transaction operations count, included in the transaction |
**token_transfers_count** | **int** | Representation of the token transfers count, included in the transaction |
**bandwidth** | **string** | Representats of the bandwidth used for the transaction |
**energy** | **string** | Representats of the energy used for the transaction |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
