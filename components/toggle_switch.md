**[Back](components.md)**

# Toggle Switch

Toggle switch is an input control that is used to quickly switch between two possible states. They are used for these binary actions that occur immediately after the user “flips the switch”. They are commonly used for “on/off” switches.

## Usage

### When to use

- Use phone fields to validate phone numbers against the correct format for the selected country.
- Set a sensible default for the country. Prefill country code based on user geolocation data.
- Allow users to modify country code when necessary. The country selector should look like an interactive element - the user should know that they can change it.

### Variants

| Variant    | Purpose |
|:---------- | :------ |
| Default Toggle Switch | Use the default toggle when you need to specify a label text in addition to the toggle action text. Default toggles appear in forms or within full pages of information. |
| Small Toggle Switch   | Use the small toggle when you do not need to specify label or action text. Small toggles are more compact in size and are used in line with other components. |

### Content

#### Label

Label text must accompany a toggle to further clarify the action that the toggle performs.

#### Action text

Use text to describe the binary action of toggle so that the action is clear. Action text must be three words or less and is displayed on the side of a toggle.

#### Language

Use adjectives rather than verbs to describe actions and the state of the object affected.

### Universal behaviors

Toggles have six states: on, off, focus, disabled, skeleton, and read-only.

### Default toggle

Default toggles are larger in size than small toggles. They are commonly used in forms and can appear within full pages of information that are not restricted in space. Default toggles are required to display visible label and action text.

### Small toggle

Small toggles are often used in condensed spaces and appear in line with other components or content, for example, inside table rows. Unlike the default toggle, the small toggle is more compact in size and displays a checkmark tick in the on state to ensure the toggle is still accessible without requiring visible label or action text.

### Toggle switch versus checkbox

Toggle switches are preferred when the resulting action will be instantaneously applied, without the need for further confirmation. By comparison, checkboxes represent one input in a larger flow which usually requires a final confirmation step.

## Style

Below is the token architecture color build of the components. The token can be changed or defined through the token mapping script that has been placed in the application repository.

**Unselected**

| State                      | Element                    | Property                   | Token name                 |
| :------------------------- | :------------------------- | :------------------------- | :------------------------- |
| Default                    | Container                  | Background Color           | `$field_1`                 |
|                            |                            | Border Color               | `$border_strong_1`         | 
|                            |                            | Box Shadow                 |                            | 
|                            | Label                      | Text Color                 | `$text_secondary`          |
|                            | Helper Text                | Text Color                 | `$text_secondary`          |
|                            | Value                      | Text Color                 | `$text_secondary`          |
|                            | Icon                       | Text Color                 | `$icon_secondary`          |
| Focus                      | Container                  | Background Color           | `$focus_highlight`         |
|                            |                            | Border Color               | `$focus`                   | 
|                            |                            | Box Shadow                 | `$shadow_1`                | 
|                            | Label                      | Text Color                 | `$focus`                   |
|                            | Helper Text                | Text Color                 | `$focus`                   |
|                            | Value                      | Text Color                 | `$text_primary`            |
|                            | Icon                       | Text Color                 | `$icon_primary`            |
| Disabled                   | Container                  | Background Color           | `$field_disabled_1`        |
|                            |                            | Border Color               | `$border_disabled`         | 
|                            |                            | Box Shadow                 |                            | 
|                            | Label                      | Text Color                 | `$text_disabled`           |
|                            | Helper Text                | Text Color                 | `$text_disabled`           |
|                            | Value                      | Text Color                 | `$text_disabled`           |
|                            | Icon                       | Text Color                 | `$icon_disabled`           |

**Selected**

| State                      | Element                    | Property                   | Token name                 |
| :------------------------- | :------------------------- | :------------------------- | :------------------------- |
| Default                    | Container                  | Background Color           | `$layer_selected_1`        |
|                            |                            | Border Color               |                            | 
|                            |                            | Box Shadow                 |                            | 
|                            | Label                      | Text Color                 | `$text_secondary`          |
|                            | Helper Text                | Text Color                 | `$text_secondary`          |
|                            | Value                      | Text Color                 | `$text_secondary`          |
|                            | Icon                       | Text Color                 | `$icon_on_color`           |
| Focus                      | Container                  | Background Color           | `$layer_selected_1`        |
|                            |                            | Border Color               | `$focus`                   | 
|                            |                            | Box Shadow                 | `$shadow_1`                | 
|                            | Label                      | Text Color                 | `$focus`                   |
|                            | Helper Text                | Text Color                 | `$focus`                   |
|                            | Value                      | Text Color                 | `$text_primary`            |
|                            | Icon                       | Text Color                 | `$icon_on_color`           |
| Disabled                   | Container                  | Background Color           | `$field_disabled_2`        |
|                            |                            | Border Color               | `$border_disabled`         | 
|                            |                            | Box Shadow                 |                            | 
|                            | Label                      | Text Color                 | `$text_disabled`           |
|                            | Helper Text                | Text Color                 | `$text_disabled`           |
|                            | Value                      | Text Color                 | `$text_disabled`           |
|                            | Icon                       | Text Color                 | `$icon_on_color_disabled`  |

### Typography

Toggle labels should be set in sentence case, with only the first word in a phrase and any proper nouns capitalized, and no more than three words.

| Element         | Font size | Font weight | Token name                |
| :-------------- | :-------- | :---------- | :------------------------ | 
| Label           | 10px      | 700 bold    | `$label_1_bold`           |
| Value           | 12px      | 400 regular | `$body_1_compact_regular` |
| Helper Text     | 12px      | 400 regular | `$helper_text_1_regular`  |

### Token Architecture

| Token name                     | Description                                            |
| :----------------------------- | :----------------------------------------------------- |
| `$toggle_switch_small`         | Defines height for the **small** variant.              |
| `$toggle_switch_medium`        | Defines height for the **medium** variant.             |
| `$toggle_switch_large`         | Defines height for the **large** variant.              |
| `$toggle_switch_padding`       | Defines **padding** for the component.                 |
| `$toggle_switch_margin`        | Defines **margin** for the component.                  |
| `$toggle_switch_border`        | Defines **border** weight for the accordion component. |
| `$toggle_switch_border_radius` | Defines **border radius** for the component.           |

### Structure

**Default Toggle Switch**

| Element               | Property                | Size      | Token name                    |
| :-------------------- | :---------------------- | :-------- | :---------------------------- |
| Container             | Width                   | 48px      |                               |
|                       | Height                  | 24px      |                               |
|                       | Border Radius           | 50px      | `$toggle_switch_border_radius`|
| Icon                  | Width                   | 18px      |                               |
|                       | Height                  | 18px      |                               |
|                       | Border Radius           | 100px     |                               |
| Label                 | Margin Bottom           | 2px       | `$spacing_2`                  |
| Helper Text           | Margin Top              | 2px       | `$spacing_2`                  |
| Value (Right Aligned) | Margin Left             | 8px       | `$toggle_switch_margin`       |
| Value (Left Aligned)  | Margin Right            | 8px       | `$toggle_switch_margin`       |

**Small Toggle Switch**

| Element               | Property                | Size      | Token name                    |
| :-------------------- | :---------------------- | :-------- | :---------------------------- |
| Container             | Width                   | 32px      |                               |
|                       | Height                  | 16px      |                               |
|                       | Border Radius           | 50px      | `$toggle_switch_border_radius`|
| Icon                  | Width                   | 10px      |                               |
|                       | Height                  | 10px      |                               |
|                       | Border Radius           | 100px     |                               |
| Label                 | Margin Bottom           | 2px       | `$spacing_2`                  |
| Helper Text           | Margin Top              | 2px       | `$spacing_2`                  |
| Value (Right Aligned) | Margin Left             | 8px       | `$toggle_switch_margin`       |
| Value (Left Aligned)  | Margin Right            | 8px       | `$toggle_switch_margin`       |

## Accessibility

The component bakes keyboard operation into its components, improving the experience of blind users and others who operate via keyboard. The component also incorporates other accessibility considerations, some of which are described below.

### Keyboard interaction

Each toggle is in the tab order. Pressing Enter or Space changes the toggle’s state between off and on.

### Redundant state information

The component’s default toggle uses both color and text to indicate on or off. Where space constraints make a smaller toggle desirable, the component adds a tick mark to the toggles “on” state so that if the text is not included, the component’s on/off state can be distinguished without relying on use of color. The state is also captured programmatically for users who cannot see or understand the visual indicators.

- Do include the on/off text for the toggle's state whenever space permits.
- Where space is confined, use the tick mark variation in lieu of on/off text.

### Do not change the toggle’s label based on its state

It is essential that designers distinguish between the text indicating the on/off state of the toggle and the text that is the toggle’s label. The label’s text should not change based on the on/off state.

- Do keep the label consistent. Only change the state text between On and Off.
- Do not change the label text as a way of indicating the toggle's on/off state.

### Development considerations

Keep this in mind if you’re modifying the component or creating a custom component.
 
- Toggle is implemented as a button with a role of switch.
- “On” and “off” text is aria-hidden; the state of the toggle is surfaced with aria-checked set to “true” or “false”.
- The toggle’s label is set with for
- See the [ARIA authoring practices guidance on switch](https://w3c.github.io/aria-practices/#switch) for more considerations.




