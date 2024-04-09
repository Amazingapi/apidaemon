# com.cryptoapis.rest_apis.sdk\CreateSubscriptionsForApi

All URIs are relative to https://rest.cryptoapis.io, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**blockHeightReached()**](CreateSubscriptionsForApi.md#blockHeightReached) | **POST** /blockchain-events/{blockchain}/{network}/subscriptions/block-height-reached | Block Height Reached |
| [**minedTransaction()**](CreateSubscriptionsForApi.md#minedTransaction) | **POST** /blockchain-events/{blockchain}/{network}/subscriptions/transaction-mined | Mined Transaction |
| [**newBlock()**](CreateSubscriptionsForApi.md#newBlock) | **POST** /blockchain-events/{blockchain}/{network}/subscriptions/block-mined | New Block |
| [**newConfirmedCoinsTransactions()**](CreateSubscriptionsForApi.md#newConfirmedCoinsTransactions) | **POST** /blockchain-events/{blockchain}/{network}/subscriptions/address-coins-transactions-confirmed | New Confirmed Coins Transactions |
| [**newConfirmedCoinsTransactionsAndEachConfirmation()**](CreateSubscriptionsForApi.md#newConfirmedCoinsTransactionsAndEachConfirmation) | **POST** /blockchain-events/{blockchain}/{network}/subscriptions/address-coins-transactions-confirmed-each-confirmation | New Confirmed Coins Transactions And Each Confirmation |
| [**newConfirmedInternalTransactions()**](CreateSubscriptionsForApi.md#newConfirmedInternalTransactions) | **POST** /blockchain-events/{blockchain}/{network}/subscriptions/address-internal-transactions-confirmed | New Confirmed Internal Transactions |
| [**newConfirmedInternalTransactionsAndEachConfirmation()**](CreateSubscriptionsForApi.md#newConfirmedInternalTransactionsAndEachConfirmation) | **POST** /blockchain-events/{blockchain}/{network}/subscriptions/address-internal-transactions-confirmed-each-confirmation | New Confirmed Internal Transactions And Each Confirmation |
| [**newConfirmedTokensTransactions()**](CreateSubscriptionsForApi.md#newConfirmedTokensTransactions) | **POST** /blockchain-events/{blockchain}/{network}/subscriptions/address-tokens-transactions-confirmed | New Confirmed Tokens Transactions |
| [**newConfirmedTokensTransactionsAndEachConfirmation()**](CreateSubscriptionsForApi.md#newConfirmedTokensTransactionsAndEachConfirmation) | **POST** /blockchain-events/{blockchain}/{network}/subscriptions/address-tokens-transactions-confirmed-each-confirmation | New Confirmed Tokens Transactions And Each Confirmation |
| [**newRevertedBlock()**](CreateSubscriptionsForApi.md#newRevertedBlock) | **POST** /blockchain-events/{blockchain}/{network}/subscriptions/reverted-block | New Reverted Block |
| [**newUnconfirmedCoinsTransactions()**](CreateSubscriptionsForApi.md#newUnconfirmedCoinsTransactions) | **POST** /blockchain-events/{blockchain}/{network}/subscriptions/address-coins-transactions-unconfirmed | New Unconfirmed Coins Transactions |
| [**newUnconfirmedTokensTransactions()**](CreateSubscriptionsForApi.md#newUnconfirmedTokensTransactions) | **POST** /blockchain-events/{blockchain}/{network}/subscriptions/address-tokens-transactions-unconfirmed | New Unconfirmed Tokens Transactions |


## `blockHeightReached()`

```php
blockHeightReached($blockchain, $network, $context, $block_height_reached_rb): \com.cryptoapis.rest_apis.sdk\Model\BlockHeightReachedR
```

Block Height Reached

Through this endpoint customers can create callback subscriptions for a specific block height that hasn't been reached yet. In this case the event is when the specified block height in the request body is reached in a said blockchain. By creating this subscription the user will be notified by Crypto APIs 2.0 when that event occurs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\CreateSubscriptionsForApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = bitcoin; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = testnet; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"ropsten\" are test networks.
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$block_height_reached_rb = new \com.cryptoapis.rest_apis.sdk\Model\BlockHeightReachedRB(); // \com.cryptoapis.rest_apis.sdk\Model\BlockHeightReachedRB

try {
    $result = $apiInstance->blockHeightReached($blockchain, $network, $context, $block_height_reached_rb);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateSubscriptionsForApi->blockHeightReached: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;ropsten\&quot; are test networks. | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **block_height_reached_rb** | [**\com.cryptoapis.rest_apis.sdk\Model\BlockHeightReachedRB**](../Model/BlockHeightReachedRB.md)|  | [optional] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\BlockHeightReachedR**](../Model/BlockHeightReachedR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `minedTransaction()`

```php
minedTransaction($blockchain, $network, $context, $mined_transaction_rb): \com.cryptoapis.rest_apis.sdk\Model\MinedTransactionR
```

Mined Transaction

Through this endpoint customers can create callback subscriptions for a specific event. In this case the event is when a specific transaction is mined. By creating this subscription the user will be notified by Crypto APIs 2.0 when that event occurs. The information is returned per specified `transactionId`.    A transaction is mined when it is included in a new block in the blockchain.    {note}To have an operational callback subscription, you need to first verify a domain for the Callback URL. Please see more information on Callbacks [here](https://developers.cryptoapis.io/technical-documentation/general-information/callbacks#callback-url).{/note}    {warning}Crypto APIs will notify the user **only when** the event occurs. There are cases when the specific event doesn't happen at all, or takes a long time to do so. A callback notification **will not** be sent if the event does not or cannot occur, or will take long time to occur.{/warning}

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\CreateSubscriptionsForApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = bitcoin; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = testnet; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"ropsten\" are test networks.
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$mined_transaction_rb = new \com.cryptoapis.rest_apis.sdk\Model\MinedTransactionRB(); // \com.cryptoapis.rest_apis.sdk\Model\MinedTransactionRB

try {
    $result = $apiInstance->minedTransaction($blockchain, $network, $context, $mined_transaction_rb);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateSubscriptionsForApi->minedTransaction: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;ropsten\&quot; are test networks. | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **mined_transaction_rb** | [**\com.cryptoapis.rest_apis.sdk\Model\MinedTransactionRB**](../Model/MinedTransactionRB.md)|  | [optional] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\MinedTransactionR**](../Model/MinedTransactionR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newBlock()`

```php
newBlock($blockchain, $network, $context, $new_block_rb): \com.cryptoapis.rest_apis.sdk\Model\NewBlockR
```

New Block

Through this endpoint customers can create callback subscriptions for a specific event. In this case the event is when a new block is mined in the specific blockchain. By creating this subscription the user will be notified by Crypto APIs 2.0 when that event occurs. The information is returned per specified address.    A new block is mined when it is added to the chain once a consensus is reached by the majority of the miners, which is when the block gets validated and added to the blockchain.    {note}To have an operational callback subscription, you need to first verify a domain for the Callback URL. Please see more information on Callbacks [here](https://developers.cryptoapis.io/technical-documentation/general-information/callbacks#callback-url).{/note}    {warning}Crypto APIs will notify the user **only when** the event occurs. There are cases when the specific event doesn't happen at all, or takes a long time to do so. A callback notification **will not** be sent if the event does not or cannot occur, or will take long time to occur.{/warning}

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\CreateSubscriptionsForApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = bitcoin; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = testnet; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"goerli\" are test networks.
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$new_block_rb = new \com.cryptoapis.rest_apis.sdk\Model\NewBlockRB(); // \com.cryptoapis.rest_apis.sdk\Model\NewBlockRB

try {
    $result = $apiInstance->newBlock($blockchain, $network, $context, $new_block_rb);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateSubscriptionsForApi->newBlock: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;goerli\&quot; are test networks. | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **new_block_rb** | [**\com.cryptoapis.rest_apis.sdk\Model\NewBlockRB**](../Model/NewBlockRB.md)|  | [optional] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\NewBlockR**](../Model/NewBlockR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newConfirmedCoinsTransactions()`

```php
newConfirmedCoinsTransactions($blockchain, $network, $context, $new_confirmed_coins_transactions_rb): \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedCoinsTransactionsR
```

New Confirmed Coins Transactions

Through this endpoint customers can create callback subscriptions for a specific event. In this case the event is when there are new incoming or outgoing confirmed transactions for coins from/to the customer's address. By creating this subscription the user will be notified by Crypto APIs 2.0 when that event occurs. The information is returned per specified address.     Being confirmed means that the transactions are verified by miners and added to the next block.    {note}For UTXO-based protocols like Bitcoin a transaction could have multiple inputs and outputs which means the address could in as both sender and recipient. [Here](https://developers.cryptoapis.io/technical-documentation/general-information/callbacks#callback-data-returned-for-utxo-based-transactions) is how we inform you on that.{/note}    {note}To have an operational callback subscription, you need to first verify a domain for the Callback URL. Please see more information on Callbacks [here](https://developers.cryptoapis.io/technical-documentation/general-information/callbacks#callback-url).{/note}    {warning}Crypto APIs will notify the user **only when** the event occurs. There are cases when the specific event doesn't happen at all, or takes a long time to do so. A callback notification **will not** be sent if the event does not or cannot occur, or will take long time to occur.{/warning}

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\CreateSubscriptionsForApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = bitcoin; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = testnet; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"goerli\" are test networks.
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$new_confirmed_coins_transactions_rb = new \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedCoinsTransactionsRB(); // \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedCoinsTransactionsRB

try {
    $result = $apiInstance->newConfirmedCoinsTransactions($blockchain, $network, $context, $new_confirmed_coins_transactions_rb);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateSubscriptionsForApi->newConfirmedCoinsTransactions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;goerli\&quot; are test networks. | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **new_confirmed_coins_transactions_rb** | [**\com.cryptoapis.rest_apis.sdk\Model\NewConfirmedCoinsTransactionsRB**](../Model/NewConfirmedCoinsTransactionsRB.md)|  | [optional] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\NewConfirmedCoinsTransactionsR**](../Model/NewConfirmedCoinsTransactionsR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newConfirmedCoinsTransactionsAndEachConfirmation()`

```php
newConfirmedCoinsTransactionsAndEachConfirmation($blockchain, $network, $context, $new_confirmed_coins_transactions_and_each_confirmation_rb): \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedCoinsTransactionsAndEachConfirmationR
```

New Confirmed Coins Transactions And Each Confirmation

Through this endpoint customers can create callback subscriptions for a specific event. In this case the event is when there are new incoming or outgoing confirmed transactions for coins from/to the customer's address with also a response at each confirmation the transaction has received until the specified confirmations limit is reached. By creating this subscription the user will be notified by Crypto APIs 2.0 when that event occurs. The information is returned per specified address.     Being confirmed means that the transactions are verified by miners and added to the next block. This endpoint refers to **coins transactions only, not tokens**.    {note}For UTXO-based protocols like Bitcoin a transaction could have multiple inputs and outputs which means the address could in as both sender and recipient. [Here](https://developers.cryptoapis.io/technical-documentation/general-information/callbacks#callback-data-returned-for-utxo-based-transactions) is how we inform you on that.{/note}    {note}To have an operational callback subscription, you need to first verify a domain for the Callback URL. Please see more information on Callbacks [here](https://developers.cryptoapis.io/technical-documentation/general-information/callbacks#callback-url).{/note}    {warning}Crypto APIs will notify the user **only when** the event occurs. There are cases when the specific event doesn't happen at all, or takes a long time to do so. A callback notification **will not** be sent if the event does not or cannot occur, or will take long time to occur.{/warning}

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\CreateSubscriptionsForApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = bitcoin; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = testnet; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"goerli\" are test networks.
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$new_confirmed_coins_transactions_and_each_confirmation_rb = new \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedCoinsTransactionsAndEachConfirmationRB(); // \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedCoinsTransactionsAndEachConfirmationRB

try {
    $result = $apiInstance->newConfirmedCoinsTransactionsAndEachConfirmation($blockchain, $network, $context, $new_confirmed_coins_transactions_and_each_confirmation_rb);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateSubscriptionsForApi->newConfirmedCoinsTransactionsAndEachConfirmation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;goerli\&quot; are test networks. | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **new_confirmed_coins_transactions_and_each_confirmation_rb** | [**\com.cryptoapis.rest_apis.sdk\Model\NewConfirmedCoinsTransactionsAndEachConfirmationRB**](../Model/NewConfirmedCoinsTransactionsAndEachConfirmationRB.md)|  | [optional] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\NewConfirmedCoinsTransactionsAndEachConfirmationR**](../Model/NewConfirmedCoinsTransactionsAndEachConfirmationR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newConfirmedInternalTransactions()`

```php
newConfirmedInternalTransactions($blockchain, $network, $context, $new_confirmed_internal_transactions_rb): \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedInternalTransactionsR
```

New Confirmed Internal Transactions

Through this endpoint customers can create callback subscriptions for a specific event. In this case the event is when there are new confirmed internal transactions. By creating this subscription the user will be notified by Crypto APIs 2.0 when that event occurs.    Being confirmed means that the transactions are verified by miners and added to the next block.    {note}To have an operational callback subscription, you need to first verify a domain for the Callback URL. Please see more information on Callbacks [here](https://developers.cryptoapis.io/technical-documentation/general-information/callbacks#callback-url).{/note}    {warning}Crypto APIs will notify the user **only when** the event occurs. There are cases when the specific event doesn't happen at all, or takes a long time to do so. A callback notification **will not** be sent if the event does not or cannot occur, or will take long time to occur.{/warning}

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\CreateSubscriptionsForApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = ethereum-classic; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = mordor; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"ropsten\" are test networks.
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$new_confirmed_internal_transactions_rb = new \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedInternalTransactionsRB(); // \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedInternalTransactionsRB

try {
    $result = $apiInstance->newConfirmedInternalTransactions($blockchain, $network, $context, $new_confirmed_internal_transactions_rb);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateSubscriptionsForApi->newConfirmedInternalTransactions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;ropsten\&quot; are test networks. | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **new_confirmed_internal_transactions_rb** | [**\com.cryptoapis.rest_apis.sdk\Model\NewConfirmedInternalTransactionsRB**](../Model/NewConfirmedInternalTransactionsRB.md)|  | [optional] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\NewConfirmedInternalTransactionsR**](../Model/NewConfirmedInternalTransactionsR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newConfirmedInternalTransactionsAndEachConfirmation()`

```php
newConfirmedInternalTransactionsAndEachConfirmation($blockchain, $network, $context, $new_confirmed_internal_transactions_and_each_confirmation_rb): \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedInternalTransactionsAndEachConfirmationR
```

New Confirmed Internal Transactions And Each Confirmation

Through this endpoint customers can create callback subscriptions for a specific event. In this case the event is when there are new confirmed internal transactions. Includes also a response at each confirmation the transaction receives until the specified confirmations limit is reached. By creating this subscription the user will be notified by Crypto APIs 2.0 when that event occurs.     Being confirmed means that the transactions are verified by miners and added to the next block.    {note}To have an operational callback subscription, you need to first verify a domain for the Callback URL. Please see more information on Callbacks [here](https://developers.cryptoapis.io/technical-documentation/general-information/callbacks#callback-url).{/note}    {warning}Crypto APIs will notify the user **only when** the event occurs. There are cases when the specific event doesn't happen at all, or takes a long time to do so. A callback notification **will not** be sent if the event does not or cannot occur, or will take long time to occur.{/warning}

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\CreateSubscriptionsForApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = ethereum-classic; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = mordor; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"ropsten\" are test networks.
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$new_confirmed_internal_transactions_and_each_confirmation_rb = new \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedInternalTransactionsAndEachConfirmationRB(); // \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedInternalTransactionsAndEachConfirmationRB

try {
    $result = $apiInstance->newConfirmedInternalTransactionsAndEachConfirmation($blockchain, $network, $context, $new_confirmed_internal_transactions_and_each_confirmation_rb);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateSubscriptionsForApi->newConfirmedInternalTransactionsAndEachConfirmation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;ropsten\&quot; are test networks. | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **new_confirmed_internal_transactions_and_each_confirmation_rb** | [**\com.cryptoapis.rest_apis.sdk\Model\NewConfirmedInternalTransactionsAndEachConfirmationRB**](../Model/NewConfirmedInternalTransactionsAndEachConfirmationRB.md)|  | [optional] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\NewConfirmedInternalTransactionsAndEachConfirmationR**](../Model/NewConfirmedInternalTransactionsAndEachConfirmationR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newConfirmedTokensTransactions()`

```php
newConfirmedTokensTransactions($blockchain, $network, $context, $new_confirmed_tokens_transactions_rb): \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedTokensTransactionsR
```

New Confirmed Tokens Transactions

Through this endpoint customers can create callback subscriptions for a specific event. In this case the event is when there are new incoming or outgoing confirmed transactions for tokens from/to the customer's address. By creating this subscription the user will be notified by Crypto APIs 2.0 when that event occurs. The information is returned per specified address.     Being confirmed means that the transactions are verified by miners and added to the next block. This endpoint refers to **tokens transactions only, not coins**.    {note}To have an operational callback subscription, you need to first verify a domain for the Callback URL. Please see more information on Callbacks [here](https://developers.cryptoapis.io/technical-documentation/general-information/callbacks#callback-url).{/note}    {warning}Crypto APIs will notify the user **only when** the event occurs. There are cases when the specific event doesn't happen at all, or takes a long time to do so. A callback notification **will not** be sent if the event does not or cannot occur, or will take long time to occur.{/warning}

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\CreateSubscriptionsForApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = ethereum; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = goerli; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"goerli\" are test networks.
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$new_confirmed_tokens_transactions_rb = new \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedTokensTransactionsRB(); // \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedTokensTransactionsRB

try {
    $result = $apiInstance->newConfirmedTokensTransactions($blockchain, $network, $context, $new_confirmed_tokens_transactions_rb);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateSubscriptionsForApi->newConfirmedTokensTransactions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;goerli\&quot; are test networks. | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **new_confirmed_tokens_transactions_rb** | [**\com.cryptoapis.rest_apis.sdk\Model\NewConfirmedTokensTransactionsRB**](../Model/NewConfirmedTokensTransactionsRB.md)|  | [optional] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\NewConfirmedTokensTransactionsR**](../Model/NewConfirmedTokensTransactionsR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newConfirmedTokensTransactionsAndEachConfirmation()`

```php
newConfirmedTokensTransactionsAndEachConfirmation($blockchain, $network, $context, $new_confirmed_tokens_transactions_and_each_confirmation_rb): \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedTokensTransactionsAndEachConfirmationR
```

New Confirmed Tokens Transactions And Each Confirmation

Through this endpoint customers can create callback subscriptions for a specific event. In this case the event is when there are new incoming or outgoing confirmed transactions for tokens from/to the customer's address with also a response at each confirmation the transaction has received until the specified confirmations limit is reached. By creating this subscription the user will be notified by Crypto APIs 2.0 when that event occurs. The information is returned per specified address.     Being confirmed means that the transactions are verified by miners and added to the next block. This endpoint refers to **tokens transactions only, not coins**.    {note}To have an operational callback subscription, you need to first verify a domain for the Callback URL. Please see more information on Callbacks [here](https://developers.cryptoapis.io/technical-documentation/general-information/callbacks#callback-url).{/note}    {warning}Crypto APIs will notify the user **only when** the event occurs. There are cases when the specific event doesn't happen at all, or takes a long time to do so. A callback notification **will not** be sent if the event does not or cannot occur, or will take long time to occur.{/warning}

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\CreateSubscriptionsForApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = ethereum; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = goerli; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"goerli\" are test networks.
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$new_confirmed_tokens_transactions_and_each_confirmation_rb = new \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedTokensTransactionsAndEachConfirmationRB(); // \com.cryptoapis.rest_apis.sdk\Model\NewConfirmedTokensTransactionsAndEachConfirmationRB

try {
    $result = $apiInstance->newConfirmedTokensTransactionsAndEachConfirmation($blockchain, $network, $context, $new_confirmed_tokens_transactions_and_each_confirmation_rb);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateSubscriptionsForApi->newConfirmedTokensTransactionsAndEachConfirmation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;goerli\&quot; are test networks. | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **new_confirmed_tokens_transactions_and_each_confirmation_rb** | [**\com.cryptoapis.rest_apis.sdk\Model\NewConfirmedTokensTransactionsAndEachConfirmationRB**](../Model/NewConfirmedTokensTransactionsAndEachConfirmationRB.md)|  | [optional] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\NewConfirmedTokensTransactionsAndEachConfirmationR**](../Model/NewConfirmedTokensTransactionsAndEachConfirmationR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newRevertedBlock()`

```php
newRevertedBlock($blockchain, $network, $context, $new_reverted_block_rb): \com.cryptoapis.rest_apis.sdk\Model\NewRevertedBlockR
```

New Reverted Block

By subscribing to this event, customers will receive callbacks from Crypto APIs every time when a block is reverted on a specific blockchain. This can happen in cases when two blocks are mined at the same time and the nodes cannot agree on which one was first. This occurs as part of the chain reorganization process.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\CreateSubscriptionsForApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = ethereum; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = goerli; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"ropsten\" are test networks.
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$new_reverted_block_rb = new \com.cryptoapis.rest_apis.sdk\Model\NewRevertedBlockRB(); // \com.cryptoapis.rest_apis.sdk\Model\NewRevertedBlockRB

try {
    $result = $apiInstance->newRevertedBlock($blockchain, $network, $context, $new_reverted_block_rb);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateSubscriptionsForApi->newRevertedBlock: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;ropsten\&quot; are test networks. | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **new_reverted_block_rb** | [**\com.cryptoapis.rest_apis.sdk\Model\NewRevertedBlockRB**](../Model/NewRevertedBlockRB.md)|  | [optional] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\NewRevertedBlockR**](../Model/NewRevertedBlockR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newUnconfirmedCoinsTransactions()`

```php
newUnconfirmedCoinsTransactions($blockchain, $network, $context, $new_unconfirmed_coins_transactions_rb): \com.cryptoapis.rest_apis.sdk\Model\NewUnconfirmedCoinsTransactionsR
```

New Unconfirmed Coins Transactions

Through this endpoint customers can create callback subscriptions for a specific event. In this case the event is when there are new unconfirmed coins transactions for the user. By creating this subscription the user will be notified by Crypto APIs 2.0 when that event occurs. The information is returned per specified address.    Unconfirmed coins transactions remain in the mempool (memory pool) until they are confirmed by miners and added to the next block. Sometimes spikes in transaction activity can cause delays in confirmations.    {note}For UTXO-based protocols like Bitcoin a transaction could have multiple inputs and outputs which means the address could in as both sender and recipient. [Here](https://developers.cryptoapis.io/technical-documentation/general-information/callbacks#callback-data-returned-for-utxo-based-transactions) is how we inform you on that.{/note}    {warning}We cannot guarantee at 100% that webhooks for unconfirmed transactions will always be received. Some may **not get received** due to the possibility of some nodes not being updated with that information. This can occur in networks with low activity and/or not many nodes, e.g. Testnet networks and rarely Mainnets.{/warning}    {note}To have an operational callback subscription, you need to first verify a domain for the Callback URL. Please see more information on Callbacks [here](https://developers.cryptoapis.io/technical-documentation/general-information/callbacks#callback-url).{/note}    {note}It is also **important to note** that just because pending unconfirmed transactions are in the mempool, **doesn't necessarily** mean they will get confirmed.{/note}    {warning}Crypto APIs will notify the user **only when** the event occurs. There are cases when the specific event doesn't happen at all, or takes a long time to do so. A callback notification **will not** be sent if the event does not or cannot occur, or will take long time to occur.{/warning}

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\CreateSubscriptionsForApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = bitcoin; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = testnet; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"ropsten\" are test networks.
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$new_unconfirmed_coins_transactions_rb = new \com.cryptoapis.rest_apis.sdk\Model\NewUnconfirmedCoinsTransactionsRB(); // \com.cryptoapis.rest_apis.sdk\Model\NewUnconfirmedCoinsTransactionsRB

try {
    $result = $apiInstance->newUnconfirmedCoinsTransactions($blockchain, $network, $context, $new_unconfirmed_coins_transactions_rb);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateSubscriptionsForApi->newUnconfirmedCoinsTransactions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;ropsten\&quot; are test networks. | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **new_unconfirmed_coins_transactions_rb** | [**\com.cryptoapis.rest_apis.sdk\Model\NewUnconfirmedCoinsTransactionsRB**](../Model/NewUnconfirmedCoinsTransactionsRB.md)|  | [optional] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\NewUnconfirmedCoinsTransactionsR**](../Model/NewUnconfirmedCoinsTransactionsR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newUnconfirmedTokensTransactions()`

```php
newUnconfirmedTokensTransactions($blockchain, $network, $context, $new_unconfirmed_tokens_transactions_rb): \com.cryptoapis.rest_apis.sdk\Model\NewUnconfirmedTokensTransactionsR
```

New Unconfirmed Tokens Transactions

Through this endpoint customers can create callback subscriptions for a specific event. In this case the event is when there are new unconfirmed tokens transactions for the user. By creating this subscription the user will be notified by Crypto APIs 2.0 when that event occurs. The information is returned per specified address.    Unconfirmed tokens transactions remain in the mempool (memory pool) until they are confirmed by miners and added to the next block. Sometimes spikes in transaction activity can cause delays in confirmations.    {warning}We cannot guarantee at 100% that webhooks for unconfirmed transactions will always be received. Some may **not get received** due to the possibility of some nodes not being updated with that information. This can occur in networks with low activity and/or not many nodes, e.g. Testnet networks and rarely Mainnets.{/warning}    {note}To have an operational callback subscription, you need to first verify a domain for the Callback URL. Please see more information on Callbacks [here](https://developers.cryptoapis.io/technical-documentation/general-information/callbacks#callback-url).{/note}    {note}It is also **important to note** that just because pending unconfirmed transactions are in the mempool, **doesn't necessarily** mean they will get confirmed.{/note}    {warning}Crypto APIs will notify the user **only when** the event occurs. There are cases when the specific event doesn't happen at all, or takes a long time to do so. A callback notification **will not** be sent if the event does not or cannot occur, or will take long time to occur.{/warning}

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\CreateSubscriptionsForApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = ethereum; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = ropsten; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"ropsten\" are test networks.
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$new_unconfirmed_tokens_transactions_rb = new \com.cryptoapis.rest_apis.sdk\Model\NewUnconfirmedTokensTransactionsRB(); // \com.cryptoapis.rest_apis.sdk\Model\NewUnconfirmedTokensTransactionsRB

try {
    $result = $apiInstance->newUnconfirmedTokensTransactions($blockchain, $network, $context, $new_unconfirmed_tokens_transactions_rb);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateSubscriptionsForApi->newUnconfirmedTokensTransactions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;ropsten\&quot; are test networks. | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **new_unconfirmed_tokens_transactions_rb** | [**\com.cryptoapis.rest_apis.sdk\Model\NewUnconfirmedTokensTransactionsRB**](../Model/NewUnconfirmedTokensTransactionsRB.md)|  | [optional] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\NewUnconfirmedTokensTransactionsR**](../Model/NewUnconfirmedTokensTransactionsR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
