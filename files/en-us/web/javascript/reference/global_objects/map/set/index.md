---
title: Map.prototype.set()
short-title: set()
slug: Web/JavaScript/Reference/Global_Objects/Map/set
page-type: javascript-instance-method
browser-compat: javascript.builtins.Map.set
sidebar: jsref
---

The **`set()`** method of {{jsxref("Map")}} instances adds or updates an entry in this map with a specified key and a value.

{{InteractiveExample("JavaScript Demo: Map.prototype.set()")}}

```js interactive-example
const map1 = new Map();
map1.set("bar", "foo");

console.log(map1.get("bar"));
// Expected output: "foo"

console.log(map1.get("baz"));
// Expected output: undefined
```

## Syntax

```js-nolint
set(key, value)
```

### Parameters

- `key`
  - : The key of the element to add to the `Map` object. The key may be any [JavaScript type](/en-US/docs/Web/JavaScript/Guide/Data_structures) (any [primitive value](/en-US/docs/Web/JavaScript/Guide/Data_structures#primitive_values) or any type of [JavaScript object](/en-US/docs/Web/JavaScript/Guide/Data_structures#objects)).
- `value`
  - : The value of the element to add to the `Map` object. The value may be any [JavaScript type](/en-US/docs/Web/JavaScript/Guide/Data_structures) (any [primitive value](/en-US/docs/Web/JavaScript/Guide/Data_structures#primitive_values) or any type of [JavaScript object](/en-US/docs/Web/JavaScript/Guide/Data_structures#objects)).

### Return value

The `Map` object.

## Examples

### Using set()

```js
const myMap = new Map();

// Add new elements to the map
myMap.set("bar", "foo");
myMap.set(1, "foobar");

// Update an element in the map
myMap.set("bar", "baz");
```

### Using the set() with chaining

Since the `set()` method returns back the same `Map` object, you can chain the
method call like below:

```js
// Add new elements to the map with chaining.
myMap.set("bar", "foo").set(1, "foobar").set(2, "baz");
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{jsxref("Map")}}
- {{jsxref("Map.prototype.get()")}}
- {{jsxref("Map.prototype.has()")}}
