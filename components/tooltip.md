**[Back](components.md)**

# Tooltip

Tooltips display additional information upon hover or focus. The information included should be contextual, helpful, and nonessential while providing that extra ability to communicate and give clarity to a user.

## Usage

A tooltip is a message box displayed when a user hovers over or focuses on a UI element. A tooltip is used to provide more information and should be paired with an interactive UI element like a button. Tooltips should be used sparingly and contain succinct supplementary information.

### When to use

- To expose names of controls, like icon buttons, that lack visual labels.
- When an element can take focus and supplying additional information is useful in helping a user make decisions.
- When an element needs more context or explanation.
- Use when defining a term or inline item.

### When not to use

- Since a tooltip disappears when a user hovers away, do not include information for the user to complete their task. Use helper text that is always visible and accessible for vital information such as required fields.
- Do not include interactive elements within a tooltip. Interactive elements in tooltips are inaccessible for some users and are hard to use for all users since tooltips do not receive focus. If images, buttons, or links need to be included in supplemental information, use the toggletip component and the disclosure pattern that allows for better tabbing and focus structure, improving the experience for all users.

### Helper text versus tooltip

- Do use helper text for pertinent information.
- Do not use tooltips for information for a user to complete with a task.

### Directive text versus interactive elements

- Use succinct, directive text.
- Do not use interactive elements within a tooltip

### Variants

| Variant               | Purpose |
|:--------------------- | :------ |
| Standard Tooltip      | Provides nonessential, supplemental information to help a user make a decision but is optional to interpret and will not prevent a user from completing a task or workflow. |
| Icon Button Tooltip   | Describes a button’s function or action. |
| Definition Tooltip    | Provides additional help or defines an item or term. It may be used on the label of a UI element, or on a word embedded in a paragraph. |

### Anatomy

1. **Caret tip** - Closely associates the container with the related trigger element.
2. **Container** - Contains helper text.

### Alignment

The container of the tooltip may be aligned to start, center or end to keep the container from bleeding off the page or covering important information. The UI trigger button and caret tip should be vertically centered with each other to associate the tooltip and the trigger. This is especially helpful when multiple elements are close to each other.

### Placement

Tooltip directions, by default, are set to auto. Upon opening, tooltips can detect the edges of the browser to be placed in view, so the container does not get cutoff. Tooltips can instead use specific directions and may be positioned right, left, bottom, or top of the trigger item. Do not cover related content that is essential to the user’s tasks. Tooltips should not bleed off page or behind other content.

For tooltips that are in line with other text, like a definition tooltip, do not obstruct words to the left and right of the trigger word. When the tooltip is active, ensure it overlays other content and is not cut off by other surrounding components or bleeds off the page where some content is not visible.

### Content

- Should contain relevant, specific content.
- Should not contain essential task instructions since a tooltip is not persistent.
- Icon button tooltips should only contain one or two-word descriptions of a button’s function.
- For definitions and instructive tooltips, use sentence-style capitalization and write the text as complete sentences with punctuation unless space is limited.

### Universal behaviors

#### States

The tooltip component has two states: active and inactive. By default, the tooltip is hidden and inactive. Tooltips are displayed on hover and focus. Definition tooltips can be displayed either on hover and focus or on click and enter.

#### Mouse

Tooltips are triggered when the mouse hovers over or focuses on the UI trigger. The tooltip persists if the mouse remains over the active container or the UI trigger. The tooltip is dismissed by hovering away or moving focus to another element. The definition tooltip can be activated on click or and dismissed by clicking outside the active container or UI element.

#### Keyboard

Users can trigger a tooltip by focusing on the element. Additionally, a definition tooltip can be triggered by using the enter key. A tooltip is dismissible using the escape key. For tooltips that reveal containers on focus, the container disappears when focus moves away.

### Standard tooltip

A standard tooltip provides additional information to further assist a user in completing a task and is paired with an interactive UI element such as a button or link.

- The content within a standard tooltip should be purely additional information that is not critical for a user to read to complete a task.
- Standard tooltips appear on hover and are not focusable or read by screen readers. If the content is essential for the user to interpret concerning their workflow, use a toggletip for this information instead.

### Icon button tooltip

An icon button tooltip is used to describe the function or action of an icon button that has no label to provide clarity on what the button will do.

- Tooltip content should only contain one or two words.
- Use the icon button tooltip instead of the title attribute. Do not use both.
- It is required to not include interactive elements within a tooltip. If interactive elements are needed use a toggletip instead.

### Definition tooltip

The definition tooltip provides inline additional help or defines a term. It may be used on the label of a UI element, on a word embedded in a paragraph, or in compact spaces such as data tables where icons clutter the UI. You can use definition tooltips on headers, body copy, or labels.

The definition tooltip is unique in that if offers both a hover or click interaction depending on specific use cases. If a user needs only a few seconds to gather their information and go, use a hover interaction. If a user needs time to think about the content or the tooltip is placed so that a user can unintentionally trigger the tooltip, then a click interaction would be more appropriate.

- Tooltip content should contain brief, read-only text.
- Use on proper nouns, technical terms, or acronyms with two letters or more.

### References

- Alita Joyce, [Tooltip Guidelines](https://www.nngroup.com/articles/tooltip-guidelines/) (Nielsen Norman Group, 2019)
- MDN Web Docs,[ARIA: tooltip role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/tooltip_role) (Mozilla: Developer contributors, 2023)

## Style

Below is the token architecture color build of the components. The token can be changed or defined through the token mapping script that has been placed in the application repository.
