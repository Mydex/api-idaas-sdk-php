# Mydex\ApiIdaasSdk\ConnectionsApi

Endpoints for First Time Connection and identification URL setup

All URIs are relative to https://idp.mydexid.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**postFtcSetup()**](ConnectionsApi.md#postFtcSetup) | **POST** /ftc/setup | Set up a First Time Connection URL. |
| [**postIdentify()**](ConnectionsApi.md#postIdentify) | **POST** /identify | Set up an identification URL. |


## `postFtcSetup()`

```php
postFtcSetup($ftc_setup_request_body): \Mydex\ApiIdaasSdk\Model\FtcUrlResponse
```

Set up a First Time Connection URL.

Generates a one-time URL for a member to complete First Time Connection. Requires OAuth2.0 authentication.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiIdaasSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiIdaasSdk\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ftc_setup_request_body = new \Mydex\ApiIdaasSdk\Model\FtcSetupRequestBody(); // \Mydex\ApiIdaasSdk\Model\FtcSetupRequestBody

try {
    $result = $apiInstance->postFtcSetup($ftc_setup_request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->postFtcSetup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ftc_setup_request_body** | [**\Mydex\ApiIdaasSdk\Model\FtcSetupRequestBody**](../Model/FtcSetupRequestBody.md)|  | [optional] |

### Return type

[**\Mydex\ApiIdaasSdk\Model\FtcUrlResponse**](../Model/FtcUrlResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postIdentify()`

```php
postIdentify($identify_request_body): \Mydex\ApiIdaasSdk\Model\IdentifyUrlResponse
```

Set up an identification URL.

Generates a one-time URL for identifying a member without requiring them to know their MydexID. Requires OAuth2.0 authentication.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiIdaasSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiIdaasSdk\Api\ConnectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$identify_request_body = new \Mydex\ApiIdaasSdk\Model\IdentifyRequestBody(); // \Mydex\ApiIdaasSdk\Model\IdentifyRequestBody

try {
    $result = $apiInstance->postIdentify($identify_request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectionsApi->postIdentify: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **identify_request_body** | [**\Mydex\ApiIdaasSdk\Model\IdentifyRequestBody**](../Model/IdentifyRequestBody.md)|  | [optional] |

### Return type

[**\Mydex\ApiIdaasSdk\Model\IdentifyUrlResponse**](../Model/IdentifyUrlResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
