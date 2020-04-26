# Add Assigned

Triggered when the more than 1 ticket is selected.

**Properties**:
|Name|Type|Description|
|---|---|---|
|event|test|event name|
|eventCategory|text|Wix category|
|eventLabel|text|Wix App name, i.e Events, Bookings|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("CustomEvent", {
  "event": "AddAssigned",
    "eventLabel": "Wix Events",
    "eventCategory" : "Enhanced Ecommerce"
} );
```
