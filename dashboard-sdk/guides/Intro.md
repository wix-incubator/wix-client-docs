# Dashboard SDK

The [dashboard](https://support.wix.com/en/article/about-your-wix-dashboard) is a control center for Wix sites. It allows users to manage their sites' settings and business features. The dashboard also includes tools for things such as analytics, eCommerce, and marketing. Third-party apps can create custom dashboard components, including pages and widgets, that are displayed in the dashboards of users who install the apps. These components are iframe elements where 3rd-party apps can run their own code.

The Dashboard SDK is a tool that allows the code in custom dashboard components to interact with other parts of the Wix dashboard. Using the SDK, developers can navigate users to pages in the dashboard, display modals, and send users alerts and updates using toasts. The SDK makes it simpler and easier to create custom experiences for users in their sites' dashboards.

## Installation

The Dashboard SDK is a [npm package](https://www.npmjs.com/package/@wix/dashboard) written in TypeScript. You can find it in the public npm registry.

To add the Dashboard SDK to your project's dependencies, run one of the following commands:

**Install using NPM**

```bash
npm i @wix/dashboard
```

**Install using Yarn**

```bash
yarn add @wix/dashboard
```

## Usage

The SDK can be used as a module for `@wix/api-client`, so if you don't have `@wix/api-client` installed you can install it by running one of the following commands:


**Install using NPM**

```bash
npm i @wix/api-client
```

**Install using Yarn**

```bash
yarn add @wix/api-client
```

Now you should be able to create a SDK instance: 

```JS
import { createClient } from '@wix/api-client';
import { dashboard } from '@wix/dashboard';

const wix = createClient({
    auth: dashboard.auth(),
    modules: { dashboard }
});
```

You can then use `wix.dashboard` to call for dashboard methods, for example:
```JS
wix.dashboard.showToast({ message: 'Hello!' });
```

## Contact Us

If you are using one of the legacy Wix SDKs, and your code has errors, you may be using a function that's not available in the Dashboard SDK. As you work on your code, you may also realize that you need a feature that's not yet available in the SDK. In either case, please reach out to [Dashboard SDK Support](https://devforum.wix.com/kb/en/contact) for assistance.