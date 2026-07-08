# OpenAPIClient-php

Identity as a Service API for member authentication, identifiers, and account management.


## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
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

## API Endpoints

All URIs are relative to *https://idp.mydexid.org*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ConnectionsApi* | [**postFtcSetup**](docs/Api/ConnectionsApi.md#postftcsetup) | **POST** /ftc/setup | Set up a First Time Connection URL.
*ConnectionsApi* | [**postIdentify**](docs/Api/ConnectionsApi.md#postidentify) | **POST** /identify | Set up an identification URL.
*IdentifiersApi* | [**getIdentifierInvite**](docs/Api/IdentifiersApi.md#getidentifierinvite) | **GET** /members/invite/{invite} | Fetch an invitation code and identifier auth data.
*IdentifiersApi* | [**patchNotifyStatus**](docs/Api/IdentifiersApi.md#patchnotifystatus) | **PATCH** /members/notify/status | Update the status of a notification.
*IdentifiersApi* | [**postInviteStatus**](docs/Api/IdentifiersApi.md#postinvitestatus) | **POST** /members/invite/status | Check the status of an invite.
*IdentifiersApi* | [**postNotifyMemberViaIdentifier**](docs/Api/IdentifiersApi.md#postnotifymemberviaidentifier) | **POST** /members/notify | Send a notification to a member via its identifier.
*IdentifiersApi* | [**postStoreAndSendIdentifierInvite**](docs/Api/IdentifiersApi.md#poststoreandsendidentifierinvite) | **POST** /members/invite | Store an invitation code and send notification.
*MyAccountApi* | [**getMydexIdFromMyAccountSvt**](docs/Api/MyAccountApi.md#getmydexidfrommyaccountsvt) | **GET** /members/myaccount/{svt} | Check if a MyAccount SVT has an associated MydexID.
*ScotAccountApi* | [**getMydexIdFromScotAccountSub**](docs/Api/ScotAccountApi.md#getmydexidfromscotaccountsub) | **GET** /members/scotaccount/{sub} | Check if a ScotAccount sub GUID has an associated MydexID.

## Models

- [AuthErrorResponse](docs/Model/AuthErrorResponse.md)
- [AuthErrorResponseError](docs/Model/AuthErrorResponseError.md)
- [CreateIdentifierResponse](docs/Model/CreateIdentifierResponse.md)
- [ErrorResponse](docs/Model/ErrorResponse.md)
- [FtcIdentifyUrlResponse](docs/Model/FtcIdentifyUrlResponse.md)
- [FtcSetupRequestBody](docs/Model/FtcSetupRequestBody.md)
- [FtcUrlResponse](docs/Model/FtcUrlResponse.md)
- [GetIdentifiersResponse](docs/Model/GetIdentifiersResponse.md)
- [GetInviteResponse](docs/Model/GetInviteResponse.md)
- [IdentifierAuthObject](docs/Model/IdentifierAuthObject.md)
- [IdentifierObject](docs/Model/IdentifierObject.md)
- [IdentifyRequestBody](docs/Model/IdentifyRequestBody.md)
- [IdentifyUrlResponse](docs/Model/IdentifyUrlResponse.md)
- [InviteRequestBody](docs/Model/InviteRequestBody.md)
- [InviteStatusRequestBody](docs/Model/InviteStatusRequestBody.md)
- [InviteStatusResponse](docs/Model/InviteStatusResponse.md)
- [NotifyMemberRequestBody](docs/Model/NotifyMemberRequestBody.md)
- [UpdateNotificationStatusRequestBody](docs/Model/UpdateNotificationStatusRequestBody.md)

## Authorization

Authentication schemes defined for the API:
### oauth2

- **Type**: `OAuth`
- **Flow**: `application`
- **Authorization URL**: ``
- **Scopes**: 
    - **mydex:identifiers**: Access to identifiers endpoints
    - **mydex:scotaccount**: Access to ScotAccount-to-MydexID mapping
    - **mydex:myaccount**: Access to MyAccount-to-MydexID mapping
    - **mydex:pdx**: Global access scope for connections endpoints

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
    - Package version: `1.0.0`
    - Generator version: `7.23.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
