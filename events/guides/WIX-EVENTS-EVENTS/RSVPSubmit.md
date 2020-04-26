# RSVP Submit

Triggered when the user clicks submit.

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
  "event": "Name:"RsvpSubmit",
  "eventLabel": "Wix Events",
  "eventCategory" : "Enhanced Ecommerce"
} );
```
