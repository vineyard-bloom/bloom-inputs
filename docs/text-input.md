# TextInput

TextInput is a single line text input used most often in forms.

### Required Props
- `label`:
  Either a string or a React element that labels the `TextInput`. Required for accessibility purposes, but hidden by default.
- `name`:
  A string tying the `formData` to the input's value. It should match one of the strings in `fieldNames` array passed into `<Form>`.
- `onChange`:
  A function used to update the `TextInput`'s value. Generally, this should be `updateForm`.
- `value`:
  A string holding the value of the `TextInput`. Generally passed in like `formData.field.value`.

### Optional Props
- `className`:
  A string that styles the input box directly.
- `containerClass`:
  A string that styles the wrapper around the entire component.
- `error`:
  A string usually passed in directly from `formData` that notes an error with that field validation. Generally passed in like `formData.field.error`.
- `isPassword`:
  A boolean that, when true, obfuscates all characters entered into the input and makes them appear as dots.
- `labelClass`:
  A string that styles only the label text of the `TextInput`.
- `placeholder`:
  A string that shows up in the background of the `TextInput` when its value is empty.
- `onBlur`:
  A function that fires when focus leaves the element. Usually used to `checkField`.
- `onKeyDown`:
  A function capturing a keydown event.
- `required`:
  A boolean indicating if the input value can't be empty.
- `showLabel`:
  A boolean showing or hiding the label text. By default, all bloom forms input labels are hidden.
- `validateAs`:
  A string tying into the validation help passed in to the wrapper `<Form>`. Examples include 'not-empty', 'zip', and 'number'.

[Back to Contents](https://github.com/vineyard-bloom/bloom-inputs#contents)
