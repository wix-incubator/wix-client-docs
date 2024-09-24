# Wix Embeds
Use the `wixEmbedsAPI` in [self-hosted Embedded Script extensions](https://dev.wix.com/docs/build-apps/develop-your-app/frameworks/self-hosting/supported-extensions/site-extensions/add-an-embedded-script-extension-to-a-self-hosted-app) to interact with a site's pages.

## Usage
You don't need to import `wixEmbedsAPI` because it's a property of the global JavaScript `window` object. However, you can't immediately access it when your embedded script runs.

Therefore, you should add an event listener that listens for the `wixEmbedsAPIReady` event.

For example:
```js
if (window.wixEmbedsAPI) {
  // Run your code that calls a wixEmbedsAPI method here.
} else {
  window.addEventListener(
    "wixEmbedsAPIReady",
    () => {
      // Run your code that calls a wixEmbedsAPI method here.
    },
    false,
  );
}
```

You could also store a boolean variable that sets to `true` on `wixEmbedsAPIReady` and check the variable value before attempting to call a `wixEmbedsAPI` method.

## Methods

### getAccessTokenFunction()

Returns an asynchronous function that resolves to an access token.

Use this access token to call Wix [REST APIs](https://dev.wix.com/docs/rest) and use the Wix [JavaScript SDK](https://dev.wix.com/docs/sdk) with [site visitor](https://dev.wix.com/docs/build-apps/develop-your-app/access/about-identities#site-visitors) or [site member](https://dev.wix.com/docs/build-apps/develop-your-app/access/about-identities#site-members) authentication in an [embedded script](https://dev.wix.com/docs/build-apps/develop-your-app/frameworks/self-hosting/supported-extensions/site-extensions/add-an-embedded-script-extension-to-a-self-hosted-app) app extension. 

Learn more about [access tokens self-hosted site extensions](https://dev.wix.com/docs/build-apps/develop-your-app/frameworks/self-hosting/supported-extensions/site-extensions/access-tokens/about-access-tokens-in-self-hosted-site-extensions).

#### Syntax
```js
getAccessTokenFunction(): () => Promise<accessToken>
```

#### Returns
Asynchronous function that resolves to an access token.

#### Examples

Retrieve an access token:
```js
const getAccessToken = window.wixEmbedsAPI.getAccessTokenFunction();
const accessToken = await getAccessToken();
```