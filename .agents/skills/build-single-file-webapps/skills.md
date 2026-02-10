# Skill: build-single-file-webapps

This skill follows the approach described by [Simon Willison](https://en.wikipedia.org/wiki/Simon_Willison) in:

[https://simonwillison.net/2025/Dec/10/html-tools/](https://simonwillison.net/2025/Dec/10/html-tools/)

The goal is to build small, useful tools as **single self-contained HTML files**
that are easy to understand, easy to modify, and easy to share.

The HTML file itself is the product, the documentation, and the distribution
format.

## Core Principles

- One tool = one `.html` file
- No build step
- No framework
- Open in a browser → it works
- View Source explains how it works
- Designed to be copied, forked, and adapted

## Allowed Technologies

- Plain HTML5
- Vanilla JavaScript (ES2020+)
- `<script>` or `<script type="module">`
- `<style>` blocks or inline CSS
- Modern browser APIs, including:
  - fetch
  - localStorage / sessionStorage
  - URLSearchParams
  - Web Workers (inline only)

## Forbidden

- React, Vue, Svelte, Angular
- npm, pnpm, yarn
- Bundlers or build tools (Vite, Webpack, etc.)
- Server-side code
- External JavaScript dependencies (unless unavoidable and clearly justified)

## File Structure

The HTML file should follow this structure:

1. `<head>`
   - `<meta charset="utf-8">`
   - `<meta name="viewport" content="width=device-width, initial-scale=1">`
   - `<title>` describing the tool
   - `<style>` with readable, minimal CSS

2. `<body>`
   - A clear heading explaining what the tool does
   - A short paragraph describing how to use it
   - A minimal, functional UI using semantic HTML
   - One `<script>` block at the end

## UX Expectations

- The page explains itself in plain language
- Inputs have visible labels
- Errors are shown inline
- Results are easy to copy
- State may persist using localStorage when helpful

## JavaScript Style

- Prefer functions over classes
- Avoid global variables
- Use async / await
- Prefer clarity over cleverness
- Comment intent and constraints, not obvious mechanics

## Data & APIs

- All behavior must be inspectable via View Source
- No hidden processing
- If an API key is required:
  - Explain how the user provides it
  - Never hardcode secrets
  - Prefer user-supplied keys via input fields

## Accessibility

- Use real `<button>` elements
- Associate labels with inputs
- Keyboard interaction must work
- Avoid relying solely on color for meaning

## Output Rules

When asked to build a tool using this skill:

- Produce a **single complete HTML file**
- Do not split code into multiple files
- Do not suggest framework-based alternatives
- Assume the file may be published directly to the `webtools` repository
- The result should be suitable for hosting via GitHub Pages or raw file access

## Intended Use

Tools built with this skill are meant to live in:

<https://github.com/cast42/webtools>

They should be small, durable, and useful — favoring simplicity and longevity
over extensibility or abstraction.
