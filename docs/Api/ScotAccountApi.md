# Mydex\ApiIdaasSdk\ScotAccountApi

Endpoints for ScotAccount integration

All URIs are relative to https://idp.mydexid.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getMydexIdFromScotAccountSub()**](ScotAccountApi.md#getMydexIdFromScotAccountSub) | **GET** /members/scotaccount/{sub} | Check if a ScotAccount sub GUID has an associated MydexID. |


## `getMydexIdFromScotAccountSub()`

```php
getMydexIdFromScotAccountSub($sub): string
```

Check if a ScotAccount sub GUID has an associated MydexID.

Retrieves the MydexID associated with a ScotAccount GUID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiIdaasSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiIdaasSdk\Api\ScotAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sub = 123e4567-e89b-12d3-a456-426614174000; // string | The ScotAccount GUID

try {
    $result = $apiInstance->getMydexIdFromScotAccountSub($sub);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScotAccountApi->getMydexIdFromScotAccountSub: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sub** | **string**| The ScotAccount GUID | |

### Return type

**string**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
