# TOON Prompt Pro

A free, unlimited, fully client-side **TOON Prompt Generator** and **JSON &harr; TOON Converter**. No server, no API calls, no rate limits — everything runs in your browser.

## Features

- **Prompt Builder** — Structured form to build TOON prompts with fields, rows, and custom delimiters
- **JSON &harr; TOON Converter** — Bidirectional conversion between JSON and TOON format
- **Format Comparison** — Compare token usage across JSON, TOON, and plain text side by side
- **Template Library** — Pre-built templates for common use cases (user profiles, product catalogs, support tickets, etc.)
- **Token Estimator** — See estimated token counts and savings vs JSON
- **Unlimited** — No input length limits, no API keys, no login, no rate limiting
- **Export** — Copy to clipboard, download as `.toon` files

## What is TOON?

**Token-Oriented Object Notation** (TOON) is a compact serialization format designed for LLM interactions. It saves 30-60% tokens compared to JSON by declaring field names once and listing values in clean rows.

Example:

```toon
items[2]{id,name,role}:
  1,Alice,admin
  2,Bob,user
```

Instead of JSON's verbose:

```json
[
  { "id": 1, "name": "Alice", "role": "admin" },
  { "id": 2, "name": "Bob", "role": "user" }
]
```

## Why This Exists

The [Feedough TOON Prompt Generator](https://www.feedough.com/toon-prompt-generator/) is useful but has limitations:
- **10,000 character input limit**
- **Backend API calls** (relies on paid APIs like OpenAI, Groq, etc.)
- **Rate limiting** (server-side)
- **Requires their server** (could go down)

This tool fixes all of that by working **entirely client-side**. No servers, no API keys, no limits.

## Deployment

### Deploy on Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fpankajjjat%2Ftoon-prompt-pro)

1. Fork this repo to your GitHub account
2. Go to [vercel.com](https://vercel.com) and import the repo
3. Vercel auto-detects it as a static site — just deploy
4. That's it. No build step needed.

### Deploy on GitHub Pages

1. Go to your repo Settings > Pages
2. Source: Deploy from branch, branch: `main`, folder: `/`
3. Save — your site is live at `https://<username>.github.io/toon-prompt-pro/`

## Local Development

Just open `index.html` in any browser. No build tools, no dependencies, nothing to install.

```bash
# Clone the repo
git clone https://github.com/pankajjjat/toon-prompt-pro.git

# Open the file
open index.html   # macOS
start index.html  # Windows
xdg-open index.html  # Linux
```

## Tech Stack

- Plain HTML, CSS, JavaScript — zero dependencies
- Everything runs client-side in the browser
- ~400 lines of vanilla JS for the entire converter engine
- No build step, no npm, no frameworks

## License

MIT
