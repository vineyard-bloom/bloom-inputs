# Dropzone
A file input that supports drag and drop and multiple files. Forked and reworked for our purposes (accessibility, stylability) from 'react-dropzone'.

### Examples
#### General
```
  import { Dropzone } from 'bloom-inputs'

  ...

  <Dropzone
    accept='.jpg'
    files={this.props.profileImage.value}
    label='Upload your Profile Picture'
    name='profileImage'
    onChange={(formId, fieldName='profileImage', value, type='file') => this.props.updateImageField(formId, fieldName, value, type)}
  />
```

#### Bloom-Forms use
```
  import { Dropzone } from 'bloom-inputs'

  ...

  const { checkField, formData, manualFieldUpdate } = this.props

  ...

  <Dropzone
    accept='.jpg'
    formData={formData}
    label='Upload your Profile Picture'
    name='profileImage'
    onBlur={checkField}
    onChange={manualFieldUpdate}
    validateAs='jpgFile' // make sure this custom validation type is defined in your form wrapper
  />
```

### Required Props
- Either `files` or `formData`:
  files: An array of File objects. Should be passed in like `formData.field.value`, as file inputs append an array of Files to the redux store.
  formData: The object holding all keys mapped to fields in your form. See [bloom-forms' formData prop](https://github.com/vineyard-bloom/bloom-forms/blob/master/docs/children-props.md). If you use formData via bloom-forms, the value will be derived from it, and any errors on that field will be passed in for you too.
- `label`:
  A string that labels the `Dropzone`. Required for accessibility purposes, but hidden by default.
- `name`:
  A string for the component's name and id. When using bloom-forms, name ties the `formData` to the input's value. It should match one of the strings in `fieldNames` array passed into `<Form>`.
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
