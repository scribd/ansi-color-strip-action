# ANSI Color Strip Action

Github Action to remove any ANSI escaped colors from a passed in file or string.

## Inputs

### `path`

The filepath to retrieve lines from.

### `string`

The string to retrieve lines from.

## Outputs

### `content`

The content after color removal.

## Example usage

```yaml
- uses: justAnotherDev/ansi-color-strip-action@v1
  id: strip
  with:
    path: xcode-build.log

- run: echo "${{ steps.strip.outputs.content }}"
```

More examples [here](https://github.com/justAnotherDev/ansi-color-strip-action/blob/master/.github/workflows/test.yml).