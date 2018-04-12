# Checkbox

### Examples
#### General Use:
```
  <Checkbox
    checked={!!this.props.agreed.value}
    error={this.props.agreed.error}
    name='agreed'
    label='Do you agree?'
    onChange={(e) => this.props.updateField('agreed', e.target.value)}
  />
```

#### Bloom-Forms use:
```
  const { checkField, formData, updateField } = this.props

  <Checkbox
    checked={formData.agreed.value}
    error={formData.agreed.error}
    name='agreed'
    label='Do you agree?'
    onBlur={checkField}
    onChange={updateField}
  />
```

### Required Props
- `checked`:
  A boolean for if the element is checked or not. Usually populated like `formData.field.value`.
- `name`:
  A string that should match one of the string in `fieldNames` passed into `<Form>`. Also used as the checkbox's ID.
- `label`:
  Either a string or an element to label the checkbox. Hidden by default, but always required for accessibility purposes.
- `onChange`:
  A function that fires when the checkbox is clicked. Usually `updateForm`.

### Optional Props
- `className`:
  A string for styling the checkbox input.
- `containerClass`:
  A string for styling the entire div around the input and its label.
- `error`:
  A string for displaying errors. Usually populated like `formData.field.error`.
- `labelClass`:
  A string for styling the label text.
- `onBlur`:
  A function that fires when the `Checkbox` loses focus. Usually fires validation via `checkField`.
- `required`:
  A boolean indicating if the input value can't be empty.
- `showLabel`:
  A boolean showing or hiding the label text. By default, all bloom forms input labels are hidden.
- `showLabelBeforeCheckbox`:
  A boolean reversing the display order of checkbox and label text.
- `validateAs`:
  A string tying into the validation help passed in to the wrapper `<Form>`. Examples include 'not-empty', 'zip', and 'number'.

[Back to Contents](https://github.com/vineyard-bloom/bloom-inputs#contents)
