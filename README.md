# TOON Prompt Pro

A free, unlimited TOON Prompt Generator — convert JSON to TOON format for LLM prompts. 100% client-side, powered by the official `@toon-format/toon` library.

## Features

- **JSON → TOON conversion** using the official spec-compliant library
- **TOON → JSON conversion** (round-trip safe)
- **Format comparison** — see token savings vs JSON
- **8 built-in templates** (User Profiles, Product Catalog, Support Tickets, Training Examples, etc.)
- **Delimiter options**: comma (default), tab, pipe
- **Zero dependencies** — fully client-side, no API key needed, unlimited usage
- **CLI integration** available via `npx @toon-format/cli`

## How to Use

Open `index.html` in any browser, or deploy to Vercel/GitHub Pages.

### Builder tab

1. Paste JSON data (array of objects)
2. Click **Generate TOON**
3. Copy or download the result

### Converter tab

- JSON → TOON: paste JSON, click Convert
- TOON → JSON: paste TOON, click Convert

## What is TOON?

**Token-Oriented Object Notation** (TOON) is a compact, line-oriented serialization format for LLM interactions. It preserves the JSON data model while cutting token usage by 30-60%.

Example:
```
items[3]{id,name,role}:
  1,Alice,admin
  2,Bob,user
  3,Charlie,user
```

vs JSON (60% more tokens):
```json
[
  { "id": 1, "name": "Alice", "role": "admin" },
  { "id": 2, "name": "Bob", "role": "user" },
  { "id": 3, "name": "Charlie", "role": "user" }
]
```

## Deployment

### Vercel
```bash
vercel --prod
```

### GitHub Pages
Push to `gh-pages` branch and enable Pages in repo settings.

## Technical Details

- Uses the `@toon-format/toon` library (v1.2.0) loaded from jsDelivr CDN
- All processing happens in the browser — no data leaves your machine
- Token estimation uses a simple `chars / 4` heuristic (actual savings depend on tokenizer)

## Credits

- [TOON Format](https://toonformat.dev) — specification and reference implementation by Johann Schopplich
- Built with [@toon-format/toon](https://github.com/toon-format/toon)
