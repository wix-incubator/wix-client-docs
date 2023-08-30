# showToast

> **Deprecated**:
>
> This function will continue to work, but a [newer version](https://dev.wix.com/docs/sdk/api-reference/dashboard/showToast) is available in the `@wix/dashboard` module.

Displays a toast notification.

Use the `config` parameter to:

- Control the toast's appearance.
- Set callback functions to run when the user sees or clicks on the toast.
- Create a clickable call-to-action that displays in the toast.

Requests to display toasts may be queued and the toast may not be displayed immediately.

> **Note:** When the `timeout` parameter is set to `none` the toast is rendered into the page layout and pushes the rest of the page down. When `timeout` is set to `normal`, the toast appears on top of other content on the page.

## Syntax

```ts
showToast(config): Promise<Object>
```

## Parameters

| Name     | Type                               | Description                  |
| :------- | :--------------------------------- | :--------------------------- |
| `config` | [ToastConfig](#toastconfig-object) | Toast configuration options. |

#### ToastConfig Object

| Name           | Type                        | Description                                                                                                                                                                                                     |
| :------------- | :-------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `action`       | [ToastAction](#toastaction) | Optional. Object representing a call-to-action that's displayed in the toast.                                                                                                                                   |
| `message`      | string                      | Text that appears in the toast.                                                                                                                                                                                 |
| `onCloseClick` | Function                    | Optional. Callback function to run when the toast is closed by clicking its close button.                                                                                                                       |
| `onToastSeen`  | Function                    | Optional. Callback function to run when the toast is seen by the user.                                                                                                                                          |
| `priority`     | ToastPriority               | Priority of the toast. If several toasts are triggered at the same time, they're displayed in the order of their priority levels. Default: `normal`. <br>Options: `low`, `normal`, `high`.                      |
| `timeout`      | ToastTimeout                | Whether the toast removes itself or not. <br>Options: `none`, `normal`.                                                                                                                                         |
| `type`         | ToastType                   | Toast color and message type. Default: `standard`. <br>Options: <br>`standard`: Blue notification toast. <br>`success`: Green success toast. <br>`warning`: Yellow warning toast. <br>`error`: Red error toast. |

#### ToastAction Object

| Name                 | Type              | Description                                                      |
| :------------------- | :---------------- | :--------------------------------------------------------------- |
| `onClick`            | Function          | Callback function to run after the call-to-action is clicked.    |
| `removeToastOnClick` | boolean           | Whether to remove the toast after the call-to-action is clicked. |
| `text`               | string            | Text that appears in the call-to-action.                         |
| `uiType`             | ToastActionUiType | The type of call-to-action. Options: `button`, `link`            |

## Returns

```
Promise<Object>
```

The object returned by `showToast` contains a function that can be used to remove the toast.

## Examples

**Display a success toast when a product is updated**

```ts
import { showToast } from '@wix/dashboard-sdk';

showToast({
  message: 'Product updated successfully!',
  type: 'success',
});
```

**Display an error toast with a 'Learn more' link**

```ts
import { showToast } from '@wix/dashboard-sdk';

const toastConfig = {
  message: 'Product update failed.',
  timeout: 'none',
  type: 'error',
  priority: 'low',
  action: {
    uiType: 'link',
    text: 'Learn more',
    removeToastOnClick: true,
    onClick: () => {
      // Logic to run when the user clicks the 'Learn more' link.
      console.log('Learn more clicked!')'
    }
  }
}

showToast(toastConfig);
```

**Remove a displayed toast**

```ts
import { showToast } from '@wix/dashboard-sdk';

// Display a toast and save the remove function.
const { remove } = await showToast({
  message: 'Product updated successfully!',
  type: 'success',
  timeout: 'none',
});

// Remove the toast.
remove();
```
