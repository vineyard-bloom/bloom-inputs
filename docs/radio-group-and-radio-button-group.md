# Radio Group
and
# Radio Button Group

Both RadioGroup and RadioButtonGroup are used when there are a variety of options to choose from, but only one can be selected at once.
RadioButtonGroup behaves nearly identically to RadioGroup but has the styling of buttons.

### Examples
#### General use
```
  import { RadioGroup, RadioButtonGroup } from 'bloom-inputs'

  const options = [
    {
      id: 'x-small',
      label: 'XS'
    },
    {
      id: 'small',
      label: 'S'
    },
    {
      id: 'medium',
      label: 'M'
    },
    {
      id: 'large',
      label: 'L'
    }
  ]

  ...

  <RadioGroup // (or RadioButtonGroup)
    name='size'
    onChange={(e) => this.props.updateSize(e.target.id)}
    options={options}
    value={this.props.size.value}
  />
```

#### Bloom-Forms use
```
  import { RadioGroup, RadioButtonGroup } from 'bloom-inputs'

  const { checkField, formData, updateField } = this.props
  const options = [
    {
      id: 'x-small',
      label: 'XS'
    },
    {
      id: 'small',
      label: 'S'
    },
    {
      id: 'medium',
      label: 'M'
    },
    {
      id: 'large',
      label: 'L'
    }
  ]

  ...

  <RadioGroup // (or RadioButtonGroup)
    formData={formData}
    name='size'
    onBlur={checkField}
    onChange={updateField}
    options={options}
    validateAs='not-empty'
  />
```

### Required Props
- `name`:
  A string tying the `RadioGroup`'s value to the `formData`. Also sets the `name` prop of each element in the group.
- `onChange`:
  A function used to update the `RadioGroup`'s value. If using bloom-forms, this should be `updateForm`.
- `options`:
  An array of radio options, with each one looking like:
```
  {
    id: string,
    label: either a string or a react element
  }
```
- Either `value` or `formData`:
  value: A string mapped to the `RadioGroup`'s value in `formData`.
  formData: The object holding all keys mapped to fields in your form. See [bloom-forms' formData prop](https://github.com/vineyard-bloom/bloom-forms/blob/master/docs/children-props.md). If you use formData via bloom-forms, the value will be derived from it, and any errors on that field will be passed in for you too.

### Optional Props
- `className`:
  A string to style each radio input.
- `containerClass`:
  A string to style the entire component wrapper.
- `error`:
  A string usually passed in directly from `formData` that notes an error with that field validation. Generally passed in like `formData.field.error`.
- `labelClass`:
  A string that styles only the label text of each radio input.
- `onBlur`:
  A function that fires when focus leaves the element. Usually used to `checkField`.
- `required`:
  A boolean indicating if the input value can't be empty.
- `validateAs`:
  A string tying into the validation help passed in to the wrapper `<Form>`. Examples include 'not-empty', 'zip', and 'number'.

[Back to Contents](https://github.com/vineyard-bloom/bloom-inputs#contents)
