# # GetBlockDetailsByBlockHeightRIBS

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bits** | **string** | Represents a specific sub-unit of Zcash. Bits have two-decimal precision |
**chainwork** | **string** | Represents a hexadecimal number of all the hashes necessary to produce the current chain. E.g., when converting 0000000000000000000000000000000000000000000086859f7a841475b236fd to a decimal you get 635262017308958427068157 hashes, or 635262 exahashes. |
**difficulty** | **string** | Numeric representation of the block difficulty | [optional]
**merkle_root** | **string** | Defines the single and final (root) node of a Merkle tree. It is the combined hash of all transactions&#39; hashes that are part of a blockchain block. |
**nonce** | **string** | Represents a random value that can be adjusted to satisfy the Proof of Work. |
**size** | **int** | Represents the total size of the block in Bytes. |
**stripped_size** | **int** | Defines the numeric representation of the block size excluding the witness data. |
**version** | **int** | Represents the block version number. |
**version_hex** | **string** | Is the hexadecimal string representation of the block&#39;s version. |
**weight** | **int** | Represents a measurement to compare the size of different transactions to each other in proportion to the block size limi |
**extra_data** | **string** | Represents any data that can be included by the miner in the block. |
**gas_limit** | **string** | Defines the total gas limit of all transactions in the block. |
**gas_used** | **string** | Represents the total amount of gas used by all transactions in this block. |
**mined_in_seconds** | **int** | Specifies the amount of time required for the block to be mined in seconds. |
**sha3_uncles** | **string** | Defines the combined hash of all uncles for a given parent. |
**total_difficulty** | **string** | Defines the total difficulty of the chain until this block, i.e. how difficult it is for a specific miner to mine a new block. |
**base_fee** | **string** | Representation of the base fee |
**base_reserve** | **string** | Representation of the base reserve that refers to the minimum amount of XLM (the native cryptocurrency of the Stellar network) that an account must hold as a reserve as minimum balance. |
**failed_transactions** | **int** | Representation of the blocks&#39; failed transactions count |
**protocol_version** | **string** | Representation of protocol version which refers to the specific set of rules and standards that govern the behavior of the network&#39;s nodes and participants. |
**total_coins** | **string** | Representation of the total coins |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
