# SelectInput

A `<select>` input that's fully accessible and fully-stylable. This is the most customized component in bloom-inputs, as styling a native `<select>` across browsers, including its `<options>` is extremely limited.

### Examples
#### General
```
  const options = [
    {
      label: '0 - 18',
      value: 'range1'
    },
    {
      label: '19 - 29',
      value: 'range2'
    },
    {
      label: '30 - 39',
      value: 'range3'
    },
    {
      label: '40 - 49',
      value: 'range4'
    },
    {
      label: '50 - 59',
      value: 'range5'
    },
    {
      label: '60 - 69',
      value: 'range6'
    },
    {
      label: '70 +',
      value: 'range7'
    }
  ]

  ...

  <SelectInput
    formId={this.props.formId}
    name='ageRange'
    onChange={(formId=this.props.formId, fieldName='ageRange', value) => this.props.updateAgeRange(formId, fieldName, value)}
    options={options}
    value={this.props.ageRange.value}
  />
```

#### Bloom-Forms use
```
  const { checkField, formData, formId, manualFieldUpdate } = this.props
  const options = [
    {
      label: '0 - 18',
      value: 'range1'
    },
    {
      label: '19 - 29',
      value: 'range2'
    },
    {
      label: '30 - 39',
      value: 'range3'
    },
    {
      label: '40 - 49',
      value: 'range4'
    },
    {
      label: '50 - 59',
      value: 'range5'
    },
    {
      label: '60 - 69',
      value: 'range6'
    },
    {
      label: '70 +',
      value: 'range7'
    }
  ]

  ...

  <SelectInput
    formData={formData}
    formId={formId}
    name='ageRange'
    onBlur={checkField}
    onChange={manualFieldUpdate}
    options={options}
    required
    validateAs='not-empty'
  />
```

### Required Props
- `formId`:
  A string that matches the id passed into your wrapper `<Form>`.
- `label`:
  A string labelling your select input. Required for accessibility purposes, but hidden by default.
- `name`:
  A string tying the `formData` to the input's value. It should match one of the strings in `fieldNames` array passed into `<Form>`.
- `onChange`:
  A function used to update the `SelectInput`'s value. Generally, this should be `manualFieldUpdate`.
- `options`:
  An array of either strings, or an object of type: { label: string, value: number or string }. These populate your `SelectInput` options.
- `value`:
  Either a number or string holding the value of the `SelectInput`. Generally passed in like `formData.field.value`.

### Optional Props
- `clearable`:
  A boolean that renders an 'x' button next to the input to clear any value selected.
- `containerClass`:
  A string to style the entire select input container. Shows up on `<label>` in the DOM.
- `error`:
  A string usually passed in directly from `formData` that notes an error with that field validation. Generally passed in like `formData.field.error`.
- `loading`:
  A boolean indicating if an ajax request is populating the options of your SelectInput.
- `onBlur`:
  A function that fires when focus leaves the element. Usually used to `checkField`.
- `required`:
  A boolean indicating if the input value can't be empty.
- `showLabel`:
  A boolean showing or hiding the label text. By default, all bloom forms input labels are hidden.
- `typeAhead`:
  A boolean indicating if the `SelectInput` should have typeahead functionality. If set to false, typing letter characters has no effect on results.
- `validateAs`:
  A string tying into the validation help passed in to the wrapper `<Form>`. Examples include 'not-empty', 'zip', and 'number'.

[Back to Contents](https://github.com/vineyard-bloom/bloom-inputs#contents)
