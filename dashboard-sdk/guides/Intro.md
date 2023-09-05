# Dashboard SDK

> **Deprecated**:
>
> The `@wix/dashboard-sdk` module has been replaced by [`@wix/dashboard`](https://dev.wix.com/docs/sdk/api-reference/dashboard/introduction).
>
> If you're already using this module in your code, it will continue to work.
> To stay compatible with future changes, update your code to use `@wix/dashboard`.

The [dashboard](https://support.wix.com/en/article/about-your-wix-dashboard) is a control center for Wix sites. It allows users to manage their sites' settings and business features. The dashboard also includes tools for things such as analytics, eCommerce, and marketing. Third-party apps can create custom dashboard components, including pages and widgets, that are displayed in the dashboards of users who install the apps. These components are iframe elements where 3rd-party apps can run their own code.

The Dashboard SDK is a tool that allows the code in custom dashboard components to interact with other parts of the Wix dashboard. Using the SDK, developers can navigate users to pages in the dashboard, display modals, and send users alerts and updates using toasts. The SDK makes it simpler and easier to create custom experiences for users in their sites' dashboards.

## Installation

The Dashboard SDK is an [npm package](https://www.npmjs.com/package/@wix/dashboard-sdk) written in TypeScript. You can find it in the public npm registry.

To add the Dashboard SDK to your project's dependencies, run 1 of the following commands:

**Install using NPM**

```bash
npm i -S @wix/dashboard-sdk
```

**Install using Yarn**

```bash
yarn add @wix/dashboard-sdk
```

## Import

To use the Dashboard SDK in your project, import the functions using the following syntax:

```JS
import { <functionName> } from '@wix/dashboard-sdk';
```

## Contact Us

If you are using one of the legacy Wix SDKs, and your code has errors, you may be using a function that's not available in the Dashboard SDK. As you work on your code, you may also realize that you need a feature that's not yet available in the SDK. In either case, please reach out to [Dashboard SDK Support](https://devforum.wix.com/kb/en/contact) for assistance.
