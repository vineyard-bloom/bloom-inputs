# ErrorTip

This is a component used to render errors next to each input. It's fully style-able, but [bloom-starter](https://github.com/vineyard-bloom/bloom-starter) includes styles to make it look like a tooltip pointed to the input.

The ErrorTip was designed to render on every bloom-inputs input that has an `error`, but can be used in other cases if needed.

### Example
```
  <ErrorTip
    contents='This section must be fully populated before submission.'
    direction='right'
  />
```

### Required Props
- `contents`:
    A string or a React element to populate the error tip

### Optional Props
- `className`:
    A string to style the ErrorTip
- `direction`:
    A string indicating which direction the arrow is pointing. By default, it's 'top'.
