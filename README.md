# Stitch → Figma Converter

Convert Google Stitch 2.0 HTML/CSS output into structured Figma-compatible node trees.

## Features

- **Paste & Convert** — Drop in Stitch HTML/CSS output, get Figma nodes
- **Tree View** — Visual hierarchy of the converted Figma node structure
- **Figma JSON** — Copy the raw Figma-compatible JSON for API use
- **Plugin Code** — Auto-generated TypeScript for direct use in Figma plugins
- **Live Preview** — See the original HTML rendered side-by-side
- **Drag & Drop** — Drop `.html` files directly onto the editor
- **Keyboard Shortcuts** — `Cmd+Enter` to convert

## How It Works

1. Paste Stitch HTML/CSS into the left panel
2. Click **Convert** (or press `Cmd+Enter`)
3. Browse the output:
   - **Tree** — Interactive node hierarchy
   - **Figma JSON** — Raw node data for Figma REST API
   - **Plugin Code** — Ready-to-use Figma plugin TypeScript
   - **Preview** — Original HTML rendering

## Conversion Details

The converter maps HTML/CSS to Figma nodes:

| HTML | Figma |
|------|-------|
| `div`, `section`, `nav`, etc. | FRAME with auto-layout |
| `p`, `h1`-`h6`, `span`, etc. | TEXT node |
| `img` | RECTANGLE with IMAGE fill |
| `svg` | VECTOR node |
| `input`, `textarea` | FRAME with TEXT child |
| `flex` / `grid` display | Auto-layout (HORIZONTAL/VERTICAL) |
| `border-radius` | Corner radius |
| `box-shadow` | Drop shadow effect |
| `padding` | Frame padding |
| `gap` | Item spacing |

## License

MIT
