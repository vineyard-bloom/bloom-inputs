# ToggleSwitch

The ToggleSwitch is a hidden checkbox that appears in the UI like a sideways light switch. In the DOM, it looks either 'on' or 'off' depending on the `isActive` prop.

### Examples
#### General
```
  import { ToggleSwitch } from 'bloom-inputs'

  <ToggleSwitch
    name='notifications'
    innerLabels={{ on: 'On', off: 'Off' }}
    isActive={this.props.notifications.value}
    labelText='Email Notifications'
    onClick={(e) => this.props.toggleNotifications(e.target.value)}
  />
```

#### Bloom-Forms use
```
  import { ToggleSwitch } from 'bloom-inputs'

  const { formData, updateField } = this.props
  
  ...

  <ToggleSwitch
    name='notifications'
    innerLabels={{ on: 'On', off: 'Off' }}
    isActive={formData.notifications.value}
    labelText='Email Notifications'
    onClick={updateField}
  />
```

### Required Props
- `name`:
  A string tying the `formData` to the input's value. It should match one of the strings in `fieldNames` array passed into `<Form>`.
- `isActive`:
  A boolean that indicates if the `ToggleSwitch` is 'on' or 'off'.
- `labelText`:
  A string that labels the `ToggleSwitch`.
- `onClick`:
  A function that changes the value of the corresponding field in `formData`. Usually passed in like `manualFieldUpdate('example-form-id', 'toggle-switch-name', !formData['toggle-switch-name'].value)`

### Optional Props
- `className`:
  A string that styles the toggle switch.
- `disabled`:
  A boolean that, when true, prevents the onClick event from firing and leaves the `ToggleSwitch` in 'off' position.
- `innerLabels`:
  An object that allows you to display text for 'on' and 'off' inside the `ToggleSwitch`. An example object might look like:
```
  { on: 'true', off: 'false' }
```
- `required`:
  A boolean indicating if the input value can't be empty. HTML checkboxes don't support this fully, so it's only used for UX display purposes.

[Back to Contents](https://github.com/vineyard-bloom/bloom-inputs#contents)
