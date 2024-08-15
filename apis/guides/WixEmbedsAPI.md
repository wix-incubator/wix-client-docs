# WixEmbedsAPI
The `wixEmbedsApi` is a property of the global `window` javascript object.

Use this API in [self-hosted Embedded Script extensions](https://dev.wix.com/docs/build-apps/develop-your-app/frameworks/self-hosting/supported-extensions/site-extensions/add-an-embedded-script-extension-to-a-self-hosted-app) to interact with the site's page.

## Usage
You don't need to import `wixEmbedsApi` because it's a property of the global `window` javascript object. However, you can't immediately access it when your embedded script runs.

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

Returns an asynchronous function that returns a promise that resolves to an access token.

Use this access token to call Wix [REST APIs](https://dev.wix.com/docs/rest) and [SDKs](https://dev.wix.com/docs/sdk) in an [embedded script](https://dev.wix.com/docs/build-apps/develop-your-app/frameworks/self-hosting/supported-extensions/site-extensions/add-an-embedded-script-extension-to-a-self-hosted-app) app extension. Learn more about [authorizing API calls in self-hosted embedded script extensions](ADD-LINK-TO-KB-ARTICLE).

#### Syntax
```js
getAccessTokenFunction(): () => Promise<accessToken>
```

#### Returns
Asynchronous function that returns a promise that resolves to an access token.

#### Code sample
```js
const getAccessToken = window.wixEmbedsAPI.getAccessTokenFunction();
const accessToken = await getAccessToken();
```