---
name: php-documentation-standards
description: WordPress PHPDoc standards for functions, classes, hooks, inline comments.
---

# PHP Documentation Standards

## DocBlock Scope
Use PHPDoc for: functions/methods, classes/interfaces/traits, properties/constants, hooks, notable globals, file includes/headers.

## Voice & Content
- Summary: single-sentence, third-person singular (e.g., "Retrieves the user's email address.")
- No HTML/Markdown in summaries
- Optional long description with Markdown/examples for complex behavior

## Placement & Formatting
- Directly above element; no code between
- Wrap at ~80 chars; consistent spacing; use spaces inside DocBlocks

## Baseline Structure
```php
/**
 * Summary sentence.
 *
 * Optional longer description.
 *
 * @since x.x.x
 *
 * @param type $var Description.
 * @return type Description.
 */
```

## Common Tags

### @since
- Required: `@since x.x.x` (use `@since Unknown` if unknown)
- Add new `@since` for behavioral changes

### @param
- Format: `@param type $variable Description.`
- Include `$` prefix; end with period
- Multiple types: `string|int`

### @return
- Format: `@return type Description.`
- Omit for void functions
- Be specific about what's returned

### @deprecated
- Format: `@deprecated version Use alternative().`
- Keep `@param`/`@return` tags

## Hooks
Document immediately before `do_action()` or `apply_filters()`:
```php
/**
 * Fires after user login.
 *
 * @since 1.0.0
 *
 * @param int    $user_id User ID.
 * @param object $user    User object.
 */
do_action( 'after_user_login', $user_id, $user );
```

## Inline Comments
- `//` for brief; `/* */` for longer
- Explain why, not what
- Close to relevant code

## Class Documentation
```php
/**
 * User authentication handler.
 *
 * @since 1.0.0
 */
class User_Auth {
    /**
     * Maximum login attempts.
     *
     * @since 1.0.0
     * @var int
     */
    const MAX_ATTEMPTS = 5;
}
```

## Formatting
- Lists: `-` unordered, `1.` ordered; blank lines before/after
- Code examples: indent 4 spaces
- Links: `@link URL`
- Element-specific: functions (summary, description, tags), arrays (document keys with `@type`), classes (summary, description, `@since`), properties (`@var type $property desc`)
- Tag policies: use plugin/theme name for `@package` (not WordPress); avoid `@author` unless required; `@license`/`@copyright` only for bundled third-party code