---
name: markdown-style-guide
description: Markdown formatting standards for headings, emphasis, lists, links, code, tables.
---

# Markdown Style Guide

## Headings
- `#` through `######`; one `#` per document
- Logical hierarchy (no skipping levels)
- Blank line before/after

## Emphasis
- Italic: `_text_`
- Bold: `**text**`
- Strikethrough: `~~text~~`

## Lists
- Unordered: `-` item; indent sub-items 2 spaces
- Ordered: `1.` item; can use `1.` for all (auto-numbering)
- Blank line before/after

## Links
- Inline: `[text](url)`
- Reference: `[text][ref]` with `[ref]: url` at bottom
- Descriptive text, not "click here"

## Blockquotes
- `>` prefix; nested: `>>`
- Blank line before/after

## Code
- Inline: `` `code` ``
- Fenced blocks: triple backticks with language
  ```javascript
  function greet(name) {
      console.log(`Hello, ${name}!`);
  }
  ```
- Prefer fenced over indented

## Tables
- `|` columns; `-` header separator
- Alignment: `:---` left, `:---:` center, `---:` right

## Horizontal Rules
- `---` on own line; blank lines before/after

## Images
- `![alt](url)`; always include descriptive alt text

## Task Lists
- `- [ ]` unchecked, `- [x]` checked

## Best Practices
- Blank lines before/after: headings, lists, code, blockquotes, tables, rules
- Lines ~80-100 chars
- Consistent formatting throughout
- Language identifiers in code blocks