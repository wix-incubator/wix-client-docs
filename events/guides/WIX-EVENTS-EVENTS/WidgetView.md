# Widget View (Event Widget/Gallery)

Triggered whenever a page is loaded that contains either an event gallery or widget.

**Properties**:

|Name|Type|Description|
|---|---|---|
|event|text|Event name |
|eventLabel|text|Wix App name, i.e Events, Bookings|
|eventCategory|text|Wix category|
|contents|array|All  events |
|contents.name|text|Event name|
|contents.list|text|Name of relevant event gallery/widget|
|position|number|Event position in the gallery/widget|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:

```JSON
trackEvent("CustomEvent", {
    "event": "widgetView",
    "eventLabel": "Wix Events",
    "eventCategory" : "Enhanced Ecommerce",
    "contents": [ {
      "name": "Some great event",
      "list": "Widget",
    "position": 1
  }, 
  {
    "name": "Some bad event",
    "list": "Widget",
    "position": 2
  } ]
} );
```
