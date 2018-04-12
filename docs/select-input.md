# SelectInput

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
