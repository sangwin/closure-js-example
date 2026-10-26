
# JavaScript Closures

## Overview

A **closure** in JavaScript is a function that retains access to variables from its outer scope, even after the outer function has finished executing.

This example demonstrates how closures can be used to maintain private variables and preserve state between function calls.

## Implementation

```javascript
const add = (function () {
    let counter = 0;

    return function () {
        counter += 1;
        return counter;
    };
})();

console.log(add()); // 1
console.log(add()); // 2
console.log(add()); // 3
```

## How It Works

- **IIFE:** The outer function executes immediately and initializes `counter` to `0`.
- **Closure:** The returned inner function retains access to the outer function's `counter` variable.
- **Private Variable:** The `counter` variable cannot be accessed directly from outside the closure.
- **State Preservation:** Each call to `add()` increments the same counter and returns its updated value.

## Output

```text
1
2
3
```

## Key Benefits

- Maintains state between function calls.
- Supports private variables and data encapsulation.
- Helps avoid unnecessary global variables.
- Useful for counters, callbacks, and function factories.

## Reference

[JavaScript Closures - W3Schools](https://www.w3schools.com/js/js_function_closures.asp)

## Author

**Sangwin Gawande**

Website: [https://sangw.in](https://sangw.in)

---

Cheers!!
