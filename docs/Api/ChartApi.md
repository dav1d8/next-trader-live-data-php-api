# OpenAPI\Client\ChartApi

All URIs are relative to http://localhost.

Method | HTTP request | Description
------------- | ------------- | -------------
[**getChart()**](ChartApi.md#getChart) | **GET** /chart | Get candle chart


## `getChart()`

```php
getChart($symbol, $interval, $since, $limit): \OpenAPI\Client\Model\Ohlcv[]
```

Get candle chart

Returns a candle chart

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$symbol = 'symbol_example'; // string | symbol
$interval = 'interval_example'; // string | interval
$since = 56; // int | since time
$limit = 56; // int | limit records

try {
    $result = $apiInstance->getChart($symbol, $interval, $since, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChartApi->getChart: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| symbol |
 **interval** | **string**| interval |
 **since** | **int**| since time | [optional]
 **limit** | **int**| limit records | [optional]

### Return type

[**\OpenAPI\Client\Model\Ohlcv[]**](../Model/Ohlcv.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
