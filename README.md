# safe-math-js

Safer floating-point math operations in JavaScript that return results we expect, so that 0.1 + 0.2 adds up to **0.3**, e.g., instead of *0.30000000000000004*. Customized and fixed from package '@dfkaye/safe-math'. 

## Fixings from package @dfkaye/safe-math
- 0.0003 * 100000000

## Documentation

See full details on my blog post at https://dfkaye.com/posts/2020/08/17/safer-math-operations-in-javascript-using-tdd/.

## Install

`npm install @dip1059/safe-math-js`

**OR**

`yarn add @dip1059/safe-math-js`

## Test

Install dependencies (mocha and chai): `npm install @dfkaye/safe-math --save-dev`

Run: `npm test`

**OR**

Visit the live demo running the browser test suite on my blog at https://dfkaye.com/demos/safe-math-test-suite/.
