# Initiate Checkout

Triggered when the ‘Checkout’ button is clicked.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|contents|array|All products in cart|  
|contents.id|text|Product ID|
|contents.name|text|Product name|
|contents.category|text|Collection name|
|contents.variant|text|Selected choice from 1st product option|
|contents.price|currency|Product price|
|contents.currency|currency|Currency in ISO-4217 format|
|contents.quantity|number|Quantity of product added to cart|
|origin|text|Wix App name, i.e Stores, Bookings |  
|isPremium|boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
{
 "contents": [{
    "id": "df19c1f7-07d8-a265-42f8-e8dfa824cc6e", 
    "name": "Soundbeam ERD - 3083", 
    "category": "All Products", 
    "price": 220, 
    "currency": "ILS", 
    "quantity": 1
  }],
  "length": 1,
  "origin": "Stores",
  "isPremium": true,
  "userId": "79f246a8-46fd-4429-aac6-006d13cce9a6",
  "metaSiteId": "e4d85293-d205-48d0-93d4-3ed7b91b9549"
}
```
