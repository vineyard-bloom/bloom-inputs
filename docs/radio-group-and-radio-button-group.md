# Radio Group
and
# Radio Button Group

Both RadioGroup and RadioButtonGroup are used when there are a variety of options, but only one can be selected at once.
RadioButtonGroup behaves nearly identically to RadioGroup but has the styling of buttons.

### Required Props
- `name`:
  A string tying the `RadioGroup`'s value to the `formData`. Also sets the `name` prop of each element in the group.
- `onChange`:
  A function used to update the `RadioGroup`'s value. Generally, this should be `updateForm`.
- `options`:
  An array of radio options, with each one looking like:
```
  {
    id: string,
    label: either a string or a react element
  }
```
- `value`:
  A string mapped to the `RadioGroup`'s value in `formData`.

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
