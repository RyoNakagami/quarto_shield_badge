# Shield_badge Extension For Quarto

This Quarto extension provides a convenient shortcode for adding [Shields.io](https://shields.io/) badges to your Quarto documents. It supports both inline JSON and JSON file inputs to customize badge appearance.

## Installing

```bash
quarto add RyoNak/quarto_shield_badge
```

This will install the extension under the `_extensions` subdirectory.
If you're using version control, you will want to check in this directory.

## Using

The extension provides a `shield_badge` shortcode that can be used in two ways:

1. Using inline JSON:

```qmd
{{< shield_badge '{"label": "version", "message": "1.0.0", "color": "blue"}' >}}
```

2. Using a JSON file:

```qmd
{{< shield_badge "path/to/badge.json" >}}
```

The JSON input (either inline or in file) should contain these properties:

- `label`: The text shown on the left side of the badge (default: "badge")
- `message`: The text shown on the right side of the badge (default: "unknown")
- `color`: The color of the right side of the badge (default: "lightgrey")

Spaces in `label` and `message` are automatically converted to underscores.

## Example

Here is the source code for a minimal example: [example.qmd](example.qmd).

Example output badges:

- ![Version](https://img.shields.io/badge/version-1.0.0-blue)
- ![Status](https://img.shields.io/badge/status-stable-green)
- ![License](https://img.shields.io/badge/license-MIT-orange)
- ![Python](https://img.shields.io/badge/python-3.11.8-blue)

## License

[MIT License](./LICENSE)

Copyright (c) 2024 [RyoNak](https://github.com/RyoNakagami)



## References

- [Shields.io](https://shields.io/)
- [Quarto](https://quarto.org/)
