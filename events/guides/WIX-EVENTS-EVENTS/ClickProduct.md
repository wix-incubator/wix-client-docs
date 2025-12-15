# Click Product

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

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
