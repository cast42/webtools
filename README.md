# webtools

Single-file HTML tools, inspired by https://simonwillison.net/2025/Dec/10/html-tools/

## Layout
- `tools/`: source HTML tools (each tool is one `.html` file)
- `docs/`: GitHub Pages publish folder (mirrors `tools/`)
- `docs/index.html`: landing page for the published tools

## GitHub Pages
Configure Pages to serve from the `main` branch and the `/docs` folder. Then each tool is available at:

`https://cast42.github.io/webtools/`

`https://cast42.github.io/webtools/<tool_name>.html`

Example: `https://cast42.github.io/webtools/feel-the-agi.html`

## Local preview
From `tools/`:

```bash
python3 -m http.server
```

Then open `http://localhost:8000/<tool_name>.html`.

## Sync tools to docs
Before pushing, sync the publish folder:

```bash
rsync -a tools/ docs/
```
