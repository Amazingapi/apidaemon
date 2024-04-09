# com.cryptoapis.rest_apis.sdk\InternalApi

All URIs are relative to https://rest.cryptoapis.io, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listInternalTransactionDetailsByTransactionHash()**](InternalApi.md#listInternalTransactionDetailsByTransactionHash) | **GET** /blockchain-data/{blockchain}/{network}/transactions/{transactionHash}/internal | List Internal Transaction Details by Transaction Hash |
| [**listInternalTransactionsByAddress()**](InternalApi.md#listInternalTransactionsByAddress) | **GET** /blockchain-data/{blockchain}/{network}/addresses/{address}/internal | List Internal Transactions By Address |


## `listInternalTransactionDetailsByTransactionHash()`

```php
listInternalTransactionDetailsByTransactionHash($blockchain, $network, $transaction_hash, $context, $limit, $offset): \com.cryptoapis.rest_apis.sdk\Model\ListInternalTransactionDetailsByTransactionHashR
```

List Internal Transaction Details by Transaction Hash

Through this endpoint customers can list internal transactions along with their details by a specific attribute `transactionHash`, which is the parent transaction's Hash.    An internal transaction is the result of a smart contract being triggered by an EOA or a subsequent contract call.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\InternalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = ethereum; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = goerli; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"goerli\" are test networks.
$transaction_hash = 0xbc8245ba5cccb524d91256224689ac0f16678321a266bab8197ad7daab4c9e16; // string | String identifier of the parent transaction of the internal transaction represented in CryptoAPIs.
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$limit = 50; // int | Defines how many items should be returned in the response per page basis.
$offset = 0; // int | The starting index of the response items, i.e. where the response should start listing the returned items.

try {
    $result = $apiInstance->listInternalTransactionDetailsByTransactionHash($blockchain, $network, $transaction_hash, $context, $limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InternalApi->listInternalTransactionDetailsByTransactionHash: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;goerli\&quot; are test networks. | |
| **transaction_hash** | **string**| String identifier of the parent transaction of the internal transaction represented in CryptoAPIs. | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **limit** | **int**| Defines how many items should be returned in the response per page basis. | [optional] [default to 50] |
| **offset** | **int**| The starting index of the response items, i.e. where the response should start listing the returned items. | [optional] [default to 0] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\ListInternalTransactionDetailsByTransactionHashR**](../Model/ListInternalTransactionDetailsByTransactionHashR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listInternalTransactionsByAddress()`

```php
listInternalTransactionsByAddress($blockchain, $network, $address, $context, $limit, $offset): \com.cryptoapis.rest_apis.sdk\Model\ListInternalTransactionsByAddressR
```

List Internal Transactions By Address

Through this endpoint customers can list internal transactions by the `address` attribute.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = com.cryptoapis.rest_apis.sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new com.cryptoapis.rest_apis.sdk\Api\InternalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blockchain = ethereum; // string | Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc.
$network = goerli; // string | Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \"mainnet\" is the live network with actual data while networks like \"testnet\", \"goerli\" are test networks.
$address = 0x3d0b25fe09e2cd92f06ba776391a122519936e90; // string | String identifier of the address document represented in CryptoAPIs
$context = yourExampleString; // string | In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. `context` is specified by the user.
$limit = 50; // int | Defines how many items should be returned in the response per page basis.
$offset = 0; // int | The starting index of the response items, i.e. where the response should start listing the returned items.

try {
    $result = $apiInstance->listInternalTransactionsByAddress($blockchain, $network, $address, $context, $limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InternalApi->listInternalTransactionsByAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blockchain** | **string**| Represents the specific blockchain protocol name, e.g. Ethereum, Bitcoin, etc. | |
| **network** | **string**| Represents the name of the blockchain network used; blockchain networks are usually identical as technology and software, but they differ in data, e.g. - \&quot;mainnet\&quot; is the live network with actual data while networks like \&quot;testnet\&quot;, \&quot;goerli\&quot; are test networks. | |
| **address** | **string**| String identifier of the address document represented in CryptoAPIs | |
| **context** | **string**| In batch situations the user can use the context to correlate responses with requests. This property is present regardless of whether the response was successful or returned as an error. &#x60;context&#x60; is specified by the user. | [optional] |
| **limit** | **int**| Defines how many items should be returned in the response per page basis. | [optional] [default to 50] |
| **offset** | **int**| The starting index of the response items, i.e. where the response should start listing the returned items. | [optional] [default to 0] |

### Return type

[**\com.cryptoapis.rest_apis.sdk\Model\ListInternalTransactionsByAddressR**](../Model/ListInternalTransactionsByAddressR.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
