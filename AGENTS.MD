# Agent instructions for webtools

These tools are single-page, single-file HTML apps served from GitHub Pages.

## Add a new tool
1. Create a new file in `docs/` named with lowercase `snake_case` or `kebab-case` (example: `feel-the-agi.html`).
2. Keep the tool self-contained in one HTML file: inline CSS in `<style>` and JS in `<script>`.
3. Include a minimal HTML skeleton with `<!doctype html>`, `<meta charset="utf-8">`, and `<meta name="viewport" content="width=device-width, initial-scale=1">`.
4. Avoid build steps. If you must use assets, put them under `docs/assets/` and reference them with relative paths.
5. Add a link to the new tool in `docs/index.html`.

## Quality checklist
- Clear title and on-page heading that match the tool name.
- Works when opened directly in the browser or via `python3 -m http.server` from `docs/`.
- No external dependencies unless they are necessary and stable.

## GitHub Pages URL
With Pages configured to serve `/docs` from `main`, each tool is available at:
`https://cast42.github.io/webtools/<tool_name>.html`
