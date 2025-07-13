# cloudmersive_spam_api_client
Easily and directly scan and block spam security threats in input.

[Cloudmersive Barcode API](https://cloudmersive.com/spam-detection-api) provides advanced spam detection capabilities.

- API version: v1
- Package version: 3.0.0


## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/cloudmersive/cloudmersive_spam_api_client.git"
    }
  ],
  "require": {
    "cloudmersive/cloudmersive_spam_api_client": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/cloudmersive_spam_api_client/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\SpamDetectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\SpamDetectionAdvancedRequest(); // \Swagger\Client\Model\SpamDetectionAdvancedRequest | Spam detection request

try {
    $result = $apiInstance->spamDetectTextStringAdvancedPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SpamDetectionApi->spamDetectTextStringAdvancedPost: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*SpamDetectionApi* | [**spamDetectTextStringAdvancedPost**](docs/Api/SpamDetectionApi.md#spamdetecttextstringadvancedpost) | **POST** /spam/detect/text-string/advanced | Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
*SpamDetectionApi* | [**spamDetectTextStringPost**](docs/Api/SpamDetectionApi.md#spamdetecttextstringpost) | **POST** /spam/detect/text-string | Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-75 API calls depending on model selected.


## Documentation For Models

 - [SpamDetectionAdvancedRequest](docs/Model/SpamDetectionAdvancedRequest.md)
 - [SpamDetectionAdvancedResponse](docs/Model/SpamDetectionAdvancedResponse.md)
 - [SpamDetectionRequest](docs/Model/SpamDetectionRequest.md)
 - [SpamDetectionResponse](docs/Model/SpamDetectionResponse.md)


## Documentation For Authorization


## Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header


## Author




