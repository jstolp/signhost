# Swagger\Client\DefaultApi

All URIs are relative to *https://api.signhost.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addFile**](DefaultApi.md#addfile) | **PUT** /transaction/{transactionId}/file/{fileId}/ | Add File to the transaction
[**createTransactionExample**](DefaultApi.md#createtransactionexample) | **POST** /transaction | Create Transaction - Example
[**fileReceiptTransactionIdGet**](DefaultApi.md#filereceipttransactionidget) | **GET** /file/receipt/{transactionId} | 
[**startTransaction**](DefaultApi.md#starttransaction) | **PUT** /transaction/ | Start Transaction
[**transactionTransactionIdDelete**](DefaultApi.md#transactiontransactioniddelete) | **DELETE** /transaction/{transactionId} | Delete a transaction
[**transactionTransactionIdFileFileIdGet**](DefaultApi.md#transactiontransactionidfilefileidget) | **GET** /transaction/{transactionId}/file/{fileId}/ | 
[**transactionTransactionIdGet**](DefaultApi.md#transactiontransactionidget) | **GET** /transaction/{transactionId} | Get information about a transaction

# **addFile**
> object addFile($transaction_id, $file_id, $content_type, $application, $authorization)

Add File to the transaction

Adds a file to the transaction

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$transaction_id = "transaction_id_example"; // string | The ID the transaction add the file
$file_id = "file_id_example"; // string | Id of the file
$content_type = "content_type_example"; // string | 
$application = "application_example"; // string | 
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->addFile($transaction_id, $file_id, $content_type, $application, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->addFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transaction_id** | **string**| The ID the transaction add the file |
 **file_id** | **string**| Id of the file |
 **content_type** | **string**|  |
 **application** | **string**|  |
 **authorization** | **string**|  |

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createTransactionExample**
> object createTransactionExample($application, $authorization)

Create Transaction - Example

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$application = "application_example"; // string | 
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->createTransactionExample($application, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->createTransactionExample: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application** | **string**|  |
 **authorization** | **string**|  |

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **fileReceiptTransactionIdGet**
> fileReceiptTransactionIdGet($transaction_id, $application, $authorization)



Get the transactions receipt. *Returns the receipt when the transaction is successfully signed (Status=30)*

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$transaction_id = "transaction_id_example"; // string | The ID the transaction to GET the receipt for
$application = "application_example"; // string | 
$authorization = "authorization_example"; // string | 

try {
    $apiInstance->fileReceiptTransactionIdGet($transaction_id, $application, $authorization);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->fileReceiptTransactionIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transaction_id** | **string**| The ID the transaction to GET the receipt for |
 **application** | **string**|  |
 **authorization** | **string**|  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **startTransaction**
> object startTransaction($application, $authorization)

Start Transaction

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$application = "application_example"; // string | 
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->startTransaction($application, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->startTransaction: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application** | **string**|  |
 **authorization** | **string**|  |

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **transactionTransactionIdDelete**
> transactionTransactionIdDelete($transaction_id)

Delete a transaction

Deletes the transaction

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$transaction_id = "transaction_id_example"; // string | The ID the transaction to GET

try {
    $apiInstance->transactionTransactionIdDelete($transaction_id);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->transactionTransactionIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transaction_id** | **string**| The ID the transaction to GET |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **transactionTransactionIdFileFileIdGet**
> transactionTransactionIdFileFileIdGet($transaction_id, $file_id, $application, $authorization)



Returns the (signed) document(s).

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$transaction_id = "transaction_id_example"; // string | The ID the transaction to GET the receipt for
$file_id = "file_id_example"; // string | Id of the file
$application = "application_example"; // string | APP key
$authorization = "authorization_example"; // string | API key

try {
    $apiInstance->transactionTransactionIdFileFileIdGet($transaction_id, $file_id, $application, $authorization);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->transactionTransactionIdFileFileIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transaction_id** | **string**| The ID the transaction to GET the receipt for |
 **file_id** | **string**| Id of the file |
 **application** | **string**| APP key |
 **authorization** | **string**| API key |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **transactionTransactionIdGet**
> transactionTransactionIdGet($transaction_id)

Get information about a transaction

Get the transacton

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$transaction_id = "transaction_id_example"; // string | The ID the transaction to GET

try {
    $apiInstance->transactionTransactionIdGet($transaction_id);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->transactionTransactionIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transaction_id** | **string**| The ID the transaction to GET |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

