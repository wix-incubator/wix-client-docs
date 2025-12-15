# View Content

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Triggered whenever site content is viewed.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|origin|text|Wix App name, i.e stores, bookings |
|id|text|Product ID|
|name|text|Product name|
|category|text|Collection name|
|price|currency|Product price|
|currency|currency|Default site currency in ISO-4217 format|
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
