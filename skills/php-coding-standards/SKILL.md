---
name: php-coding-standards
description: Guidelines for writing clean, maintainable PHP code following WordPress coding standards. Use when generating or reviewing PHP, including formatting, naming, control structures, database access, and discouraged practices.
---

# PHP Coding Standards

Guidelines distilled from WordPress PHP coding standards.

## General

- **PHP tags**: In multi-line snippets embedded in HTML, place `<?php` and `?>` on their own lines; omit the closing tag in PHP-only files
- **Short tags**: Do not use `<?` or `<?=`; always use full tags
- **Quoting**: Use single quotes when interpolation is not required; alternate quote types to avoid escaping; properly escape output for HTML/XML contexts
- **Includes**: `require`/`include` are language constructs—do not use parentheses; prefer `require` or `require_once` for unconditional includes
- **Hooks**: Use interpolated strings (`"{ $var }"`) for dynamic hooks instead of concatenation

## Naming Conventions

- **Variables, functions, actions, filters**: Lowercase with underscores
- **Classes, traits, interfaces, enums**: Capitalized words separated by underscores; acronyms stay uppercase
- **Constants**: Uppercase with underscores
- **File names**: Lowercase with hyphens; class files use `class-` prefix and convert underscores to hyphens

## Whitespace & Indentation

- **Spacing**: Add spaces after commas and around logical, arithmetic, comparison, assignment, and concatenation operators
- **Control structures**: Include spaces inside parentheses
- **Arrays**: No spaces for literal indices (`$foo['bar']`); add spaces for variable indices (`$foo[ $bar ]`)
- **Switch cases**: No space before `:` in `case`
- **Increment/decrement**: No spaces (`$i++`, not `$i ++`)
- **Indentation**: Use tabs at the beginning of lines; use spaces only for alignment
- **Trailing whitespace**: Remove trailing spaces
- **Closing tag**: Omit `?>` at the end of PHP-only files

## Brace Style

- **Mandatory braces**: Always use braces, even when optional; avoid single-line control structures without braces

## Control Structures

- **`elseif`**: Use `elseif` instead of `else if`
- **Yoda conditions**: Use Yoda conditions for equality comparisons (`==`, `!=`, `===`, `!==`); do not use Yoda conditions with `<`, `>`, `<=`, `>=`
- **Assignments**: Avoid assignments inside conditionals

## Operators

- **Ternary**: Allowed, but evaluate the true condition first; do not use shorthand ternary
- **Error suppression**: Avoid the `@` operator
- **Increment style**: Prefer pre-increment/pre-decrement in standalone statements

## Database

- **APIs first**: Avoid direct database access when an API or abstraction exists
- **SQL style**: Use uppercase SQL keywords; break long queries into multiple lines if needed
- **Escaping**: Escape values as close to the query as possible and use `$wpdb->prepare()`
- **Placeholders**: Do not quote placeholders (`%d`, `%f`, `%s`, `%i`)

## Discouraged & Forbidden

- **Clarity over cleverness**: Prefer readable solutions
- **Fall-throughs**: Explicitly comment intentional `switch` fall-throughs
- **Forbidden constructs**: Do not use `goto`, `eval()`, or `create_function()`
- **Regular expressions**: Use PCRE (`preg_*`), never use the `/e` modifier, and prefer single-quoted strings
- **Dangerous helpers**: Do not use `extract()` or backtick/shell execution shortcuts

## AI Requirements

When generating PHP code, you must:

- Use full PHP tags with proper quoting and escaping rules
- Follow lowercase-with-underscores naming for functions/variables and uppercase constants
- Indent with tabs (spaces only for alignment) and include required spacing around operators
- Apply braces to all control structures and avoid assignments in conditionals
- Use Yoda conditions for equality comparisons and avoid shorthand ternary
- Prefer WordPress APIs over direct SQL; when querying, use `$wpdb->prepare()` with unquoted placeholders
- Avoid forbidden constructs (`goto`, `eval()`, `create_function()`, `extract()`, backticks)
