# Add Coupon

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Triggered when the user adds a coupon.

**Properties**:

|Name|Type|Description|
|---|---|---|
|eventLabel|text|Wix App name, i.e Events, Bookings|
|eventCategory|text|Wix category|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:

```JSON
trackEvent("CustomEvent", {
  "event": "AddCoupon",
    "eventLabel": "Wix Events",
   "eventCategory": "Enhanced Ecommerce",
} );
```
