# # PointOfSaleAppData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Id of the app | [optional]
**app_name** | **string** | Name given to the app when it was created | [optional]
**store_id** | **string** | Id of the store to which the app belongs | [optional]
**created** | **int** | UNIX timestamp for when the app was created | [optional]
**app_type** | **string** | Type of the app which was created | [optional]
**archived** | **bool** | If true, the app does not appear in the apps list by default. | [optional] [default to false]
**title** | **string** | Display title of the app | [optional]
**description** | **string** | App description | [optional]
**default_view** | **string** | App view type (e.g., static, cart, etc...) | [optional]
**show_items** | **bool** | Display item selection for keypad | [optional] [default to false]
**show_custom_amount** | **bool** | Whether the option to enter a custom amount is shown | [optional]
**show_discount** | **bool** | Whether the option to enter a discount is shown | [optional] [default to false]
**show_search** | **bool** | Display the search bar | [optional] [default to true]
**show_categories** | **bool** | Display the list of categories | [optional] [default to true]
**enable_tips** | **bool** | Whether the option to enter a tip is shown | [optional] [default to false]
**currency** | **string** | Currency used for the app | [optional]
**fixed_amount_pay_button_text** | **string** | Payment button text template for items with a set price | [optional]
**custom_amount_pay_button_text** | **string** | Payment button text which appears for items which allow user to input a custom amount | [optional]
**tip_text** | **string** | Prompt which appears next to the tip amount field if tipping is enabled | [optional]
**custom_tip_percentages** | **float[]** | Array of predefined tip percentage amounts | [optional]
**notification_url** | **string** | Callback notification url to POST to once when invoice is paid for and once when there are enough blockchain confirmations | [optional]
**redirect_url** | **string** | URL user is redirected to once invoice is paid | [optional]
**redirect_automatically** | **bool** | Whether user is redirected to specified redirect URL automatically after the invoice is paid | [optional]
**html_lang** | **string** | Used for SEO, the [HTML Lang](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/lang) of the page | [optional]
**html_meta_tags** | **string** | Used for SEO, the [Meta tags](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta) of the page | [optional]
**form_id** | **string** | Form ID to request customer data | [optional]
**items** | [**\OpenAPI\Client\Model\AppItem[]**](AppItem.md) | JSON object of app items | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
