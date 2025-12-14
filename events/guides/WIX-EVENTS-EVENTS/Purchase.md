# Purchase

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Triggered on thank-you-page load.

**Properties**:

|Name|Type|Description|
|---|---|---|
|origin|text|Wix App name, i.e Events, Stores|
|revenue|number|Total purchase amount|
|tax|number|Purchase tax|
|coupon|text|Coupon name|
|contents|array|All purchased products/events|
|contents.quantity|number|Number of tickets|
|contents.price|number|Product/event price|
|contents.currency|currency|Currency in ISO-4217 format|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|


**Example**:

```JSON
trackEvent("Purchase", {
  "origin": "Wix Events",
  "revenue": 880,
  "tax": 20,
  "coupon": "SUMMER2018",
  "contents": [ {
    "quantity": 2,
    "price": 180,
    "currency": "USD"
  }, 
  {
    "quantity": 4,
    "price": 130,
    "currency": "USD"
  } ]
} );
```
