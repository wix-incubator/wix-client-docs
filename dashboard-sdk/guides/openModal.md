# openModal

Opens a modal.

This function returns an object containing a promise that resolves when the modal is closed. The object that the promise resolves to contains
any data passed to the [closeModal](closeModal.md) function used to close the modal.


## Syntax

```ts
openModal(componentId, componentParams): Object
```

## Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `componentId` | string | ID of the component to show in the modal. |
| `componentParams` | Record<string, any\> | Optional. Custom data to pass into the component. |


## Returns
```
Object
```
## Examples

[How to create a dashboard sdk instance?](Intro.md#usage)

**Open a modal and log the data returned when it's closed**

```ts
const { modalClosed } = wix.dashboard.openModal('my-component-id');
modalClosed.then((result) => {
  console.log('The modal was closed and returned the value:', result);
});
```