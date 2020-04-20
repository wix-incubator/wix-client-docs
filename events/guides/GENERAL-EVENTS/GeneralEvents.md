## Page View

Triggered whenever a site page is opened.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|pageId|text|Page ID|
|pageNumber|integer|Page Number|
|pagePath|text|Page Path|
|pageTitle|text|Page Title|
|isPremium|Boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
{
    "isPremium": true,
    "metaSiteId": "e4d85293-d205-48d0-93d4-3ed7b91b9549",
    "pageId": "c1dmp",
    "pageNumber": 4,
    "pagePath": "",
    "pageTitle": "Headphones LP",
    "userId": "79f246a8-46fd-4429-aac6-006d13cce9a6"
}
```

## View Content

Triggered whenever site content is viewed.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|origin|text|Wix App name, i.e stores, bookings |
|id|text|Product ID|
|name|text|Product Name|
|category|text|Collection Name|
|price|currency|Product price|
|currency|currency|default site currency in ISO-4217 format|
|sku|text|Product SKU|
|type|text|Product type: physical or digital|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
{
    "category": "All Products",
    "origin": "Stores",
    "id": "df19c1f7-07d8-a265-42f8-e8dfa824cc6e",
    "name": "Soundbeam ERD - 3083",
    "price": 220,
    "currency": "ILS",
    "type": "physical",
    "sku": "00001",
    "isPremium": true,
    "userId": "79f246a8-46fd-4429-aac6-006d13cce9a6",
    "metaSiteId": "e4d85293-d205-48d0-93d4-3ed7b91b9549"      
}
```

## Lead

Triggered when a form is submitted.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|label|text|Form label|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
{
    "label": "Page Name: Form",
    "isPremium": true,
    "userId": "affea1e3-8652-4b59-a3a0-e8f88fdab661",
    "metaSiteId": "58617836-3714-4dac-860a-dd524531c13e"
}
```
