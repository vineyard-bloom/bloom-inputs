# CurrencyInput

CurrencyInput is a special TextInput that always validates as a number and displays the type of currency in the background of the input.

### Required Props
- `currency`:
  A string noting the type of currency. Typically 'ETH', 'BTC', etc.
- `id`:
  A string that becomes the input's ID.
- `label`:
  Either a string or a React element that labels the `CurrencyInput`. Required for accessibility purposes, but hidden by default.
- `name`:
  A string tying the `formData` to the input's value. It should match one of the strings in `fieldNames` array passed into `<Form>`.
- `onChange`:
  A function used to update the `CurrencyInput`'s value. Generally, this should be `updateForm`.
- `value`:
  A string holding the value of the `CurrencyInput`. Generally passed in like `formData.field.value`.

### Optional Props
- `className`:
  A string for styling the currency input.
- `containerClass`:
  A string for styling the entire div around the input and its label.
- `error`:
  A string usually passed in directly from `formData` that notes an error with that field validation. Generally passed in like `formData.field.error`.
- `labelClass`:
  A string that styles just the label text.
- `placeholder`:
  A string that shows up in the background of the `CurrencyInput` when its value is empty.
- `onBlur`:
  A function that fires when focus leaves the element. Usually used to `checkField`.
- `required`:
  A boolean indicating if the input value can't be empty.
- showLabel:
  A boolean showing or hiding the label text. By default, all bloom forms input labels are hidden.

[Back to Contents](https://github.com/vineyard-bloom/bloom-inputs#contents)
