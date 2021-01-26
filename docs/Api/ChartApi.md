# OpenAPI\Client\ChartApi

All URIs are relative to http://localhost.

Method | HTTP request | Description
------------- | ------------- | -------------
[**getChart()**](ChartApi.md#getChart) | **GET** /chart/{symbol}/{interval} | Get candle chart


## `getChart()`

```php
getChart($symbol, $interval): \OpenAPI\Client\Model\Ohlcv[]
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
$symbol = 'symbol_example'; // string | symbol name
$interval = 'interval_example'; // string | symbol name

try {
    $result = $apiInstance->getChart($symbol, $interval);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChartApi->getChart: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| symbol name |
 **interval** | **string**| symbol name |

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
