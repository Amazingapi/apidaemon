# # GetTransactionDetailsByTransactionIDRIBSS

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**addresses** | **string[]** |  |
**memo** | **string** | Represents an additional information that can be attached to a payment transaction. It is an optional field that can be used to provide a message or a reference number along with the payment. | [optional]
**memo_type** | **string** | Represents a field that defines the format of the memo data. It specifies whether the memo field contains plaintext or encoded data, and how the data should be interpreted. |
**operations** | [**\com.cryptoapis.rest_apis.sdk\Model\GetTransactionDetailsByTransactionIDRIBSSOperationsInner[]**](GetTransactionDetailsByTransactionIDRIBSSOperationsInner.md) | Object Array representation of transaction operations |
**paging_token** | **string** | Represents the paging token used to retrieve data from the Stellar network in manageable chunks, rather than in a single large response. |
**transaction_status** | **bool** | Represents the status of this transaction. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
