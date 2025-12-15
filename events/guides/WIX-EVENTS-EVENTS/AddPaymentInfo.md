# Add Payment Info

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Triggered after the user adds their payment information.

**Properties**:

|Name|Type|Description|
|---|---|---|
|origin|text|Wix App name, i.e Stores, Bookings|
|option|text|Additional information to send with Extended Ecommerce checkout step|

**Example**:

```JSON
trackEvent("AddPaymentInfo", {
  "origin": "Wix Events",
  "option": "Paypal"
} );
```
