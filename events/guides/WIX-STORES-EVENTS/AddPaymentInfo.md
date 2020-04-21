# Add Payment Info

Triggered after the user adds their payment information.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|origin|text|Wix App name, i.e Stores, Bookings |
|option|text|Additional information to send with Extended Ecommerce checkout step|
|contents|array|All products in cart|  
|contents.Id|text|Product ID|
|contents.name|text|Product name|
|contents.category|text|Collection name|
|contents.variant|text|Selected choice from 1st product option|
|contents.price|currency|Product price|
|contents.currency|currency|Currency in ISO-4217 format|

**Example**:

```JSON
{
  "origin": "Stores",
  "option": "Express",
  "contents": [{
    "id": "T123", 
    "name": "Running shoes",
    "..."
  }]
}
```
