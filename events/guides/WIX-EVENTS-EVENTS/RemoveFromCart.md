# Remove From Cart

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Triggered when the user clicks to remove a ticket from the cart.

**Properties**:

|Name|Type|Description|
|---|---|---|
|origin|text|Wix App name, i.e Events, Bookings |
|name|text|Event name |
|price|number|Ticket price|
|currency|currency|Currency in ISO-4217 format|
|variant|text|Ticket type|
|position|number|Event position in the gallery|
|quantity|number|Number of tickets added|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:

```JSON
trackEvent("RemoveFromCart", {
  "origin": "Wix Events",
  "name": "Some bad event",
  "price": 130,
  "currency": "USD",
  "variant": "regular",
  "position": 2,
  "quantity": 1 
} );
```
