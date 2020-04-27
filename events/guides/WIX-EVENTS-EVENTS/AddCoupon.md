# Add Coupon

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
