# Click Product

Triggered when the user clicks on a event from any of the galleries.

**Properties**:
|Name|Type|Description|
|---|---|---|
|origin|text|Wix App name, i.e Events, Bookings |
|name|text|event name |
list|text|Name of relevant event gallery|
|position|number|Event position in the gallery|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("ClickProduct", {
  "origin": "Wix Events",
  "name": "Some bad event",
    "list": "Widget",
    "position": 2
} );
```
