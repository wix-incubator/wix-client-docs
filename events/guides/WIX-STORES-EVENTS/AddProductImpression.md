# Add Product Impression

Triggered whenever a page is loaded that contains either a product gallery or widget.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|contents|Array|All purchased products |  
|contents.Id|text|Product ID|
|contents.name|text|Product Name|
|contents.list|text|Name of relevant product gallery|
|contents.category|text|Collection Name|
|contents.position|integer|Product position in the gallery|
|contents.price|currency|Product Price|
|contents.currency|currency|default site currency in ISO-4217 format|
|origin|text|Wix App name, i.e Stores, Bookings |  
|isPremium|Boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:  
```JSON
{
  "contents": [{
    "id": "df19c1f7-07d8-a265-42f8-e8dfa824cc6e", 
    "name": "Shoes", 
    "list": "Grid Gallery", 
    "category": "All Products", 
    "position": 0, 
    "price": 85,
    "currency": "USD"
  },
  {
    "id": "cd59cd36-b6d2-2cf3-9d48-81793a7bdbbd", 
    "name": "Reading glasses", 
    "list": "Grid Gallery", 
    "category": "All Products", 
    "position": 1,
    "price": 20,
    "currency": "USD"
  },
  {
    "id": "c8539b66-7a44-fe18-affc-afec4be8562a", 
    "name": "Watch", 
    "list": "Grid Gallery", 
    "category": "All Products", 
    "position": 2,
    "price": 10,
    "currency": "USD"
  }],
  "origin": "Stores", 
  "isPremium": true, 
  "userId": "affea1e3-8652-4b59-a3a0-e8f88fdab661", 
  "metaSiteId": "58617836-3714-4dac-860a-dd524531c13e"
}
```
