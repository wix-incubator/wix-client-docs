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

**Close a modal**

```ts
import { closeModal } from '@wix/dashboard-sdk';

closeModal({'message': 'The modal is closed!'});
```