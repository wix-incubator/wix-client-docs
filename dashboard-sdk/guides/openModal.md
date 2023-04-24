# openModal

Opens a modal.

This function returns a promise that resolves when the modal is closed. The object that the promise resolves to contains
any data passed to the [closeModal](closeModal.md) function used to close the modal.


## Syntax

```ts
openModal(componentId, componentParams): Promise<Object>
```

## Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `componentId` | string | ID of the component to show in the modal. |
| `componentParams` | Record<string, any\> | Optional. Custom data to pass into the component. |


## Returns
```
Promise<Object>
```
## Examples

**Open a modal and log the data returned when it's closed**

```ts
import { openModal } from '@wix/dashboard-sdk';

const { modalClosed } = await openModal('my-component-id');
modalClosed.then((result) => {
  console.log('The modal was closed and returned the value:', result);
});
```