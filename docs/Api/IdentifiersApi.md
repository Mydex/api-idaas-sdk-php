# Mydex\ApiIdaasSdk\IdentifiersApi

Endpoints for managing member identifiers and invitations

All URIs are relative to https://idp.mydexid.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getIdentifierInvite()**](IdentifiersApi.md#getIdentifierInvite) | **GET** /members/invite/{invite} | Fetch an invitation code and identifier auth data. |
| [**patchNotifyStatus()**](IdentifiersApi.md#patchNotifyStatus) | **PATCH** /members/notify/status | Update the status of a notification. |
| [**postInviteStatus()**](IdentifiersApi.md#postInviteStatus) | **POST** /members/invite/status | Check the status of an invite. |
| [**postNotifyMemberViaIdentifier()**](IdentifiersApi.md#postNotifyMemberViaIdentifier) | **POST** /members/notify | Send a notification to a member via its identifier. |
| [**postStoreAndSendIdentifierInvite()**](IdentifiersApi.md#postStoreAndSendIdentifierInvite) | **POST** /members/invite | Store an invitation code and send notification. |


## `getIdentifierInvite()`

```php
getIdentifierInvite($invite): \Mydex\ApiIdaasSdk\Model\GetInviteResponse
```

Fetch an invitation code and identifier auth data.

Retrieves the invitation data for a given invite code.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiIdaasSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiIdaasSdk\Api\IdentifiersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invite = a1b2c3d4e5f6; // string | The invitation code

try {
    $result = $apiInstance->getIdentifierInvite($invite);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentifiersApi->getIdentifierInvite: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invite** | **string**| The invitation code | |

### Return type

[**\Mydex\ApiIdaasSdk\Model\GetInviteResponse**](../Model/GetInviteResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchNotifyStatus()`

```php
patchNotifyStatus($update_notification_status_request_body): \Mydex\ApiIdaasSdk\Model\CreateIdentifierResponse
```

Update the status of a notification.

Updates the status of a notification identifier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiIdaasSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiIdaasSdk\Api\IdentifiersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$update_notification_status_request_body = new \Mydex\ApiIdaasSdk\Model\UpdateNotificationStatusRequestBody(); // \Mydex\ApiIdaasSdk\Model\UpdateNotificationStatusRequestBody

try {
    $result = $apiInstance->patchNotifyStatus($update_notification_status_request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentifiersApi->patchNotifyStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **update_notification_status_request_body** | [**\Mydex\ApiIdaasSdk\Model\UpdateNotificationStatusRequestBody**](../Model/UpdateNotificationStatusRequestBody.md)|  | [optional] |

### Return type

[**\Mydex\ApiIdaasSdk\Model\CreateIdentifierResponse**](../Model/CreateIdentifierResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postInviteStatus()`

```php
postInviteStatus($invite_status_request_body): \Mydex\ApiIdaasSdk\Model\InviteStatusResponse
```

Check the status of an invite.

Checks the status of an invitation without modifying it.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiIdaasSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiIdaasSdk\Api\IdentifiersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invite_status_request_body = new \Mydex\ApiIdaasSdk\Model\InviteStatusRequestBody(); // \Mydex\ApiIdaasSdk\Model\InviteStatusRequestBody

try {
    $result = $apiInstance->postInviteStatus($invite_status_request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentifiersApi->postInviteStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invite_status_request_body** | [**\Mydex\ApiIdaasSdk\Model\InviteStatusRequestBody**](../Model/InviteStatusRequestBody.md)|  | [optional] |

### Return type

[**\Mydex\ApiIdaasSdk\Model\InviteStatusResponse**](../Model/InviteStatusResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postNotifyMemberViaIdentifier()`

```php
postNotifyMemberViaIdentifier($notify_member_request_body): \Mydex\ApiIdaasSdk\Model\CreateIdentifierResponse
```

Send a notification to a member via its identifier.

Sends a notification (email or SMS) to a member using their identifier for authentication.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiIdaasSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiIdaasSdk\Api\IdentifiersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$notify_member_request_body = new \Mydex\ApiIdaasSdk\Model\NotifyMemberRequestBody(); // \Mydex\ApiIdaasSdk\Model\NotifyMemberRequestBody

try {
    $result = $apiInstance->postNotifyMemberViaIdentifier($notify_member_request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentifiersApi->postNotifyMemberViaIdentifier: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **notify_member_request_body** | [**\Mydex\ApiIdaasSdk\Model\NotifyMemberRequestBody**](../Model/NotifyMemberRequestBody.md)|  | [optional] |

### Return type

[**\Mydex\ApiIdaasSdk\Model\CreateIdentifierResponse**](../Model/CreateIdentifierResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postStoreAndSendIdentifierInvite()`

```php
postStoreAndSendIdentifierInvite($invite_request_body): \Mydex\ApiIdaasSdk\Model\GetInviteResponse
```

Store an invitation code and send notification.

Stores an invitation code and sends an invitation to the member via their identifier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiIdaasSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiIdaasSdk\Api\IdentifiersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invite_request_body = new \Mydex\ApiIdaasSdk\Model\InviteRequestBody(); // \Mydex\ApiIdaasSdk\Model\InviteRequestBody

try {
    $result = $apiInstance->postStoreAndSendIdentifierInvite($invite_request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentifiersApi->postStoreAndSendIdentifierInvite: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invite_request_body** | [**\Mydex\ApiIdaasSdk\Model\InviteRequestBody**](../Model/InviteRequestBody.md)|  | [optional] |

### Return type

[**\Mydex\ApiIdaasSdk\Model\GetInviteResponse**](../Model/GetInviteResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
