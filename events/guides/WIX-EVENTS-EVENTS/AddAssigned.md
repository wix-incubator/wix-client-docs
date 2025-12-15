# Add Assigned

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

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
