# FileInput

Inline file input that does not support drag and drop.

### Examples
#### General
```
  import { FileInput } from 'bloom-inputs'
  
  ...

  <FileInput
    accept='.jpg'
    clearable
    files={this.props.profileImage.value}
    label='Upload your Profile Picture'
    name='profileImage'
    onChange={(formId, fieldName='profileImage', value, type='file') => this.props.updateImageField(formId, fieldName, value, type)}
  />
```

#### Bloom-Forms use
```
  import { FileInput } from 'bloom-inputs'

  ...
  
  const { checkField, formData, manualFieldUpdate } = this.props

  ...

  <FileInput
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
- `formId`:
  A string that matches the id passed into your wrapper `<Form>`.
- `label`:
  A string labelling your `FileInput`. Required for accessibility purposes, but hidden by default.
- `name`:
  A string tying the `FileInput`'s value to the `formData`. Also sets the `name` prop of each element in the group.
- `onChange`:
  A function used to update the `FileInput`'s value. Generally, this should be `manualFieldUpdate`.

### Optional Props
- `accept`:
  A string limiting the file types accepted. Native HTML5 'accept' attribute on input type='file'.
- `clearable`:
  A boolean that renders a 'clear' button when the field is populated to easily empty the field
- `containerClass`:
  A string for styling the entire div around the input and its label.
- `error`:
  A string for displaying errors
- `id`:
  A string giving the `FileInput` its ID. Defaults to the `name` passed in if not defined.
- `multiple`:
  A boolean allowing multiple files to be uploaded simultaneously.
- `onBlur`:
- `required`:

[Back to Contents](https://github.com/vineyard-bloom/bloom-inputs#contents)
