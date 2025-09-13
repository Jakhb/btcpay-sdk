# BTCPayClient

# Introduction

The BTCPay Server Greenfield API is a REST API. Our API has predictable resource-oriented URLs, accepts form-encoded request bodies, returns JSON-encoded responses, and uses standard HTTP response codes, authentication, and verbs.

# Authentication

You can authenticate either via Basic Auth or an API key. It's recommended to use an API key for better security. You can create an API key in the BTCPay Server UI under `Account` -> `Manage Account` -> `API keys`. You can restrict the API key for one or multiple stores and for specific permissions. For testing purposes, you can give it the 'Unrestricted access' permission. On production you should limit the permissions to the actual endpoints you use, you can see the required permission on the API docs at the top of each endpoint under `AUTHORIZATIONS`.

If you want to simplify the process of creating API keys for your users, you can use the [Authorization endpoint](https://docs.btcpayserver.org/API/Greenfield/v1/#tag/Authorization) to predefine permissions and redirect your users to the BTCPay Server Authorization UI. You can find more information about this on the [API Authorization Flow docs](https://docs.btcpayserver.org/BTCPayServer/greenfield-authorization/) page.

# Usage examples

Use **Basic Auth** to read store information with cURL:
```bash
BTCPAY_INSTANCE=\"https://mainnet.demo.btcpayserver.org\"
USER=\"MyTestUser@gmail.com\"
PASSWORD=\"notverysecurepassword\"
PERMISSION=\"btcpay.store.canmodifystoresettings\"
BODY=\"$(echo \"{}\" | jq --arg \"a\" \"$PERMISSION\" '. + {permissions:[$a]}')\"

API_KEY=\"$(curl -s \\
     -H \"Content-Type: application/json\" \\
     --user \"$USER:$PASSWORD\" \\
     -X POST \\
     -d \"$BODY\" \\
     \"$BTCPAY_INSTANCE/api/v1/api-keys\" | jq -r .apiKey)\"
```


Use an **API key** to read store information with cURL:
```bash
STORE_ID=\"yourStoreId\"

curl -s \\
     -H \"Content-Type: application/json\" \\
     -H \"Authorization: token $API_KEY\" \\
     -X GET \\
     \"$BTCPAY_INSTANCE/api/v1/stores/$STORE_ID\"
```

You can find more examples on our docs for different programming languages:
- [cURL](https://docs.btcpayserver.org/Development/GreenFieldExample/)
- [Javascript/Node.Js](https://docs.btcpayserver.org/Development/GreenFieldExample-NodeJS/)
- [PHP](https://docs.btcpayserver.org/Development/GreenFieldExample-PHP/)



For more information, please visit [https://btcpayserver.org](https://btcpayserver.org).

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
require_once('/path/to/BTCPayClient/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure HTTP basic authorization: Basic
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure API key authorization: API_Key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\APIKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_keys_create_api_key_request = new \OpenAPI\Client\Model\ApiKeysCreateApiKeyRequest(); // \OpenAPI\Client\Model\ApiKeysCreateApiKeyRequest

try {
    $result = $apiInstance->apiKeysCreateApiKey($api_keys_create_api_key_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling APIKeysApi->apiKeysCreateApiKey: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*APIKeysApi* | [**apiKeysCreateApiKey**](docs/Api/APIKeysApi.md#apikeyscreateapikey) | **POST** /api/v1/api-keys | Create a new API Key
*APIKeysApi* | [**apiKeysCreateUserApiKey**](docs/Api/APIKeysApi.md#apikeyscreateuserapikey) | **POST** /api/v1/users/{idOrEmail}/api-keys | Create a new API Key for a user
*APIKeysApi* | [**apiKeysDeleteApiKey**](docs/Api/APIKeysApi.md#apikeysdeleteapikey) | **DELETE** /api/v1/api-keys/{apikey} | Revoke an API Key
*APIKeysApi* | [**apiKeysDeleteCurrentApiKey**](docs/Api/APIKeysApi.md#apikeysdeletecurrentapikey) | **DELETE** /api/v1/api-keys/current | Revoke the current API Key
*APIKeysApi* | [**apiKeysDeleteUserApiKey**](docs/Api/APIKeysApi.md#apikeysdeleteuserapikey) | **DELETE** /api/v1/users/{idOrEmail}/api-keys/{apikey} | Revoke an API Key of target user
*APIKeysApi* | [**apiKeysGetCurrentApiKey**](docs/Api/APIKeysApi.md#apikeysgetcurrentapikey) | **GET** /api/v1/api-keys/current | Get the current API Key information
*AppsApi* | [**appDeleteAppItemImage**](docs/Api/AppsApi.md#appdeleteappitemimage) | **DELETE** /api/v1/apps/{appId}/image/{fileId} | Deletes the app item image
*AppsApi* | [**appsCreateCrowdfundApp**](docs/Api/AppsApi.md#appscreatecrowdfundapp) | **POST** /api/v1/stores/{storeId}/apps/crowdfund | Create a new Crowdfund app
*AppsApi* | [**appsCreatePointOfSaleApp**](docs/Api/AppsApi.md#appscreatepointofsaleapp) | **POST** /api/v1/stores/{storeId}/apps/pos | Create a new Point of Sale app
*AppsApi* | [**appsDeleteApp**](docs/Api/AppsApi.md#appsdeleteapp) | **DELETE** /api/v1/apps/{appId} | Delete app
*AppsApi* | [**appsGetAllApps**](docs/Api/AppsApi.md#appsgetallapps) | **GET** /api/v1/apps | Get basic app data for all apps for all stores for a user
*AppsApi* | [**appsGetAllAppsForStore**](docs/Api/AppsApi.md#appsgetallappsforstore) | **GET** /api/v1/stores/{storeId}/apps | Get basic app data for all apps for a store
*AppsApi* | [**appsGetApp**](docs/Api/AppsApi.md#appsgetapp) | **GET** /api/v1/apps/{appId} | Get basic app data
*AppsApi* | [**appsGetAppSales**](docs/Api/AppsApi.md#appsgetappsales) | **GET** /api/v1/apps/{appId}/sales | Get app sales statistics
*AppsApi* | [**appsGetAppTopItems**](docs/Api/AppsApi.md#appsgetapptopitems) | **GET** /api/v1/apps/{appId}/top-items | Get app top items statistics
*AppsApi* | [**appsGetCrowdfundApp**](docs/Api/AppsApi.md#appsgetcrowdfundapp) | **GET** /api/v1/apps/crowdfund/{appId} | Get crowdfund app data
*AppsApi* | [**appsGetPointOfSaleApp**](docs/Api/AppsApi.md#appsgetpointofsaleapp) | **GET** /api/v1/apps/pos/{appId} | Get Point of Sale app data
*AppsApi* | [**appsPutPointOfSaleApp**](docs/Api/AppsApi.md#appsputpointofsaleapp) | **PUT** /api/v1/apps/pos/{appId} | Update a Point of Sale app
*AppsApi* | [**appsUploadAppItemImage**](docs/Api/AppsApi.md#appsuploadappitemimage) | **POST** /api/v1/apps/{appId}/image | Uploads an image for a app item
*AuthorizationApi* | [**apiKeysAuthorize**](docs/Api/AuthorizationApi.md#apikeysauthorize) | **GET** /api-keys/authorize | Authorize User
*CrowdfundApi* | [**appsCreateCrowdfundApp**](docs/Api/CrowdfundApi.md#appscreatecrowdfundapp) | **POST** /api/v1/stores/{storeId}/apps/crowdfund | Create a new Crowdfund app
*CrowdfundApi* | [**appsGetCrowdfundApp**](docs/Api/CrowdfundApi.md#appsgetcrowdfundapp) | **GET** /api/v1/apps/crowdfund/{appId} | Get crowdfund app data
*FilesApi* | [**filesDeleteFile**](docs/Api/FilesApi.md#filesdeletefile) | **DELETE** /api/v1/files/{fileId} | Delete file
*FilesApi* | [**filesGetFile**](docs/Api/FilesApi.md#filesgetfile) | **GET** /api/v1/files/{fileId} | Get file
*FilesApi* | [**filesGetFiles**](docs/Api/FilesApi.md#filesgetfiles) | **GET** /api/v1/files | Get all files
*FilesApi* | [**filesUploadFile**](docs/Api/FilesApi.md#filesuploadfile) | **POST** /api/v1/files | Uploads a file
*HealthApi* | [**healthGetHealth**](docs/Api/HealthApi.md#healthgethealth) | **GET** /api/v1/health | Get health status
*InvoicesApi* | [**invoicesActivatePaymentMethod**](docs/Api/InvoicesApi.md#invoicesactivatepaymentmethod) | **POST** /api/v1/stores/{storeId}/invoices/{invoiceId}/payment-methods/{paymentMethodId}/activate | Activate Payment Method
*InvoicesApi* | [**invoicesArchiveInvoice**](docs/Api/InvoicesApi.md#invoicesarchiveinvoice) | **DELETE** /api/v1/stores/{storeId}/invoices/{invoiceId} | Archive invoice
*InvoicesApi* | [**invoicesCreateInvoice**](docs/Api/InvoicesApi.md#invoicescreateinvoice) | **POST** /api/v1/stores/{storeId}/invoices | Create a new invoice
*InvoicesApi* | [**invoicesGetInvoice**](docs/Api/InvoicesApi.md#invoicesgetinvoice) | **GET** /api/v1/stores/{storeId}/invoices/{invoiceId} | Get invoice
*InvoicesApi* | [**invoicesGetInvoicePaymentMethods**](docs/Api/InvoicesApi.md#invoicesgetinvoicepaymentmethods) | **GET** /api/v1/stores/{storeId}/invoices/{invoiceId}/payment-methods | Get invoice payment methods
*InvoicesApi* | [**invoicesGetInvoiceRefundTriggerData**](docs/Api/InvoicesApi.md#invoicesgetinvoicerefundtriggerdata) | **GET** /api/v1/stores/{storeId}/invoices/{invoiceId}/refund/{paymentMethodId} | Get invoice refund trigger data
*InvoicesApi* | [**invoicesGetInvoices**](docs/Api/InvoicesApi.md#invoicesgetinvoices) | **GET** /api/v1/stores/{storeId}/invoices | Get invoices
*InvoicesApi* | [**invoicesMarkInvoiceStatus**](docs/Api/InvoicesApi.md#invoicesmarkinvoicestatus) | **POST** /api/v1/stores/{storeId}/invoices/{invoiceId}/status | Mark invoice status
*InvoicesApi* | [**invoicesRefund**](docs/Api/InvoicesApi.md#invoicesrefund) | **POST** /api/v1/stores/{storeId}/invoices/{invoiceId}/refund | Refund invoice
*InvoicesApi* | [**invoicesUnarchiveInvoice**](docs/Api/InvoicesApi.md#invoicesunarchiveinvoice) | **POST** /api/v1/stores/{storeId}/invoices/{invoiceId}/unarchive | Unarchive invoice
*InvoicesApi* | [**invoicesUpdateInvoice**](docs/Api/InvoicesApi.md#invoicesupdateinvoice) | **PUT** /api/v1/stores/{storeId}/invoices/{invoiceId} | Update invoice
*LightningAddressApi* | [**storeLightningAddressesAddOrUpdateStoreLightningAddress**](docs/Api/LightningAddressApi.md#storelightningaddressesaddorupdatestorelightningaddress) | **POST** /api/v1/stores/{storeId}/lightning-addresses/{username} | Add or update store configured lightning address
*LightningAddressApi* | [**storeLightningAddressesGetStoreLightningAddress**](docs/Api/LightningAddressApi.md#storelightningaddressesgetstorelightningaddress) | **GET** /api/v1/stores/{storeId}/lightning-addresses/{username} | Get store configured lightning address
*LightningAddressApi* | [**storeLightningAddressesGetStoreLightningAddresses**](docs/Api/LightningAddressApi.md#storelightningaddressesgetstorelightningaddresses) | **GET** /api/v1/stores/{storeId}/lightning-addresses | Get store configured lightning addresses
*LightningAddressApi* | [**storeLightningAddressesRemoveStoreLightningAddress**](docs/Api/LightningAddressApi.md#storelightningaddressesremovestorelightningaddress) | **DELETE** /api/v1/stores/{storeId}/lightning-addresses/{username} | Remove configured lightning address
*LightningInternalNodeApi* | [**internalLightningNodeApiConnectToNode**](docs/Api/LightningInternalNodeApi.md#internallightningnodeapiconnecttonode) | **POST** /api/v1/server/lightning/{cryptoCode}/connect | Connect to lightning node
*LightningInternalNodeApi* | [**internalLightningNodeApiCreateInvoice**](docs/Api/LightningInternalNodeApi.md#internallightningnodeapicreateinvoice) | **POST** /api/v1/server/lightning/{cryptoCode}/invoices | Create lightning invoice
*LightningInternalNodeApi* | [**internalLightningNodeApiGetBalance**](docs/Api/LightningInternalNodeApi.md#internallightningnodeapigetbalance) | **GET** /api/v1/server/lightning/{cryptoCode}/balance | Get node balance
*LightningInternalNodeApi* | [**internalLightningNodeApiGetChannels**](docs/Api/LightningInternalNodeApi.md#internallightningnodeapigetchannels) | **GET** /api/v1/server/lightning/{cryptoCode}/channels | Get channels
*LightningInternalNodeApi* | [**internalLightningNodeApiGetDepositAddress**](docs/Api/LightningInternalNodeApi.md#internallightningnodeapigetdepositaddress) | **POST** /api/v1/server/lightning/{cryptoCode}/address | Get deposit address
*LightningInternalNodeApi* | [**internalLightningNodeApiGetHistogram**](docs/Api/LightningInternalNodeApi.md#internallightningnodeapigethistogram) | **GET** /api/v1/server/lightning/{cryptoCode}/histogram | Get node balance histogram
*LightningInternalNodeApi* | [**internalLightningNodeApiGetInfo**](docs/Api/LightningInternalNodeApi.md#internallightningnodeapigetinfo) | **GET** /api/v1/server/lightning/{cryptoCode}/info | Get node information
*LightningInternalNodeApi* | [**internalLightningNodeApiGetInvoice**](docs/Api/LightningInternalNodeApi.md#internallightningnodeapigetinvoice) | **GET** /api/v1/server/lightning/{cryptoCode}/invoices/{id} | Get invoice
*LightningInternalNodeApi* | [**internalLightningNodeApiGetInvoices**](docs/Api/LightningInternalNodeApi.md#internallightningnodeapigetinvoices) | **GET** /api/v1/server/lightning/{cryptoCode}/invoices | Get invoices
*LightningInternalNodeApi* | [**internalLightningNodeApiGetPayment**](docs/Api/LightningInternalNodeApi.md#internallightningnodeapigetpayment) | **GET** /api/v1/server/lightning/{cryptoCode}/payments/{paymentHash} | Get payment
*LightningInternalNodeApi* | [**internalLightningNodeApiGetPayments**](docs/Api/LightningInternalNodeApi.md#internallightningnodeapigetpayments) | **GET** /api/v1/server/lightning/{cryptoCode}/payments | Get payments
*LightningInternalNodeApi* | [**internalLightningNodeApiOpenChannel**](docs/Api/LightningInternalNodeApi.md#internallightningnodeapiopenchannel) | **POST** /api/v1/server/lightning/{cryptoCode}/channels | Open channel
*LightningInternalNodeApi* | [**internalLightningNodeApiPayInvoice**](docs/Api/LightningInternalNodeApi.md#internallightningnodeapipayinvoice) | **POST** /api/v1/server/lightning/{cryptoCode}/invoices/pay | Pay Lightning Invoice
*LightningStoreApi* | [**storeLightningNodeApiConnectToNode**](docs/Api/LightningStoreApi.md#storelightningnodeapiconnecttonode) | **POST** /api/v1/stores/{storeId}/lightning/{cryptoCode}/connect | Connect to lightning node
*LightningStoreApi* | [**storeLightningNodeApiCreateInvoice**](docs/Api/LightningStoreApi.md#storelightningnodeapicreateinvoice) | **POST** /api/v1/stores/{storeId}/lightning/{cryptoCode}/invoices | Create lightning invoice
*LightningStoreApi* | [**storeLightningNodeApiGetBalance**](docs/Api/LightningStoreApi.md#storelightningnodeapigetbalance) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/balance | Get node balance
*LightningStoreApi* | [**storeLightningNodeApiGetChannels**](docs/Api/LightningStoreApi.md#storelightningnodeapigetchannels) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/channels | Get channels
*LightningStoreApi* | [**storeLightningNodeApiGetDepositAddress**](docs/Api/LightningStoreApi.md#storelightningnodeapigetdepositaddress) | **POST** /api/v1/stores/{storeId}/lightning/{cryptoCode}/address | Get deposit address
*LightningStoreApi* | [**storeLightningNodeApiGetHistogram**](docs/Api/LightningStoreApi.md#storelightningnodeapigethistogram) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/histogram | Get node balance histogram
*LightningStoreApi* | [**storeLightningNodeApiGetInfo**](docs/Api/LightningStoreApi.md#storelightningnodeapigetinfo) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/info | Get node information
*LightningStoreApi* | [**storeLightningNodeApiGetInvoice**](docs/Api/LightningStoreApi.md#storelightningnodeapigetinvoice) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/invoices/{id} | Get invoice
*LightningStoreApi* | [**storeLightningNodeApiGetInvoices**](docs/Api/LightningStoreApi.md#storelightningnodeapigetinvoices) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/invoices | Get invoices
*LightningStoreApi* | [**storeLightningNodeApiGetPayment**](docs/Api/LightningStoreApi.md#storelightningnodeapigetpayment) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/payments/{paymentHash} | Get payment
*LightningStoreApi* | [**storeLightningNodeApiGetPayments**](docs/Api/LightningStoreApi.md#storelightningnodeapigetpayments) | **GET** /api/v1/stores/{storeId}/lightning/{cryptoCode}/payments | Get payments
*LightningStoreApi* | [**storeLightningNodeApiOpenChannel**](docs/Api/LightningStoreApi.md#storelightningnodeapiopenchannel) | **POST** /api/v1/stores/{storeId}/lightning/{cryptoCode}/channels | Open channel
*LightningStoreApi* | [**storeLightningNodeApiPayInvoice**](docs/Api/LightningStoreApi.md#storelightningnodeapipayinvoice) | **POST** /api/v1/stores/{storeId}/lightning/{cryptoCode}/invoices/pay | Pay Lightning Invoice
*MiscelleneousApi* | [**getRateSources**](docs/Api/MiscelleneousApi.md#getratesources) | **GET** /misc/rate-sources | Get available rate sources
*MiscelleneousApi* | [**invoiceCheckout**](docs/Api/MiscelleneousApi.md#invoicecheckout) | **GET** /i/{invoiceId} | Invoice checkout
*MiscelleneousApi* | [**langCodes**](docs/Api/MiscelleneousApi.md#langcodes) | **GET** /misc/lang | Language codes
*MiscelleneousApi* | [**permissionsMetadata**](docs/Api/MiscelleneousApi.md#permissionsmetadata) | **GET** /misc/permissions | Permissions metadata
*NotificationsCurrentUserApi* | [**notificationsDeleteNotification**](docs/Api/NotificationsCurrentUserApi.md#notificationsdeletenotification) | **DELETE** /api/v1/users/me/notifications/{id} | Remove Notification
*NotificationsCurrentUserApi* | [**notificationsGetNotification**](docs/Api/NotificationsCurrentUserApi.md#notificationsgetnotification) | **GET** /api/v1/users/me/notifications/{id} | Get notification
*NotificationsCurrentUserApi* | [**notificationsGetNotificationSettings**](docs/Api/NotificationsCurrentUserApi.md#notificationsgetnotificationsettings) | **GET** /api/v1/users/me/notification-settings | Get notification settings
*NotificationsCurrentUserApi* | [**notificationsGetNotifications**](docs/Api/NotificationsCurrentUserApi.md#notificationsgetnotifications) | **GET** /api/v1/users/me/notifications | Get notifications
*NotificationsCurrentUserApi* | [**notificationsUpdateNotification**](docs/Api/NotificationsCurrentUserApi.md#notificationsupdatenotification) | **PUT** /api/v1/users/me/notifications/{id} | Update notification
*NotificationsCurrentUserApi* | [**notificationsUpdateNotificationSettings**](docs/Api/NotificationsCurrentUserApi.md#notificationsupdatenotificationsettings) | **PUT** /api/v1/users/me/notification-settings | Update notification settings
*PaymentRequestsApi* | [**paymentRequestsArchivePaymentRequest**](docs/Api/PaymentRequestsApi.md#paymentrequestsarchivepaymentrequest) | **DELETE** /api/v1/stores/{storeId}/payment-requests/{paymentRequestId} | Archive payment request
*PaymentRequestsApi* | [**paymentRequestsCreatePaymentRequest**](docs/Api/PaymentRequestsApi.md#paymentrequestscreatepaymentrequest) | **POST** /api/v1/stores/{storeId}/payment-requests | Create a new payment request
*PaymentRequestsApi* | [**paymentRequestsGetPaymentRequest**](docs/Api/PaymentRequestsApi.md#paymentrequestsgetpaymentrequest) | **GET** /api/v1/stores/{storeId}/payment-requests/{paymentRequestId} | Get payment request
*PaymentRequestsApi* | [**paymentRequestsGetPaymentRequests**](docs/Api/PaymentRequestsApi.md#paymentrequestsgetpaymentrequests) | **GET** /api/v1/stores/{storeId}/payment-requests | Get payment requests
*PaymentRequestsApi* | [**paymentRequestsPay**](docs/Api/PaymentRequestsApi.md#paymentrequestspay) | **POST** /api/v1/stores/{storeId}/payment-requests/{paymentRequestId}/pay | Create a new invoice for the payment request
*PaymentRequestsApi* | [**paymentRequestsUpdatePaymentRequest**](docs/Api/PaymentRequestsApi.md#paymentrequestsupdatepaymentrequest) | **PUT** /api/v1/stores/{storeId}/payment-requests/{paymentRequestId} | Update payment request
*PayoutProcessorsApi* | [**payoutProcessorsGetPayoutProcessors**](docs/Api/PayoutProcessorsApi.md#payoutprocessorsgetpayoutprocessors) | **GET** /api/v1/payout-processors | Get payout processors
*PointOfSaleApi* | [**appsGetPointOfSaleApp**](docs/Api/PointOfSaleApi.md#appsgetpointofsaleapp) | **GET** /api/v1/apps/pos/{appId} | Get Point of Sale app data
*PullPaymentsManagementApi* | [**pullPaymentsArchivePullPayment**](docs/Api/PullPaymentsManagementApi.md#pullpaymentsarchivepullpayment) | **DELETE** /api/v1/stores/{storeId}/pull-payments/{pullPaymentId} | Archive a pull payment
*PullPaymentsManagementApi* | [**pullPaymentsCreatePullPayment**](docs/Api/PullPaymentsManagementApi.md#pullpaymentscreatepullpayment) | **POST** /api/v1/stores/{storeId}/pull-payments | Create a new pull payment
*PullPaymentsManagementApi* | [**pullPaymentsGetPullPayments**](docs/Api/PullPaymentsManagementApi.md#pullpaymentsgetpullpayments) | **GET** /api/v1/stores/{storeId}/pull-payments | Get store&#39;s pull payments
*PullPaymentsPayoutPublicApi* | [**pullPaymentsGetPayout**](docs/Api/PullPaymentsPayoutPublicApi.md#pullpaymentsgetpayout) | **GET** /api/v1/pull-payments/{pullPaymentId}/payouts/{payoutId} | Get Payout
*PullPaymentsPublicApi* | [**pullPaymentsCreatePayout**](docs/Api/PullPaymentsPublicApi.md#pullpaymentscreatepayout) | **POST** /api/v1/pull-payments/{pullPaymentId}/payouts | Create Payout
*PullPaymentsPublicApi* | [**pullPaymentsGetPayout**](docs/Api/PullPaymentsPublicApi.md#pullpaymentsgetpayout) | **GET** /api/v1/pull-payments/{pullPaymentId}/payouts/{payoutId} | Get Payout
*PullPaymentsPublicApi* | [**pullPaymentsGetPayouts**](docs/Api/PullPaymentsPublicApi.md#pullpaymentsgetpayouts) | **GET** /api/v1/pull-payments/{pullPaymentId}/payouts | Get Payouts
*PullPaymentsPublicApi* | [**pullPaymentsGetPullPayment**](docs/Api/PullPaymentsPublicApi.md#pullpaymentsgetpullpayment) | **GET** /api/v1/pull-payments/{pullPaymentId} | Get Pull Payment
*PullPaymentsPublicApi* | [**pullPaymentsGetPullPaymentLNURL**](docs/Api/PullPaymentsPublicApi.md#pullpaymentsgetpullpaymentlnurl) | **GET** /api/v1/pull-payments/{pullPaymentId}/lnurl | Get Pull Payment LNURL details
*PullPaymentsPublicApi* | [**pullPaymentsLinkBoltcard**](docs/Api/PullPaymentsPublicApi.md#pullpaymentslinkboltcard) | **POST** /api/v1/pull-payments/{pullPaymentId}/boltcards | Link a boltcard to a pull payment
*ServerEmailApi* | [**serverEmailGetSettings**](docs/Api/ServerEmailApi.md#serveremailgetsettings) | **GET** /api/v1/server/email | Get server email settings
*ServerEmailApi* | [**serverEmailUpdateSettings**](docs/Api/ServerEmailApi.md#serveremailupdatesettings) | **PUT** /api/v1/server/email | Update server email settings
*ServerInfoApi* | [**serverGetStoreRoles**](docs/Api/ServerInfoApi.md#servergetstoreroles) | **GET** /api/v1/server/roles | Get store&#39;s roles
*ServerInfoApi* | [**serverInfoGetServerInfo**](docs/Api/ServerInfoApi.md#serverinfogetserverinfo) | **GET** /api/v1/server/info | Get server info
*StorePaymentMethodsApi* | [**storePaymentMethodsDeleteStorePaymentMethod**](docs/Api/StorePaymentMethodsApi.md#storepaymentmethodsdeletestorepaymentmethod) | **DELETE** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId} | Delete store&#39;s payment method
*StorePaymentMethodsApi* | [**storePaymentMethodsGetStorePaymentMethod**](docs/Api/StorePaymentMethodsApi.md#storepaymentmethodsgetstorepaymentmethod) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId} | Get store payment method
*StorePaymentMethodsApi* | [**storePaymentMethodsGetStorePaymentMethods**](docs/Api/StorePaymentMethodsApi.md#storepaymentmethodsgetstorepaymentmethods) | **GET** /api/v1/stores/{storeId}/payment-methods | Get store payment methods
*StorePaymentMethodsApi* | [**storePaymentMethodsUpdateStorePaymentMethod**](docs/Api/StorePaymentMethodsApi.md#storepaymentmethodsupdatestorepaymentmethod) | **PUT** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId} | Update store&#39;s payment method
*StoreWalletOnChainApi* | [**storeOnChainPaymentMethodsGenerateOnChainWallet**](docs/Api/StoreWalletOnChainApi.md#storeonchainpaymentmethodsgenerateonchainwallet) | **POST** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/generate | Generate store on-chain wallet
*StoreWalletOnChainApi* | [**storeOnChainPaymentMethodsGetOnChainPaymentMethodPreview**](docs/Api/StoreWalletOnChainApi.md#storeonchainpaymentmethodsgetonchainpaymentmethodpreview) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/preview | Preview store on-chain payment method addresses
*StoreWalletOnChainApi* | [**storeOnChainPaymentMethodsPOSTOnChainPaymentMethodPreview**](docs/Api/StoreWalletOnChainApi.md#storeonchainpaymentmethodspostonchainpaymentmethodpreview) | **POST** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/preview | Preview proposed store on-chain payment method addresses
*StoreWalletOnChainApi* | [**storeOnChainWalletsAddOrUpdateOnChainWalletLink**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsaddorupdateonchainwalletlink) | **POST** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/objects/{objectType}/{objectId}/links | Add/Update store on-chain wallet object link
*StoreWalletOnChainApi* | [**storeOnChainWalletsAddOrUpdateOnChainWalletObjects**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsaddorupdateonchainwalletobjects) | **POST** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/objects | Add/Update store on-chain wallet objects
*StoreWalletOnChainApi* | [**storeOnChainWalletsCreateOnChainTransaction**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletscreateonchaintransaction) | **POST** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/transactions | Create store on-chain wallet transaction
*StoreWalletOnChainApi* | [**storeOnChainWalletsGetOnChainFeeRate**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsgetonchainfeerate) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/feerate | Get store on-chain wallet fee rate
*StoreWalletOnChainApi* | [**storeOnChainWalletsGetOnChainWalletObject**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsgetonchainwalletobject) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/objects/{objectType}/{objectId} | Get store on-chain wallet object
*StoreWalletOnChainApi* | [**storeOnChainWalletsGetOnChainWalletObjects**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsgetonchainwalletobjects) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/objects | Get store on-chain wallet objects
*StoreWalletOnChainApi* | [**storeOnChainWalletsGetOnChainWalletReceiveAddress**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsgetonchainwalletreceiveaddress) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/address | Get store on-chain wallet address
*StoreWalletOnChainApi* | [**storeOnChainWalletsGetOnChainWalletTransaction**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsgetonchainwallettransaction) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/transactions/{transactionId} | Get store on-chain wallet transaction
*StoreWalletOnChainApi* | [**storeOnChainWalletsGetOnChainWalletUTXOs**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsgetonchainwalletutxos) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/utxos | Get store on-chain wallet UTXOS
*StoreWalletOnChainApi* | [**storeOnChainWalletsPatchOnChainWalletTransaction**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletspatchonchainwallettransaction) | **PATCH** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/transactions/{transactionId} | Patch store on-chain wallet transaction info
*StoreWalletOnChainApi* | [**storeOnChainWalletsRemoveOnChainWalletLink**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsremoveonchainwalletlink) | **DELETE** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/objects/{objectType}/{objectId}/links/{linkType}/{linkId} | Remove store on-chain wallet object links
*StoreWalletOnChainApi* | [**storeOnChainWalletsRemoveOnChainWalletObject**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsremoveonchainwalletobject) | **DELETE** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/objects/{objectType}/{objectId} | Remove store on-chain wallet objects
*StoreWalletOnChainApi* | [**storeOnChainWalletsShowOnChainWalletHistogram**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsshowonchainwallethistogram) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/histogram | Get store on-chain wallet balance histogram
*StoreWalletOnChainApi* | [**storeOnChainWalletsShowOnChainWalletOverview**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsshowonchainwalletoverview) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet | Get store on-chain wallet overview
*StoreWalletOnChainApi* | [**storeOnChainWalletsShowOnChainWalletTransactions**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsshowonchainwallettransactions) | **GET** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/transactions | Get store on-chain wallet transactions
*StoreWalletOnChainApi* | [**storeOnChainWalletsUnReserveOnChainWalletReceiveAddress**](docs/Api/StoreWalletOnChainApi.md#storeonchainwalletsunreserveonchainwalletreceiveaddress) | **DELETE** /api/v1/stores/{storeId}/payment-methods/{paymentMethodId}/wallet/address | UnReserve last store on-chain wallet address
*StoresApi* | [**storesCreateStore**](docs/Api/StoresApi.md#storescreatestore) | **POST** /api/v1/stores | Create a new store
*StoresApi* | [**storesDeleteStore**](docs/Api/StoresApi.md#storesdeletestore) | **DELETE** /api/v1/stores/{storeId} | Remove Store
*StoresApi* | [**storesDeleteStoreLogo**](docs/Api/StoresApi.md#storesdeletestorelogo) | **DELETE** /api/v1/stores/{storeId}/logo | Deletes the store logo
*StoresApi* | [**storesGetStore**](docs/Api/StoresApi.md#storesgetstore) | **GET** /api/v1/stores/{storeId} | Get store
*StoresApi* | [**storesGetStoreRoles**](docs/Api/StoresApi.md#storesgetstoreroles) | **GET** /api/v1/stores/{storeId}/roles | Get store&#39;s roles
*StoresApi* | [**storesGetStores**](docs/Api/StoresApi.md#storesgetstores) | **GET** /api/v1/stores | Get stores
*StoresApi* | [**storesUpdateStore**](docs/Api/StoresApi.md#storesupdatestore) | **PUT** /api/v1/stores/{storeId} | Update store
*StoresApi* | [**storesUploadStoreLogo**](docs/Api/StoresApi.md#storesuploadstorelogo) | **POST** /api/v1/stores/{storeId}/logo | Uploads a logo for the store
*StoresEmailApi* | [**storesGetStoreEmailSettings**](docs/Api/StoresEmailApi.md#storesgetstoreemailsettings) | **GET** /api/v1/stores/{storeId}/email | Get store email settings
*StoresEmailApi* | [**storesSendStoreEmail**](docs/Api/StoresEmailApi.md#storessendstoreemail) | **POST** /api/v1/stores/{storeId}/email/send | Send an email for a store
*StoresEmailApi* | [**storesUpdateStoreEmailSettings**](docs/Api/StoresEmailApi.md#storesupdatestoreemailsettings) | **PUT** /api/v1/stores/{storeId}/email | Update store email settings
*StoresPayoutProcessorsApi* | [**greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutProcessorsForPaymentMethod**](docs/Api/StoresPayoutProcessorsApi.md#greenfieldstoreautomatedlightningpayoutprocessorscontrollergetstorelightningautomatedpayoutprocessorsforpaymentmethod) | **GET** /api/v1/stores/{storeId}/payout-processors/LightningAutomatedPayoutSenderFactory/{payoutMethodId} | Get configured store Lightning automated payout processors
*StoresPayoutProcessorsApi* | [**greenfieldStoreAutomatedLightningPayoutProcessorsControllerGetStoreLightningAutomatedPayoutSenderFactory**](docs/Api/StoresPayoutProcessorsApi.md#greenfieldstoreautomatedlightningpayoutprocessorscontrollergetstorelightningautomatedpayoutsenderfactory) | **GET** /api/v1/stores/{storeId}/payout-processors/LightningAutomatedPayoutSenderFactory | Get configured store Lightning automated payout processors
*StoresPayoutProcessorsApi* | [**greenfieldStoreAutomatedLightningPayoutProcessorsControllerUpdateStoreLightningAutomatedPayoutProcessor**](docs/Api/StoresPayoutProcessorsApi.md#greenfieldstoreautomatedlightningpayoutprocessorscontrollerupdatestorelightningautomatedpayoutprocessor) | **PUT** /api/v1/stores/{storeId}/payout-processors/LightningAutomatedPayoutSenderFactory/{payoutMethodId} | Update configured store Lightning automated payout processors
*StoresPayoutProcessorsApi* | [**greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedPayoutProcessorsForPaymentMethod**](docs/Api/StoresPayoutProcessorsApi.md#greenfieldstoreautomatedonchainpayoutprocessorscontrollergetstoreonchainautomatedpayoutprocessorsforpaymentmethod) | **GET** /api/v1/stores/{storeId}/payout-processors/OnChainAutomatedPayoutSenderFactory/{paymentMethodId} | Get configured store onchain automated payout processors
*StoresPayoutProcessorsApi* | [**greenfieldStoreAutomatedOnChainPayoutProcessorsControllerGetStoreOnChainAutomatedTransferSenderFactory**](docs/Api/StoresPayoutProcessorsApi.md#greenfieldstoreautomatedonchainpayoutprocessorscontrollergetstoreonchainautomatedtransfersenderfactory) | **GET** /api/v1/stores/{storeId}/payout-processors/OnChainAutomatedTransferSenderFactory | Get configured store onchain automated payout processors
*StoresPayoutProcessorsApi* | [**greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedPayoutProcessorForPaymentMethod**](docs/Api/StoresPayoutProcessorsApi.md#greenfieldstoreautomatedonchainpayoutprocessorscontrollerupdatestoreonchainautomatedpayoutprocessorforpaymentmethod) | **PUT** /api/v1/stores/{storeId}/payout-processors/OnChainAutomatedPayoutSenderFactory/{paymentMethodId} | Update configured store onchain automated payout processors
*StoresPayoutProcessorsApi* | [**greenfieldStoreAutomatedOnChainPayoutProcessorsControllerUpdateStoreOnChainAutomatedTransferSenderFactory**](docs/Api/StoresPayoutProcessorsApi.md#greenfieldstoreautomatedonchainpayoutprocessorscontrollerupdatestoreonchainautomatedtransfersenderfactory) | **PUT** /api/v1/stores/{storeId}/payout-processors/OnChainAutomatedTransferSenderFactory | Update configured store onchain automated payout processors
*StoresPayoutProcessorsApi* | [**storePayoutProcessorsGetStorePayoutProcessors**](docs/Api/StoresPayoutProcessorsApi.md#storepayoutprocessorsgetstorepayoutprocessors) | **GET** /api/v1/stores/{storeId}/payout-processors | Get store configured payout processors
*StoresPayoutProcessorsApi* | [**storePayoutProcessorsRemoveStorePayoutProcessor**](docs/Api/StoresPayoutProcessorsApi.md#storepayoutprocessorsremovestorepayoutprocessor) | **DELETE** /api/v1/stores/{storeId}/payout-processors/{processor}/{paymentMethodId} | Remove store configured payout processor
*StoresPayoutsApi* | [**getStorePayout**](docs/Api/StoresPayoutsApi.md#getstorepayout) | **GET** /api/v1/stores/{storeId}/payouts/{payoutId} | Get Payout
*StoresPayoutsApi* | [**payoutsCreatePayoutThroughStore**](docs/Api/StoresPayoutsApi.md#payoutscreatepayoutthroughstore) | **POST** /api/v1/stores/{storeId}/payouts | Create Payout
*StoresPayoutsApi* | [**pullPaymentsApprovePayout**](docs/Api/StoresPayoutsApi.md#pullpaymentsapprovepayout) | **POST** /api/v1/stores/{storeId}/payouts/{payoutId} | Approve Payout
*StoresPayoutsApi* | [**pullPaymentsCancelPayout**](docs/Api/StoresPayoutsApi.md#pullpaymentscancelpayout) | **DELETE** /api/v1/stores/{storeId}/payouts/{payoutId} | Cancel Payout
*StoresPayoutsApi* | [**pullPaymentsGetStorePayouts**](docs/Api/StoresPayoutsApi.md#pullpaymentsgetstorepayouts) | **GET** /api/v1/stores/{storeId}/payouts | Get Store Payouts
*StoresPayoutsApi* | [**pullPaymentsMarkPayout**](docs/Api/StoresPayoutsApi.md#pullpaymentsmarkpayout) | **POST** /api/v1/stores/{storeId}/payouts/{payoutId}/mark | Mark Payout
*StoresPayoutsApi* | [**pullPaymentsMarkPayoutPaid**](docs/Api/StoresPayoutsApi.md#pullpaymentsmarkpayoutpaid) | **POST** /api/v1/stores/{storeId}/payouts/{payoutId}/mark-paid | Mark Payout as Paid
*StoresRatesApi* | [**storesGetStoreRateConfiguration**](docs/Api/StoresRatesApi.md#storesgetstorerateconfiguration) | **GET** /api/v1/stores/{storeId}/rates/configuration/{rateSource} | Get store rate settings for the specified rate source
*StoresRatesApi* | [**storesGetStoreRates**](docs/Api/StoresRatesApi.md#storesgetstorerates) | **GET** /api/v1/stores/{storeId}/rates | Get rates
*StoresRatesApi* | [**storesPreviewStoreRateConfiguration**](docs/Api/StoresRatesApi.md#storespreviewstorerateconfiguration) | **POST** /api/v1/stores/{storeId}/rates/configuration/preview | Preview rate configuration results
*StoresRatesApi* | [**storesUpdateStoreRateConfiguration**](docs/Api/StoresRatesApi.md#storesupdatestorerateconfiguration) | **PUT** /api/v1/stores/{storeId}/rates/configuration/{rateSource} | Get store rate settings for the specified rate source
*StoresUsersApi* | [**storesAddStoreUser**](docs/Api/StoresUsersApi.md#storesaddstoreuser) | **POST** /api/v1/stores/{storeId}/users | Add a store user
*StoresUsersApi* | [**storesGetStoreUsers**](docs/Api/StoresUsersApi.md#storesgetstoreusers) | **GET** /api/v1/stores/{storeId}/users | Get store users
*StoresUsersApi* | [**storesRemoveStoreUser**](docs/Api/StoresUsersApi.md#storesremovestoreuser) | **DELETE** /api/v1/stores/{storeId}/users/{idOrEmail} | Remove Store User
*StoresUsersApi* | [**storesUpdateStoreUser**](docs/Api/StoresUsersApi.md#storesupdatestoreuser) | **PUT** /api/v1/stores/{storeId}/users/{idOrEmail} | Updates a store user
*UsersApi* | [**usersCreateUser**](docs/Api/UsersApi.md#userscreateuser) | **POST** /api/v1/users | Create user
*UsersApi* | [**usersDeleteCurrentUser**](docs/Api/UsersApi.md#usersdeletecurrentuser) | **DELETE** /api/v1/users/me | Deletes user profile
*UsersApi* | [**usersDeleteCurrentUserProfilePicture**](docs/Api/UsersApi.md#usersdeletecurrentuserprofilepicture) | **DELETE** /api/v1/users/me/picture | Deletes user profile picture
*UsersApi* | [**usersDeleteUser**](docs/Api/UsersApi.md#usersdeleteuser) | **DELETE** /api/v1/users/{idOrEmail} | Delete user
*UsersApi* | [**usersGetCurrentUser**](docs/Api/UsersApi.md#usersgetcurrentuser) | **GET** /api/v1/users/me | Get current user information
*UsersApi* | [**usersGetUser**](docs/Api/UsersApi.md#usersgetuser) | **GET** /api/v1/users/{idOrEmail} | Get user by ID or Email
*UsersApi* | [**usersGetUsers**](docs/Api/UsersApi.md#usersgetusers) | **GET** /api/v1/users | Get all users
*UsersApi* | [**usersToggleUserApproval**](docs/Api/UsersApi.md#userstoggleuserapproval) | **POST** /api/v1/users/{idOrEmail}/approve | Toggle user approval
*UsersApi* | [**usersToggleUserLock**](docs/Api/UsersApi.md#userstoggleuserlock) | **POST** /api/v1/users/{idOrEmail}/lock | Toggle user lock out
*UsersApi* | [**usersUpdateCurrentUser**](docs/Api/UsersApi.md#usersupdatecurrentuser) | **PUT** /api/v1/users/me | Update current user information
*UsersApi* | [**usersUploadCurrentUserProfilePicture**](docs/Api/UsersApi.md#usersuploadcurrentuserprofilepicture) | **POST** /api/v1/users/me/picture | Uploads a profile picture for the current user
*WebhooksApi* | [**webhooksCreateWebhook**](docs/Api/WebhooksApi.md#webhookscreatewebhook) | **POST** /api/v1/stores/{storeId}/webhooks | Create a new webhook
*WebhooksApi* | [**webhooksDeleteWebhook**](docs/Api/WebhooksApi.md#webhooksdeletewebhook) | **DELETE** /api/v1/stores/{storeId}/webhooks/{webhookId} | Delete a webhook
*WebhooksApi* | [**webhooksGetWebhook**](docs/Api/WebhooksApi.md#webhooksgetwebhook) | **GET** /api/v1/stores/{storeId}/webhooks/{webhookId} | Get a webhook of a store
*WebhooksApi* | [**webhooksGetWebhookDeliveries**](docs/Api/WebhooksApi.md#webhooksgetwebhookdeliveries) | **GET** /api/v1/stores/{storeId}/webhooks/{webhookId}/deliveries | Get latest deliveries
*WebhooksApi* | [**webhooksGetWebhookDelivery**](docs/Api/WebhooksApi.md#webhooksgetwebhookdelivery) | **GET** /api/v1/stores/{storeId}/webhooks/{webhookId}/deliveries/{deliveryId} | Get a webhook delivery
*WebhooksApi* | [**webhooksGetWebhookDeliveryRequests**](docs/Api/WebhooksApi.md#webhooksgetwebhookdeliveryrequests) | **GET** /api/v1/stores/{storeId}/webhooks/{webhookId}/deliveries/{deliveryId}/request | Get the delivery&#39;s request
*WebhooksApi* | [**webhooksGetWebhooks**](docs/Api/WebhooksApi.md#webhooksgetwebhooks) | **GET** /api/v1/stores/{storeId}/webhooks | Get webhooks of a store
*WebhooksApi* | [**webhooksRedeliverWebhookDelivery**](docs/Api/WebhooksApi.md#webhooksredeliverwebhookdelivery) | **POST** /api/v1/stores/{storeId}/webhooks/{webhookId}/deliveries/{deliveryId}/redeliver | Redeliver the delivery
*WebhooksApi* | [**webhooksUpdateWebhook**](docs/Api/WebhooksApi.md#webhooksupdatewebhook) | **PUT** /api/v1/stores/{storeId}/webhooks/{webhookId} | Update a webhook

## Models

- [AddOnChainWalletObjectLinkRequest](docs/Model/AddOnChainWalletObjectLinkRequest.md)
- [ApiKeyData](docs/Model/ApiKeyData.md)
- [ApiKeysCreateApiKeyRequest](docs/Model/ApiKeysCreateApiKeyRequest.md)
- [AppBaseData](docs/Model/AppBaseData.md)
- [AppItem](docs/Model/AppItem.md)
- [AppItemStats](docs/Model/AppItemStats.md)
- [AppSalesStats](docs/Model/AppSalesStats.md)
- [AppSalesStatsItem](docs/Model/AppSalesStatsItem.md)
- [ApplicationHealthData](docs/Model/ApplicationHealthData.md)
- [ApplicationServerInfoData](docs/Model/ApplicationServerInfoData.md)
- [ApplicationServerInfoNodeStatusData](docs/Model/ApplicationServerInfoNodeStatusData.md)
- [ApplicationServerInfoSyncStatusData](docs/Model/ApplicationServerInfoSyncStatusData.md)
- [ApplicationUserData](docs/Model/ApplicationUserData.md)
- [ApproveUserRequest](docs/Model/ApproveUserRequest.md)
- [BuyerInformations](docs/Model/BuyerInformations.md)
- [CHAIN](docs/Model/CHAIN.md)
- [CheckoutOptions](docs/Model/CheckoutOptions.md)
- [ConnectToNodeRequest](docs/Model/ConnectToNodeRequest.md)
- [CreateInvoiceRequest](docs/Model/CreateInvoiceRequest.md)
- [CreateLightningInvoiceRequest](docs/Model/CreateLightningInvoiceRequest.md)
- [CreateOnChainTransactionRequest](docs/Model/CreateOnChainTransactionRequest.md)
- [CreateOnChainTransactionRequestDestination](docs/Model/CreateOnChainTransactionRequestDestination.md)
- [CreatePayoutRequest](docs/Model/CreatePayoutRequest.md)
- [CreatePayoutThroughStoreRequest](docs/Model/CreatePayoutThroughStoreRequest.md)
- [CrowdfundAppData](docs/Model/CrowdfundAppData.md)
- [CrowdfundAppRequest](docs/Model/CrowdfundAppRequest.md)
- [CrowdfundBaseData](docs/Model/CrowdfundBaseData.md)
- [EmailSettingsBase](docs/Model/EmailSettingsBase.md)
- [FileData](docs/Model/FileData.md)
- [GeneralInformation](docs/Model/GeneralInformation.md)
- [GenerateOnChainWalletRequest](docs/Model/GenerateOnChainWalletRequest.md)
- [GenericPaymentMethodData](docs/Model/GenericPaymentMethodData.md)
- [GenericPaymentMethodDataConfig](docs/Model/GenericPaymentMethodDataConfig.md)
- [GetEmailSettings](docs/Model/GetEmailSettings.md)
- [GetRateSources200ResponseInner](docs/Model/GetRateSources200ResponseInner.md)
- [GetServerEmailSettings](docs/Model/GetServerEmailSettings.md)
- [HistogramData](docs/Model/HistogramData.md)
- [InvoiceAdditionalStatus](docs/Model/InvoiceAdditionalStatus.md)
- [InvoiceData](docs/Model/InvoiceData.md)
- [InvoiceDataBase](docs/Model/InvoiceDataBase.md)
- [InvoiceMetadata](docs/Model/InvoiceMetadata.md)
- [InvoicePaymentMethodDataModel](docs/Model/InvoicePaymentMethodDataModel.md)
- [InvoicePaymentMethodDataModelAdditionalData](docs/Model/InvoicePaymentMethodDataModelAdditionalData.md)
- [InvoiceRefundTriggerData](docs/Model/InvoiceRefundTriggerData.md)
- [InvoiceStatus](docs/Model/InvoiceStatus.md)
- [InvoiceStatusMark](docs/Model/InvoiceStatusMark.md)
- [InvoiceType](docs/Model/InvoiceType.md)
- [InvoicesRefundRequest](docs/Model/InvoicesRefundRequest.md)
- [LNURL](docs/Model/LNURL.md)
- [LNURLData](docs/Model/LNURLData.md)
- [LNURLPayPaymentMethodBaseData](docs/Model/LNURLPayPaymentMethodBaseData.md)
- [LabelData](docs/Model/LabelData.md)
- [LangCodes200ResponseInner](docs/Model/LangCodes200ResponseInner.md)
- [LightningAddressData](docs/Model/LightningAddressData.md)
- [LightningAutomatedTransferSettings](docs/Model/LightningAutomatedTransferSettings.md)
- [LightningChannelData](docs/Model/LightningChannelData.md)
- [LightningInvoiceData](docs/Model/LightningInvoiceData.md)
- [LightningInvoiceStatus](docs/Model/LightningInvoiceStatus.md)
- [LightningNetworkPaymentMethodBaseData](docs/Model/LightningNetworkPaymentMethodBaseData.md)
- [LightningNodeBalanceData](docs/Model/LightningNodeBalanceData.md)
- [LightningNodeInformationData](docs/Model/LightningNodeInformationData.md)
- [LightningPaymentData](docs/Model/LightningPaymentData.md)
- [LightningPaymentStatus](docs/Model/LightningPaymentStatus.md)
- [LockUserRequest](docs/Model/LockUserRequest.md)
- [MarkInvoiceStatusRequest](docs/Model/MarkInvoiceStatusRequest.md)
- [NetworkFeeMode](docs/Model/NetworkFeeMode.md)
- [NotificationData](docs/Model/NotificationData.md)
- [NotificationSettingsData](docs/Model/NotificationSettingsData.md)
- [NotificationSettingsItemData](docs/Model/NotificationSettingsItemData.md)
- [OffchainBalanceData](docs/Model/OffchainBalanceData.md)
- [OnChainAutomatedTransferSettings](docs/Model/OnChainAutomatedTransferSettings.md)
- [OnChainPaymentMethodBaseData](docs/Model/OnChainPaymentMethodBaseData.md)
- [OnChainPaymentMethodPreviewResultAddressItem](docs/Model/OnChainPaymentMethodPreviewResultAddressItem.md)
- [OnChainPaymentMethodPreviewResultData](docs/Model/OnChainPaymentMethodPreviewResultData.md)
- [OnChainWalletAddressData](docs/Model/OnChainWalletAddressData.md)
- [OnChainWalletFeeRateData](docs/Model/OnChainWalletFeeRateData.md)
- [OnChainWalletObjectData](docs/Model/OnChainWalletObjectData.md)
- [OnChainWalletObjectId](docs/Model/OnChainWalletObjectId.md)
- [OnChainWalletObjectLink](docs/Model/OnChainWalletObjectLink.md)
- [OnChainWalletOverviewData](docs/Model/OnChainWalletOverviewData.md)
- [OnChainWalletTransactionData](docs/Model/OnChainWalletTransactionData.md)
- [OnChainWalletUTXOData](docs/Model/OnChainWalletUTXOData.md)
- [OnchainBalanceData](docs/Model/OnchainBalanceData.md)
- [OpenLightningChannelRequest](docs/Model/OpenLightningChannelRequest.md)
- [OrderInformation](docs/Model/OrderInformation.md)
- [PatchOnChainTransactionRequest](docs/Model/PatchOnChainTransactionRequest.md)
- [PayLightningInvoiceRequest](docs/Model/PayLightningInvoiceRequest.md)
- [Payment](docs/Model/Payment.md)
- [PaymentMethodCriteriaData](docs/Model/PaymentMethodCriteriaData.md)
- [PaymentRequestBaseData](docs/Model/PaymentRequestBaseData.md)
- [PaymentRequestData](docs/Model/PaymentRequestData.md)
- [PaymentRequestInformation](docs/Model/PaymentRequestInformation.md)
- [PaymentRequestsPayRequest](docs/Model/PaymentRequestsPayRequest.md)
- [PaymentStatus](docs/Model/PaymentStatus.md)
- [PayoutData](docs/Model/PayoutData.md)
- [PayoutPaymentProof](docs/Model/PayoutPaymentProof.md)
- [PayoutPaymentProofAnyOf](docs/Model/PayoutPaymentProofAnyOf.md)
- [PayoutPaymentProofAnyOf1](docs/Model/PayoutPaymentProofAnyOf1.md)
- [PayoutProcessorData](docs/Model/PayoutProcessorData.md)
- [PayoutState](docs/Model/PayoutState.md)
- [PermissionsMetadata200ResponseInner](docs/Model/PermissionsMetadata200ResponseInner.md)
- [PointOfSaleAppData](docs/Model/PointOfSaleAppData.md)
- [PointOfSaleAppRequest](docs/Model/PointOfSaleAppRequest.md)
- [PointOfSaleBaseData](docs/Model/PointOfSaleBaseData.md)
- [PointOfSaleCartView](docs/Model/PointOfSaleCartView.md)
- [ProblemDetails](docs/Model/ProblemDetails.md)
- [ProductInformation](docs/Model/ProductInformation.md)
- [PullPaymentData](docs/Model/PullPaymentData.md)
- [PullPaymentsApprovePayoutRequest](docs/Model/PullPaymentsApprovePayoutRequest.md)
- [PullPaymentsCreatePullPaymentRequest](docs/Model/PullPaymentsCreatePullPaymentRequest.md)
- [PullPaymentsLinkBoltcard200Response](docs/Model/PullPaymentsLinkBoltcard200Response.md)
- [PullPaymentsLinkBoltcardRequest](docs/Model/PullPaymentsLinkBoltcardRequest.md)
- [PullPaymentsMarkPayoutRequest](docs/Model/PullPaymentsMarkPayoutRequest.md)
- [ReceiptInformation](docs/Model/ReceiptInformation.md)
- [ReceiptOptions](docs/Model/ReceiptOptions.md)
- [RoleData](docs/Model/RoleData.md)
- [SpeedPolicy](docs/Model/SpeedPolicy.md)
- [StoreBaseData](docs/Model/StoreBaseData.md)
- [StoreData](docs/Model/StoreData.md)
- [StoreOnChainPaymentMethodsGenerateOnChainWallet200Response](docs/Model/StoreOnChainPaymentMethodsGenerateOnChainWallet200Response.md)
- [StoreOnChainPaymentMethodsPOSTOnChainPaymentMethodPreviewRequest](docs/Model/StoreOnChainPaymentMethodsPOSTOnChainPaymentMethodPreviewRequest.md)
- [StoreOnChainWalletsCreateOnChainTransaction200Response](docs/Model/StoreOnChainWalletsCreateOnChainTransaction200Response.md)
- [StoreRateConfiguration](docs/Model/StoreRateConfiguration.md)
- [StoreRateResult](docs/Model/StoreRateResult.md)
- [StoreUserData](docs/Model/StoreUserData.md)
- [StoresSendStoreEmailRequest](docs/Model/StoresSendStoreEmailRequest.md)
- [TransactionStatus](docs/Model/TransactionStatus.md)
- [UpdateEmailSettings](docs/Model/UpdateEmailSettings.md)
- [UpdateInvoiceRequest](docs/Model/UpdateInvoiceRequest.md)
- [UpdateLightningAutomatedTransferSettings](docs/Model/UpdateLightningAutomatedTransferSettings.md)
- [UpdateNotification](docs/Model/UpdateNotification.md)
- [UpdateNotificationSettingsRequest](docs/Model/UpdateNotificationSettingsRequest.md)
- [UpdateOnChainAutomatedTransferSettings](docs/Model/UpdateOnChainAutomatedTransferSettings.md)
- [UpdatePaymentMethodConfig](docs/Model/UpdatePaymentMethodConfig.md)
- [UpdatePaymentMethodConfigConfig](docs/Model/UpdatePaymentMethodConfigConfig.md)
- [UpdateServerEmailSettings](docs/Model/UpdateServerEmailSettings.md)
- [UsersCreateUserRequest](docs/Model/UsersCreateUserRequest.md)
- [UsersUpdateCurrentUserRequest](docs/Model/UsersUpdateCurrentUserRequest.md)
- [ValidationProblemDetailsInner](docs/Model/ValidationProblemDetailsInner.md)
- [WebhookData](docs/Model/WebhookData.md)
- [WebhookDataBase](docs/Model/WebhookDataBase.md)
- [WebhookDataBaseAuthorizedEvents](docs/Model/WebhookDataBaseAuthorizedEvents.md)
- [WebhookDataCreate](docs/Model/WebhookDataCreate.md)
- [WebhookDataCreateResult](docs/Model/WebhookDataCreateResult.md)
- [WebhookDataUpdate](docs/Model/WebhookDataUpdate.md)
- [WebhookDeliveryData](docs/Model/WebhookDeliveryData.md)
- [WebhookEvent](docs/Model/WebhookEvent.md)
- [WebhookInvoiceEvent](docs/Model/WebhookInvoiceEvent.md)
- [WebhookInvoiceExpiredEvent](docs/Model/WebhookInvoiceExpiredEvent.md)
- [WebhookInvoiceInvalidEvent](docs/Model/WebhookInvoiceInvalidEvent.md)
- [WebhookInvoicePaymentSettledEvent](docs/Model/WebhookInvoicePaymentSettledEvent.md)
- [WebhookInvoiceProcessingEvent](docs/Model/WebhookInvoiceProcessingEvent.md)
- [WebhookInvoiceReceivedPaymentEvent](docs/Model/WebhookInvoiceReceivedPaymentEvent.md)
- [WebhookInvoiceSettledEvent](docs/Model/WebhookInvoiceSettledEvent.md)

## Authorization

Authentication schemes defined for the API:
### API_Key

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


### Basic

- **Type**: HTTP basic authentication

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `v1`
    - Generator version: `7.16.0-SNAPSHOT`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
