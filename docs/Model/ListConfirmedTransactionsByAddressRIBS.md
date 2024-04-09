# # ListConfirmedTransactionsByAddressRIBS

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**locktime** | **int** | Represents the locktime on the transaction on the specific blockchain, i.e. the blockheight at which the transaction is valid. |
**size** | **int** | Represents the total size of this transaction. |
**v_size** | **int** | Represents the virtual size of this transaction. |
**version** | **int** | Defines the version of the transaction. |
**vin** | [**\com.cryptoapis.rest_apis.sdk\Model\ListConfirmedTransactionsByAddressRIBSZVinInner[]**](ListConfirmedTransactionsByAddressRIBSZVinInner.md) | Object Array representation of transaction inputs |
**vout** | [**\com.cryptoapis.rest_apis.sdk\Model\GetTransactionDetailsByTransactionIDRIBSZVoutInner[]**](GetTransactionDetailsByTransactionIDRIBSZVoutInner.md) | Object Array representation of transaction outputs |
**contract** | **string** | Numeric representation of the transaction contract |
**gas_limit** | **string** | Represents the amount of gas used by this specific transaction alone. |
**gas_price** | [**\com.cryptoapis.rest_apis.sdk\Model\ListConfirmedTransactionsByAddressRIBSBSCGasPrice**](ListConfirmedTransactionsByAddressRIBSBSCGasPrice.md) |  |
**gas_used** | **string** | Represents the exact unit of gas that was used for the transaction. |
**input_data** | **string** | Numeric representation of the transaction input |
**internal_transactions_count** | **int** | Representation of the internal transactions count |
**nonce** | **int** | Defines the nonce |
**token_transfers_count** | **int** | Representation of the  token transfers count |
**transaction_status** | **string** | Defines the transaction status |
**binding_sig** | **string** | It is used to enforce balance of Spend and Output transfers, in order to prevent their replay across transactions. |
**expiry_height** | **int** | Represents a block height after which the transaction will expire. |
**join_split_pub_key** | **string** | Represents an encoding of a JoinSplitSig public validating key. |
**join_split_sig** | **string** | Is used to sign transactions that contain at least one JoinSplit description. |
**overwintered** | **bool** | \&quot;Overwinter\&quot; is the network upgrade for the Zcash blockchain. |
**v_join_split** | [**\com.cryptoapis.rest_apis.sdk\Model\ListConfirmedTransactionsByAddressRIBSZVJoinSplitInner[]**](ListConfirmedTransactionsByAddressRIBSZVJoinSplitInner.md) | Represents a sequence of JoinSplit descriptions using BCTV14 proofs. |
**v_shielded_output** | [**\com.cryptoapis.rest_apis.sdk\Model\GetTransactionDetailsByTransactionIDRIBSZVShieldedOutputInner[]**](GetTransactionDetailsByTransactionIDRIBSZVShieldedOutputInner.md) | Object Array representation of transaction output descriptions |
**v_shielded_spend** | [**\com.cryptoapis.rest_apis.sdk\Model\GetTransactionDetailsByTransactionIDRIBSZVShieldedSpendInner[]**](GetTransactionDetailsByTransactionIDRIBSZVShieldedSpendInner.md) | Object Array representation of transaction spend descriptions |
**value_balance** | **string** | Defines the transaction value balance. |
**version_group_id** | **string** | Represents the transaction version group ID. |
**bandwidth_used** | **string** | Numeric representation of the transaction used bandwidth |
**energy_used** | **string** | String representation of the transaction used energy |
**has_internal_transactions** | **bool** | Represents the presence of internal transactions |
**has_token_transfers** | **bool** | Defines if there are  tokens transfers (true) or not (false) |
**addresses** | **string[]** |  |
**counter** | **int** | Representation of the counter value |
**is_confirmed** | **bool** | Representation of the confirmation status of the transfer |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
