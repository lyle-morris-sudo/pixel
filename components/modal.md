**[Back](components.md)**

# Modal

Modals are a variant of dialog used to present critical information or request user input needed to complete a user’s workflow. Modals interrupt a user’s workflow by design. When active, a user is blocked from the on-page content and cannot return to their previous workflow until the modal task is completed or the user dismisses the modal. While effective when used correctly, modals should be used sparingly to limit disruption to the user. 

Modal dialogs are commonly used for short and non-frequent tasks, such as editing or management tasks. If a user needs to repeatably preform a task, consider making the task do-able from the main page.

## Usage

### When to use

- **Require an immediate response from the user** - Use a dialog to request information that is preventing the system from continuing a user-initiated process.
- **Notify the user of urgent information** - Use a modal dialog to notify the user of urgent information concerning their current work. Modal dialogs are commonly used to report system errors or convey a consequence of a user’s action.
- **Confirm a user decision** - Use a modal dialog to confirm user decisions. Clearly describe the action being confirmed and explain any potential consequences that it may cause. Both the title and the button should reflect the action that will occur. If the action is destructive or irreversible then use a transactional danger modal.

### Variant

| Variant       | Purpose |
|:------------- | :------ |
| Passive       | Presents information the user needs to be aware of concerning their current workflow. Contains no actions for the user to take. |
| Transactional | Requires an action to be taken in order for the modal to be completed and closed. Contains a cancel and primary action buttons. |

### Passive modal

Passive modals presents information the user needs to be aware of concerning their current workflow. It contains no actions for the user to take and should not include any data that needs to be submitted. They serve as a type of notification alerting the user to urgent information such as reporting system errors or conveying a consequence of a user’s action.

#### Dismissing a passive modal

Passive modals are persistent until dismissed in one of the following ways.

- **X** - Clicking the close x icon in the upper right will close the modal without submitting any data and return the user to its previous context.
- **Click elsewhere** - Clicking outside the passive modal area will automatically close the modal.
- **Esc** - Press ESC on the keyboard.

### Transactional modal

Transactional modals are used to validate user decisions or to gain secondary confirmation from the user. Transactional modals require an action to be taken in order for the modal to be completed and closed. It contains a cancel and primary action buttons.

#### Dismissing a transactional modal

Transactional modals are persistent until dismissed in one of the following ways.

- **Task completion** - clicking the primary action will complete the task and automatically close the modal.
- **Cancel button** - clicking the cancel button will close the modal and return the user to its previous context. Cancel undoes all applied changes.
- **X** - Clicking the close x icon in the upper right will close the modal without submitting any data and return the user to its previous context.
- **Esc** - Press ESC on the keyboard.

### Anatomy

The modal is composed of three distinct zones: A header, the body, and a footer. Components (eg. data table, form, progress indicator) can occupy the full width of the modal.

1. **Header** - Includes a title, optional label, and the close icon.
2. **Body** - Contains the information and/or controls needed to complete the modal’s task. It can include message text and components.
3. **Footer** - Contains the main actions needed to complete or cancel the dialog task. Button groupings change based on modal variant.
4. **X** - The close x icon will close the dialog without submitting any data.
5. **Overlay** - Screen overlay that obscures the on-page content.

### Alignment

Certain components, such as a structure list or table, can expand into the margins of the modal and align flush to the container edges. These components typically have border dividers or containers extending beyond the text or icon. Labels or text of any kind should never be in the modal margins.

#### Title

- The title should be brief, using a verb plus noun combination that clearly describes the dialog’s task or purpose.
- You can use an optional label above the title to set the context for the information in the dialog.

#### Body

- A modal should include only content relevant to completing the current task.
- Text should only be 80% of the modal’s width and components can span 100% of the width.

#### Footer

- Use descriptive words for the actions such as `Add`, `Delete`, and `Save`. Avoid vague words like Done or OK. For a list of approved action labels.
- If you need to include a “docs” or other non-primary action, include it as a link in the modal’s body.

### Overflow content

When the modal content is longer than the modal height then the body section should scroll vertically with the header and footer remaining fixed in place. The content should visibly fade at the end of the modal body area to indicate there is additional content out of view.

Modal content should never scroll horizontally; instead, use a larger size modal.

### Universal behavior

#### Trigger

Modals are triggered as a result of a user’s action and are not system generated. Common components that can trigger a modal include, button, link, or icon. On a keyboard, selecting `Enter` or `Space` should launch the modal.

#### Focus

Once the modal is open, set the initial focus to the first location that accepts user input. For example, if the modal contains a form then the focus should automatically be set to the first field when opened. If it is a transactional modal without form inputs in the body section then the first focus should be on the primary button.

Focus should then remain trapped in the dialog until it is closed. When navigating by keyboard, Tab and Shift-Tab do not move the focus outside of the modal.

