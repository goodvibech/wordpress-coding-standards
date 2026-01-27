---
name: php-coding-standards
description: WordPress PHP coding standards for formatting, naming, control structures, database access.
---

# PHP Coding Standards

## Syntax & Tags
- Use `<?php` on own line in HTML; omit `?>` in PHP-only files
- No short tags (`<?`, `<?=`); always use full tags
- Single quotes unless interpolation needed; escape HTML/XML output
- `require`/`include` without parentheses; prefer `require_once`
- Dynamic hooks: `"{ $var }"` not concatenation

## Naming
- Variables/functions/actions/filters: `lowercase_with_underscores`
- Classes/traits/interfaces/enums: `Capitalized_Words` (acronyms uppercase)
- Constants: `UPPERCASE_WITH_UNDERSCORES`
- Files: `lowercase-with-hyphens`; class files: `class-name.php`

## Whitespace
- Spaces after commas; around operators (`=`, `+`, `==`, etc.)
- Spaces inside control structure parentheses
- Arrays: `$foo['bar']` (no space), `$foo[ $var ]` (space)
- `case label:` (no space before colon)
- Increment: `$i++` (no spaces)
- Indent with tabs; spaces only for alignment
- No trailing whitespace

## Control Structures
- Always use braces; no single-line control structures
- Use `elseif` not `else if`
- Yoda conditions for equality (`==`, `!=`, `===`, `!==`) only
- No assignments in conditionals

## Operators
- Ternary: evaluate true first; no shorthand ternary
- Avoid `@` error suppression
- Prefer pre-increment/pre-decrement

## Database
- Use APIs over direct SQL when available
- Uppercase SQL keywords; break long queries
- Escape with `$wpdb->prepare()`; don't quote placeholders (`%d`, `%s`, etc.)

## Forbidden
- `goto`, `eval()`, `create_function()`, `extract()`, backticks
- PCRE only (`preg_*`); no `/e` modifier
- Comment intentional switch fall-throughs