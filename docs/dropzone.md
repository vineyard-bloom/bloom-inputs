# Dropzone
A file input that supports drag and drop and multiple files. Forked and reworked for our purposes from 'react-dropzone'.

### Required Props
- `files`:
  An array of File objects. Should be passed in like `formData.field.value`, as file inputs append an array of Files to the redux store.
- `label`:
  A string that labels the `Dropzone`. Required for accessibility purposes, but hidden by default.
- `name`:
  A string tying the `formData` to the input's value. It should match one of the strings in `fieldNames` array passed into `<Form>`.
- `onChange`:
  A function used to update the `Dropzone`'s value. Generally, this should be `manualFieldUpdate`.

### Optional Props
- `accept`:
  A string limiting the file types accepted. Native HTML5 'accept' attribute on input type='file'.
- `containerClass`:
  A string for styling the entire div around the input and its label.
- `imageStyle`:
  An object with CSS for styling the preview images of any uploaded files. Will fall back to default styles if not defined.
- `loadingElement`:
  A React Element containing a spinner or other loading indicator in case you don't want to use the bloom-forms default spinner.
- `multiple`:
  A boolean allowing multiple files to be uploaded simultaneously. Defaults to `true`.
- `required`:
  A boolean indicating if the input value can't be empty.

[Back to Contents](https://github.com/vineyard-bloom/bloom-inputs#contents)
