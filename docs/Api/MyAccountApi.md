# Mydex\ApiIdaasSdk\MyAccountApi

Endpoints for MyAccount integration

All URIs are relative to https://idp.mydexid.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getMydexIdFromMyAccountSvt()**](MyAccountApi.md#getMydexIdFromMyAccountSvt) | **GET** /members/myaccount/{svt} | Check if a MyAccount SVT has an associated MydexID. |


## `getMydexIdFromMyAccountSvt()`

```php
getMydexIdFromMyAccountSvt($svt): string
```

Check if a MyAccount SVT has an associated MydexID.

Retrieves the MydexID associated with a MyAccount SVT.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiIdaasSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiIdaasSdk\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$svt = abc123xyz456; // string | The MyAccount security verification token

try {
    $result = $apiInstance->getMydexIdFromMyAccountSvt($svt);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->getMydexIdFromMyAccountSvt: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **svt** | **string**| The MyAccount security verification token | |

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
