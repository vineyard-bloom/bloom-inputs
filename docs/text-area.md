# TextArea

TextArea is a multi-line text input for large amounts of text. Uses HTML5 `<textarea>`.

### Examples
#### General
```
  <TextArea
    label='Comment'
    name='comment'
    onChange={(e) => this.props.updateComment(e.target.value)}
    value={this.props.comment.value}
  />
```

#### Bloom-Forms use
```
  const { checkField, formData, updateField } = this.props

  <TextArea
    formData={formData}
    label='Comment'
    name='comment'
    onBlur={checkField}
    onChange={updateField}
    validateAs='max-120-chars'
  />
```

### Required Props
- `label`:
  Either a string or a React element that labels the `TextArea`. Required for accessibility purposes, but hidden by default.
- `name`:
  A string tying the `formData` to the input's value. It should match one of the strings in `fieldNames` array passed into `<Form>`.
- `onChange`:
  A function used to update the `TextArea`'s value. Generally, this should be `updateForm`.
- `value`:
  A string holding the value of the `TextArea`. Generally passed in like `formData.field.value`.

### Optional Props
- `className`:
  A string that styles the input box directly.
- `containerClass`:
  A string for styling the entire div around the input and its label.
- `error`:
  A string usually passed in directly from `formData` that notes an error with that field validation. Generally passed in like `formData.field.error`.
- `labelClass`:
  A string that styles only the label text of the `TextArea`.
- `placeholder`:
  A string that shows up in the background of the `TextArea` when its value is empty.
- `onBlur`:
  A function that fires when focus leaves the element. Usually used to `checkField`.
- `required`:
  A boolean indicating if the input value can't be empty.
- `showLabel`:
  A boolean showing or hiding the label text. By default, all bloom forms input labels are hidden.
- `validateAs`:
  A string tying into the validation help passed in to the wrapper `<Form>`. Examples include 'not-empty', 'zip', and 'number'.

[Back to Contents](https://github.com/vineyard-bloom/bloom-inputs#contents)
