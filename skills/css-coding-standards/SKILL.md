---
name: css-coding-standards
description: WordPress CSS standards for formatting, naming, BEM, specificity, property ordering.
---

# CSS Coding Standards

## Formatting
- One selector per line; one declaration per line
- Braces on new lines
- ~80 char lines; 2 blank lines between sections, 1 between rules
- Consistent indentation (tabs for WordPress, 2 spaces otherwise)

## Naming & Selectors
- Classes: `lowercase-hyphenated` (e.g., `.main-header`)
- BEM: `.block__element--modifier`
- Use classes, not IDs, for styling
- Avoid over-qualification (`.nav` not `ul.nav`)
- Keep specificity low; avoid deep nesting
- Rare `!important` with explanation

## Properties
- `property: value;` (space after colon)
- Lowercase values (except font names, vendor-specific)
- Order: display/position → box model → colors/typography → other
- Use shorthand properties; TRBL order
- Consistent ordering across project

## Comments
- Section headers in large files; TOC at top
- Document intent/reasoning, not mechanics
- Explain hacks and `!important` usage

## Architecture
- Build reusable components; keep specificity low
- Avoid magic numbers; document necessary ones
- Separate JS hooks: `data-js` or `.js-` prefix

## Media Queries
- Group near end or in relevant sections
- Indent nested rules one level
- Organize by component/logical block