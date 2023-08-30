# observeState

> **Deprecated**:
>
> This function will continue to work, but a [newer version](https://dev.wix.com/docs/sdk/api-reference/dashboard/observeState) is available in the `@wix/dashboard` module.

Receives changes to the state of the page surrounding a dashboard component. You can use this data to dynamically update a
dashboard component's content.

The callback function passed to `observeState` is triggered when the dashboard component is initialized and every time the page is updated.

The callback function should define the following parameters:

- `state` : For receiving state data.
- `envData` : For receiving general data about the user's current environment.

The format of the `state` argument received by `observeState` depends on the page that hosts the dashboard component.

**Sample `envData` object**

```
{
  locale: 'en'
}
```

## Syntax

```ts
observeState<S>(observer: Observer<S>): void
```

## Type parameters

| Name | Type   | Description                                             |
| :--- | :----- | :------------------------------------------------------ |
| `S`  | Object | State's type, the first parameter sent to the callback. |

## Function Parameters

| Name       | Type            | Description                                                                               |
| :--------- | :-------------- | :---------------------------------------------------------------------------------------- |
| `observer` | Observer<S, T\> | Callback function for receiving state data. Receives 2 parameters, `state` and `envData`. |

## Examples

**Receive state data and log it to the console**

```ts
import { observeState } from '@wix/dashboard-sdk';

observeState<{ customStateProp: string }>((state, envData) => {
  console.log('custom prop', state.customStateProp);
  console.log('locale', envData.locale);
});
```
