# OpenAPIClient-php

Description


## Installation & Usage

### Requirements

PHP 7.2 and later .

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/dav1d8/next-trader-live-data-php-api.git"
    }
  ],
  "require": {
    "dav1d8/next-trader-live-data-php-api": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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
    $apiInstance->getChart($symbol, $interval);
} catch (Exception $e) {
    echo 'Exception when calling ChartApi->getChart: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *http://localhost/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ChartApi* | [**getChart**](docs/Api/ChartApi.md#getchart) | **GET** /chart/{symbol}/{interval} | Get candle chart

## Models


## Authorization
All endpoints do not require authorization.
## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
