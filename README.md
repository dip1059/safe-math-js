# safe-math-js

Safer floating-point math operations in JavaScript that return results we expect, so that 0.1 + 0.2 adds up to **0.3**, e.g., instead of *0.30000000000000004*. Customized and fixed from package '@dfkaye/safe-math'. 

## Fixings from package @dfkaye/safe-math
- 0.0003 * 100000000 = 20000 (error), (fixed result = 30000)
- 0.00000003 * 100000000 = 300000000 (error), (fixed result = 3)

## Some Existing Issue of @dip1059/safe-math-js
- 0.00000003 * 1000000000000000000 = 30000000000.000004 (error), should return 30000000000. For this kind of big integer(1000000000000000000) and large decimal value(0.00000003 equivalent to 3e-8) operations, wrap the output with Math.round() or parseInt(). e.g: 

```
let result = safe-math-js.multiply(0.00000003, 1000000000000000000);
console.log(Math.round(result)); //30000000000

// or

result = safe-math-js.multiply(3e-8, 1000000000000000000);
console.log(parseInt(result)); //30000000000
```
**Warning**: you need to check the actual output then you have to decide whether to keep the result as it is or to wrap with round() or parseInt()

## Basic Usage

```
const math = require('@dip1059/safe-math-js');

console.log(math.add(0.1, 0.2));
console.log(math.minus(0.1, 0.2));
console.log(math.divide(0.1, 0.2));
console.log(math.multiply(0.1, 0.2));

```
For more usage check the tests

## Documentation

See full details at https://dfkaye.com/posts/2020/08/17/safer-math-operations-in-javascript-using-tdd/.

## Install

`npm install @dip1059/safe-math-js`

**OR**

`yarn add @dip1059/safe-math-js`
