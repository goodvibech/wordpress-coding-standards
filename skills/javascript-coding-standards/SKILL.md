---
name: javascript-coding-standards
description: WordPress JS standards for style, formatting, JSDoc, type checking, control flow.
---

# JavaScript Coding Standards

## Style & Formatting
- Spaces after keywords and around operators
- Space after commas: `[1, 2, 3]`, `function(a, b)`
- Opening brace same line, closing on own line
- Lines under 100 chars when possible
- Always terminate with semicolons

## Variables & Naming
- `const` for constants, `let` for variables, avoid `var`
- `camelCase` for variables/functions
- `PascalCase` for classes/constructors
- `UPPER_SNAKE_CASE` for constants
- Declare at scope top; descriptive names; minimize globals

## Equality & Type Checking
- Use `===` and `!==` only
- Type checks: `typeof value === 'type'`, `Array.isArray(value)`, `value === null`

## Strings & Data
- Default to single quotes; escape internal quotes
- Template literals for clarity only
- Use `[]` and `{}` literals
- Prefer dot notation: `object.property`
- Use array methods: `map()`, `filter()`, `reduce()`, `forEach()`
- Avoid unnecessary mutation

## Functions & Control Flow
- Small, descriptive functions
- `switch`: indent `case` inside; always `break`; comment fall-throughs

## Comments & JSDoc
- Inline: `//` single-line, `/* */` multi-line
- JSDoc for: public APIs, classes, methods, namespaces, closures, file headers, events
- Format: single-sentence summary (third-person), no HTML in summary
- Tags: `@since`, `@param {type} name desc`, `@return {type} desc`
- Align tags; wrap at ~80 chars

## Example JSDoc
```javascript
/**
 * Calculates sum of two numbers.
 *
 * @since 1.0.0
 *
 * @param {number} a - First number.
 * @param {number} b - Second number.
 * @return {number} Sum of a and b.
 */
function add(a, b) {
    return a + b;
}
```

## Linting
- Follow project ESLint/JSHint config
- Use standard libraries consistently
- Keep dependencies minimal and updated