# AI Coding Standards & Style Guides

This repository contains a set of focused Markdown guidelines that standardise how code and documentation should be written – both by humans and by AI coding tools.

The idea:  
You feed these files into your AI environment (or reference them in prompts), and every generated file will follow the same standards for style, naming, documentation, and structure.

---

## Repository Contents

### Language-specific documentation standards

These files define **how to write comments / docblocks**, not the code style itself.

- **`js-documentation-standards.md`**  
  JSDoc-based documentation rules for JavaScript:
  - What needs a docblock (functions, methods, classes, events, namespaces).
  - Format of docblocks (summary line, `@param`, `@return`, `@since`, etc.).
  - How to phrase summaries and descriptions.
  - When and how to document deprecations.

- **`php-documentation-standards.md`**  
  PHPDoc rules for PHP:
  - DocBlocks for functions, methods, classes, hooks, constants, and files.
  - `@since`, `@deprecated`, `@see`, `@throws`, etc.
  - How to document actions and filters.
  - Structure of file headers and inline documentation.

---

### Language-specific coding standards

These files define **how the code itself should look and behave** (formatting, naming, conventions).

- **`js-coding-standards.md`**  
  JavaScript coding rules:
  - Spacing, braces, semicolons, and line length.
  - `const`/`let` usage, naming conventions, and strict equality (`===`/`!==`).
  - Recommended type checks and array/object usage.
  - Expectations around linting and library usage.

- **`php-coding-standards.md`**  
  PHP coding rules:
  - Full PHP tags, WordPress-style naming, and indentation.
  - Control structure style (`if/elseif/else`), Yoda conditions, and arrays.
  - Visibility on methods and properties.
  - Safe patterns for error handling and database access.

- **`html-coding-standards.md`**  
  HTML rules:
  - Valid, well-formed markup.
  - Lowercase tags/attributes, quoted attribute values.
  - Self-closing tags (`<br />`, `<img />`) and indentation.
  - Basic accessibility expectations (alt attributes, headings, keyboard-friendly controls).

- **`css-coding-standards.md`**  
  CSS rules (WordPress style):
  - Selector and property formatting, indentation, and spacing.
  - Semantic, hyphenated class names.
  - Property ordering and media query structure.
  - Comment styles and how to handle `!important` and magic values.

---

### Higher-level architecture & patterns

These files complement the language-specific standards with **architectural and design guidance**.

- **`css-guidelines-harry-roberts.md`**  
  High-level CSS architecture guidelines (Harry Roberts style):
  - BEM-like naming (`.block__element--modifier`).
  - Shallow, reusable selectors and low specificity.
  - Component / object thinking, DRY, and separation of concerns.
  - How to structure large CSS codebases (sections, TOC, comments).

- **`browserstack-coding-standards-best-practices.md`**  
  Cross-language best practices:
  - Why coding standards matter (readability, maintainability, scalability).
  - Clean architecture, error handling, and security basics.
  - Version control, code reviews, and CI integration.
  - How to treat AI as a “junior dev” whose output must be reviewed.

---

### Markdown & documentation style

- **`markdown-style-guide.md`**  
  Markdown formatting rules:
  - Heading levels (`#`–`######`) and structure.
  - Lists, links, blockquotes, horizontal rules.
  - Tables and fenced code blocks with language hints.
  - How AI should structure documentation, READMEs, and specs.

---

## How to Use These Files With AI Coding Tools

### 1. As a “system” or base prompt

When configuring an AI coding assistant (e.g. in an editor plugin, CI helper, or custom tool):

- Load the relevant files as **base guidelines**:
  - JS → `js-coding-standards.md` + `js-documentation-standards.md`
  - PHP → `php-coding-standards.md` + `php-documentation-standards.md`
  - Frontend → `html-coding-standards.md` + `css-coding-standards.md` + `css-guidelines-harry-roberts.md`
  - Any docs/READMEs → `markdown-style-guide.md`
- Include `browserstack-coding-standards-best-practices.md` as a general quality layer.

Example meta-prompt for an AI tool:

> “Follow the coding and documentation rules defined in the Markdown files in this repository (JS/PHP/HTML/CSS standards, CSS Guidelines, Markdown Style Guide). Any generated code must comply with these documents.”

### 2. As part of PR / code review workflow

- Reference these documents in your **pull request template**:
  - “Does this change comply with `js-coding-standards.md` and `js-documentation-standards.md`?”
- Use them as checklists when reviewing AI-generated code:
  - Naming, spacing, docblocks, and architecture can all be checked against these files.

### 3. As local developer reference

- Keep the files in a top-level `docs/` or `standards/` folder.
- Link to them from your main project `README` or `CONTRIBUTING` guide.
- Use them when onboarding new developers or configuring their editor settings and linters.

---

## Priority & Conflicts

If there’s ever a conflict between documents:

1. **Project-specific rules first** (if you add additional rules on top).  
2. **Language-specific coding standards**  
   - e.g. `js-coding-standards.md`, `php-coding-standards.md`, `css-coding-standards.md`.  
3. **Language-specific documentation standards**  
   - e.g. `js-documentation-standards.md`, `php-documentation-standards.md`.  
4. **Higher-level architecture & best practices**  
   - `css-guidelines-harry-roberts.md`, `browserstack-coding-standards-best-practices.md`.  
5. **Markdown style** for docs and READMEs.

You can always extend these files with project-specific sections (e.g. “Project-specific exceptions” at the bottom of each file).

---

## Extending These Guidelines

- Add new files for other languages or frameworks (e.g. `python-coding-standards.md`, `react-component-guidelines.md`).
- Document any **exceptions** you intentionally allow (e.g. “no Yoda conditions in this project”).
- Keep all changes in version control so both humans and AI tools evolve with the codebase.

---

By keeping these standards in plain Markdown and in the repo, you can use the same source of truth for humans, linters, and AI coding tools.
