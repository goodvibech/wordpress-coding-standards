---
name: html-coding-standards
description: WordPress HTML standards for structure, accessibility, semantic markup, formatting.
---

# HTML Coding Standards

## Validity & Structure
- W3C-valid markup; proper nesting; close required tags
- Use semantic HTML5: `<main>`, `<nav>`, `<section>`, `<article>`, `<aside>`, `<header>`, `<footer>`

## Self-Closing
- Space before `/>`: `<img src="..." />`, `<br />`, `<input />`, `<meta />`

## Tags & Attributes
- Lowercase tag/attribute names
- Quote all attribute values
- Machine-readable values lowercase: `<meta charset="utf-8">`, `<input type="email">`
- Natural case for human-readable text: `<img alt="Product Image" />`

## Indentation & Readability
- Consistent indentation reflecting structure
- Avoid unnecessary nesting; no table layouts
- Logical document structure

## Accessibility
- `alt` on all images (empty for decorative)
- Keyboard accessible: `<button>` for buttons, `<a href>` for links
- Logical heading hierarchy (one `<h1>` per page, no skipped levels)
- Label form inputs: `<label for="id">` with matching `id`, or wrap input
- Prefer semantic tags over `<div>`/`<span>`
