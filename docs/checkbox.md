# Checkbox

A styleable, semantic, accessible checkbox. Attributes not in the below Required and Optional props can be passed in, but must be HTML5 attributes.

The checked background image of the Checkbox can be styled via `.Input--checked--placeholder.is-checked`.

### Examples
#### General Use:
```
  import { Checkbox } from 'bloom-inputs'

  ...

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
  import { Checkbox } from 'bloom-inputs'

  ...

  const { checkField, formData, updateField } = this.props

  ...

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
- Either `checked` or `formData`:
  checked: A boolean for if the element is checked or not. Usually populated like `formData.field.value`.
  formData: The object holding all keys mapped to fields in your form. See [bloom-forms' formData prop](https://github.com/vineyard-bloom/bloom-forms/blob/master/docs/children-props.md). If you use formData via bloom-forms, `checked` will be derived from it, and any errors on that field will be passed in for you too.
- `name`:
  A string for the component's name and id. When using bloom-forms, name ties the `formData` to the input's value. It should match one of the strings in `fieldNames` array passed into `<Form>`.
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
