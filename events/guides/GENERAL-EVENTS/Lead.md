# Lead

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Triggered when a form is submitted.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|label|text|Form label|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
{
    "label": "Page Name: Form",
    "isPremium": true,
    "userId": "affea1e3-8652-4b59-a3a0-e8f88fdab661",
    "metaSiteId": "58617836-3714-4dac-860a-dd524531c13e"
}
```
