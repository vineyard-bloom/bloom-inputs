# DateInput

An input type='date' styled like other bloom-inputs. All date-picking functionality is native to the browser at this time.

*** This component needs custom date-picking implementation for cross-browser uniformity.

### Examples
#### General
```
  import { DateInput } from 'bloom-inputs'
  
  <DateInput
    error={this.props.date.error}
    label='Date Joined'
    name='date'
    onChange={(e) => this.props.updateField('date', e.target.value)}
    value={this.props.date.value}
  />
```

#### Bloom-Forms use
```
  import { DateInput } from 'bloom-inputs'

  const { checkField, formData, updateField } = this.props
  
  ...

  <DateInput
    formData={formData}
    name='date'
    label='Date Joined'
    onBlur={checkField}
    onChange={updateField}
    validateAs='date'
  />
```

### Required Props
- `label`:
  Either a string or a React element that labels the `DateInput`. Required for accessibility purposes, but hidden by default.
- `name`:
  A string for the component's name and id. When using bloom-forms, name ties the `formData` to the input's value. It should match one of the strings in `fieldNames` array passed into `<Form>`.
- `onChange`:
  A function used to update the `DateInput`'s value. Generally, this should be `updateForm`.
- Either `formData` or `value`:
    formData: The object holding all keys mapped to fields in your form. See [bloom-forms' formData prop](https://github.com/vineyard-bloom/bloom-forms/blob/master/docs/children-props.md). If you use formData via bloom-forms, the value will be derived from it, and any errors on that field will be passed in for you too.
    value: A string holding the value of the `DateInput`. Generally passed in like `formData.field.value`.

### Optional Props
- `className`:
    A string to style the DateInput
- `error`:
  A string for displaying errors. Usually populated like `formData.field.error`.
- `labelClass`:
  A string for styling the label text.
- `onBlur`:
  A function that fires when the `DateInput` loses focus. Usually fires validation via `checkField`.
- `placeholder`:
  The helper text rendered inside the DateInput when it has no value
- `required`:
  A boolean indicating if the input value can't be empty.
- `showLabel`:
  A boolean showing or hiding the label text. By default, all bloom forms input labels are hidden.
- `suppressErrors`:
  A boolean controlling whether errors will render (though they may still be validated)
- `validateAs`:
  A string tying into the validation help passed in to the wrapper `<Form>`. Examples include 'not-empty', 'zip', and 'number'.
