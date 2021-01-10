---
layout: default
title: assert.true()
excerpt: A strict boolean true comparison.
categories:
  - assert
version_added: "2.11"
---

`true( actual [, message ] )`

A strict comparison that passes if the first argument is boolean `true`.

| name               | description                          |
|--------------------|--------------------------------------|
| `actual`           | Expression being tested              |
| `message` (string) | A short description of the assertion |

### Description

`true()` requires just one argument. If the argument evaluates to true, the assertion passes; otherwise, it fails.

[`false()`](./false.md) can be used to explicitly test for a false value.

### Examples

```js
QUnit.test( "true test", function( assert ) {
  assert.true( true, "true succeeds" );

  assert.true( "non-empty", "non-empty string fails" );
  assert.true( "", "empty string fails" );
  assert.true( 1, "1 fails" );
  assert.true( false, "false fails" );
  assert.true( NaN, "NaN fails" );
  assert.true( null, "null fails" );
  assert.true( undefined, "undefined fails" );
});
```

