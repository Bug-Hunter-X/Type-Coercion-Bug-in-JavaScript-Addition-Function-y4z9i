# JavaScript Type Coercion Bug

This repository demonstrates a subtle bug in a JavaScript function that involves type coercion and handling of null and undefined values. The function `foo` adds two numbers, but its behavior is unexpected when dealing with `undefined` inputs.

## Bug Description

The `foo` function is designed to return `null` if either input is `null`. However, it doesn't explicitly handle `undefined` inputs. This leads to unexpected behavior because JavaScript's loose typing will coerce `undefined` to 0, producing incorrect results. 

## How to Reproduce

1. Clone this repository.
2. Open `bug.js`.
3. Run the code using a JavaScript runtime (like Node.js). Note that the output for `undefined` input values is not the intended null but instead 0 + inputNumber. 

## Solution

The solution involves explicitly checking for both `null` and `undefined` inputs to ensure the function behaves as expected in all cases.

## License

MIT