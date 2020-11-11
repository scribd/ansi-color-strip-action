# ANSI Color Strip Action

Github Action to remove any ANSI escaped colors from a passed in file or string.

## Inputs

### `string`

The string to retrieve lines from.

### `path`

The filepath to retrieve lines from.

### `overwrite-path`

Replace the provided filepath with the content after color removal.

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