---
title: Date.prototype.valueOf()
short-title: valueOf()
slug: Web/JavaScript/Reference/Global_Objects/Date/valueOf
page-type: javascript-instance-method
browser-compat: javascript.builtins.Date.valueOf
sidebar: jsref
---

The **`valueOf()`** method of {{jsxref("Date")}} instances returns the number of milliseconds for this date since the [epoch](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date#the_epoch_timestamps_and_invalid_date), which is defined as the midnight at the beginning of January 1, 1970, UTC.

{{InteractiveExample("JavaScript Demo: Date.prototype.valueOf()")}}

```js interactive-example
const date1 = new Date(Date.UTC(96, 1, 2, 3, 4, 5));

console.log(date1.valueOf());
// Expected output: 823230245000

const date2 = new Date("02 Feb 1996 03:04:05 GMT");

console.log(date2.valueOf());
// Expected output: 823230245000
```

## Syntax

```js-nolint
valueOf()
```

### Parameters

None.

### Return value

A number representing the [timestamp](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date#the_epoch_timestamps_and_invalid_date), in milliseconds, of this date. Returns `NaN` if the date is [invalid](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date#the_epoch_timestamps_and_invalid_date).

## Description

The `valueOf()` method is part of the [type coercion protocol](/en-US/docs/Web/JavaScript/Guide/Data_structures#type_coercion). Because `Date` has a [`[Symbol.toPrimitive]()`](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/Symbol.toPrimitive) method, that method always takes priority over `valueOf()` when a `Date` object is implicitly [coerced to a number](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number#number_coercion). However, `Date.prototype[Symbol.toPrimitive]()` still calls `this.valueOf()` internally.

The {{jsxref("Date")}} object overrides the {{jsxref("Object/valueOf", "valueOf()")}} method of {{jsxref("Object")}}. `Date.prototype.valueOf()` returns the timestamp of the date, which is functionally equivalent to the {{jsxref("Date.prototype.getTime()")}} method.

## Examples

### Using valueOf()

```js
const d = new Date(0); // 1970-01-01T00:00:00.000Z
console.log(d.valueOf()); // 0
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{jsxref("Object.prototype.valueOf()")}}
- {{jsxref("Date.prototype.getTime()")}}
