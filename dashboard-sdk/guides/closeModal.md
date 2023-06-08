# closeModal

Closes the currently open modal.

## Syntax

```ts
closeModal(closeData): void
```
## Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `closeData` | Serializable | Optional. Data to pass to the modal's opener. This data is returned by [openModal](openModal.md) once the modal is closed. Should not contain any functions as values. |

#### Returns

void

## Examples
[How to create a dashboard sdk instance?](Intro.md#usage)

**Close a modal**

```ts
wix.dashboard.closeModal({ message: 'The modal is closed!' });
```