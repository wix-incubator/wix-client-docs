# Initiate Checkout

Triggered when the ‘Checkout’ button is clicked.

**Properties**:

|Name|Type|Description|
|---|---|---|
|origin|text|Wix App name, i.e Events, Bookings |
|contents|array|All events in cart |
|contents.name|text|Event name|
|contents.price|number|Ticket price|
|contents.currency|currency|Currency in ISO-4217 format|
|contents.variant|text|Ticket type|
|contents.quantity|number|Number of tickets|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:

```JSON
trackEvent("InitiateCheckout", {
  "origin": "Wix Events",
  "contents": [ {
    "name": "Some bad event",
  "price": 130,
  "currency": "USD",
  "variant": "regular", 
  "quantity": 4  
  }, {
    "name": "Some great event",
  "price": 180,
  "currency": "USD",
  "variant": "vip", 
  "position": 2,
  "quantity": 2  
  } ]
} );
```
