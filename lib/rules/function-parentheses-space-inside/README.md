# function-parentheses-space-inside

Require a single space or disallow whitespace on the inside of the parentheses of functions.

```css
a { transform: translate( 1, 1 ); }
/**                     ↑      ↑
 * The space inside these two parentheses */
```

The `--fix` option on the [command line](../../../docs/user-guide/usage/cli.md#autofixing-errors) can automatically fix all of the problems reported by this rule.

## Options

`string`: `"always"|"never"|"always-single-line"|"never-single-line"`

### `"always"`

There *must always* be a single space inside of the parentheses.

The following patterns are considered violations:

```css
a { transform: translate(1, 1); }
```

```css
a { transform: translate(1, 1 ); }
```

The following patterns are *not* considered violations:

```css
a { transform: translate( 1, 1 ); }
```

### `"never"`

There *must never* be whitespace on the inside of the parentheses.

The following patterns are considered violations:

```css
a { transform: translate( 1, 1 ); }
```

```css
a { transform: translate(1, 1 ); }
```

The following patterns are *not* considered violations:

```css
a { transform: translate(1, 1); }
```

### `"always-single-line"`

There *must always* be a single space inside the parentheses of single-line functions.

The following patterns are considered violations:

```css
a { transform: translate(1, 1) }
```

```css
a { transform: translate(1, 1 ) }
```

The following patterns are *not* considered violations:

```css
a { transform: translate( 1, 1 ) }
```

```css
a { transform: translate(1,
  1) }
```

```css
a {
  transform: translate(
    1,
    1
  )
}
```

### `"never-single-line"`

There *must never* be whitespace inside the parentheses of single-line functions.

The following patterns are considered violations:

```css
a { transform: translate( 1, 1 ) }
```

```css
a { transform: translate(1, 1 ) }
```

The following patterns are *not* considered violations:

```css
a { transform: translate(1, 1) }
```

```css
a { transform: translate( 1,
  1) }
```

```css
a {
  transform: translate(
    1,
    1
  )
}
```
