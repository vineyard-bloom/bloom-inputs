# FileInput

Inline file input that does not support drag and drop.

### Required Props
- `formId`:
  A string that matches the id passed into your wrapper `<Form>`.
- `label`:
  A string labelling your `FileInput`. Required for accessibility purposes, but hidden by default.
- `id`:
  A string giving the `FileInput` its ID.
- `name`:
  A string tying the `FileInput`'s value to the `formData`. Also sets the `name` prop of each element in the group.
- `onChange`:
  A function used to update the `FileInput`'s value. Generally, this should be `manualFieldUpdate`.

### Optional Props
- `accept`:
  A string limiting the file types accepted. Native HTML5 'accept' attribute on input type='file'.
- `containerClass`:
  A string for styling the entire div around the input and its label.
- `error`:
  A string for displaying errors
- `multiple`:
  A boolean allowing multiple files to be uploaded simultaneously.
- `onBlur`:
- `required`:

[Back to Contents](https://github.com/vineyard-bloom/bloom-inputs#contents)
