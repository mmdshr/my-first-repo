---
layout: default
title: assert.notEqual()
excerpt: A non-strict comparison, checking for inequality.
categories:
  - assert
redirect_from:
  - "/notEqual/"
version_added: "1.0"
---

`notEqual( actual, expected [, message ] )`

A non-strict comparison, checking for inequality.

| name               | description                          |
|--------------------|--------------------------------------|
| `actual`           | Expression being tested              |
| `expected`         | Known comparison value               |
| `message` (string) | A short description of the assertion |

### Description

The `notEqual` assertion uses the simple inverted comparison operator (`!=`) to compare the actual and expected arguments. When they aren't equal, the assertion passes; otherwise, it fails. When it fails, both actual and expected values are displayed in the test result, in addition to a given message.

[`equal()`](./equal.md) can be used to test equality.

[`notStrictEqual()`](./notStrictEqual.md) can be used to test strict inequality.

### Examples

The simplest assertion example:

```js
QUnit.test( "a test", function( assert ) {
  assert.notEqual( 1, "2", "String '2' and number 1 don't have the same value" );
});
```
