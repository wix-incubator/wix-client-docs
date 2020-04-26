# RSVP Click

Triggered when the user clicks "Register now".

**Properties**:
|Name|Type|Description|
|---|---|---|
|event|text|Event name|
|eventLabel|text|Wix App name, i.e Events, Bookings|
|eventCategory|text|Wix category|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("CustomEvent", {
  "event": "Name:rsvpClick",
  "eventLabel": "Wix Events",
  "eventCategory" : "Enhanced Ecommerce"
} );
```
