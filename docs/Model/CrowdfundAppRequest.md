# # CrowdfundAppRequest

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
**enabled** | **bool** | Whether the app is enabled to be viewed by everyone | [optional]
**enforce_target_amount** | **bool** | Whether contributions over the set target amount are allowed | [optional]
**start_date** | **float** | UNIX timestamp for crowdfund start time (https://www.unixtimestamp.com/) | [optional]
**end_date** | **float** | UNIX timestamp for crowdfund end time (https://www.unixtimestamp.com/) | [optional]
**target_currency** | **string** | Target currency for the crowdfund | [optional]
**target_amount** | **float** | Target amount for the crowdfund | [optional]
**main_image_url** | **string** | URL for image used as a cover image for the app | [optional]
**notification_url** | **string** | Callback notification url to POST to once when invoice is paid for and once when there are enough blockchain confirmations | [optional]
**tagline** | **string** | Tagline for the app displayed to user | [optional]
**disqus_enabled** | **bool** | Whether Disqus is enabled for the app | [optional]
**disqus_shortname** | **string** | Disqus shortname to used for the app | [optional]
**sounds_enabled** | **bool** | Whether sounds on new contributions are enabled | [optional]
**animations_enabled** | **bool** | Whether background animations on new contributions are enabled | [optional]
**reset_every_amount** | **float** | Contribution goal reset frequency amount | [optional]
**reset_every** | **string** | Contribution goal reset frequency | [optional]
**display_perks_value** | **bool** | Whether perk values are displayed | [optional]
**sort_perks_by_popularity** | **bool** | Whether perks are sorted by popularity | [optional] [default to true]
**sounds** | **string[]** | Array of custom sounds which can be used on new contributions | [optional]
**animation_colors** | **string[]** | Array of custom HEX colors which can be used for background animations on new contributions | [optional]
**html_lang** | **string** | Used for SEO, the [HTML Lang](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/lang) of the page | [optional]
**html_meta_tags** | **string** | Used for SEO, the [Meta tags](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta) of the page | [optional]
**form_id** | **string** | Form ID to request customer data | [optional]
**perks_template** | **string** | JSON of perks available in the app | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
