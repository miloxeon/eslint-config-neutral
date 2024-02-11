# ⚪️ ESLint-config-neutral

ESLint [Shareable Config](http://eslint.org/docs/developer-guide/shareable-configs) that catches strictly the errors and nothing more. 

With that config, you can code however you want. This config is a good choice for those who don't use ESLint at all because they feel like linters restrict them. By default, it doesn't dictate any opinionated things. Strictly the errors.

Also, this config is a good starter, akin to [normalize.css](https://github.com/necolas/normalize.css), but for ESLint. Feel free to extend it to your liking.

## Usage

```bash
npm install --save-dev eslint-config-neutral
```

Then, add this to your `.eslintrc` file:

```JSON
{
   "extends": "neutral"
}
```

You can override rules or add yours directly in `.eslintrc` file.

## Overview

|Rule                     |Description                                                                         |Comment                                                                                                                       |
|-------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
|for-direction            |enforce for loop update clause moving the counter in the right direction            |One wrong symbol will produce an unintended infinite loop that doesn’t seem wrong at first glance.                                            |
|no-async-promise-executor|disallow using an async function as a Promise executor                              |Promise won’t be rejected if a runtime error happens.                                                                           |
|no-await-in-loop         |disallow await inside of loops                                                      |`await` in loops doesn’t lead to asynchronou sequential execution.                                                                        |
|no-compare-neg-zero      |disallow comparing against -0                                                       |Comparing against -0 is very odd and unlikely. Programmers who didn’t research this topic specifically hardly know the answer.|
|no-cond-assign           |disallow assignment operators in conditional expressions                            |A classic mistake.                                                                                                            |
|no-dupe-args             |disallow duplicate arguments in function definitions                                |                                                                                                                              |
|no-dupe-else-if          |disallow duplicate conditions in if-else-if chains                                  |Leads to the code that looks like it will execute while it won’t.                                                             |
|no-dupe-keys             |disallow duplicate keys in object literals                                          |                                                                                                                              |
|no-duplicate-case        |disallow duplicate case labels                                                      |                                                                                                                              |
|no-invalid-regexp        |disallow invalid regular expression strings in RegExp constructors                  |                                                                                                                              |
|no-loss-of-precision     |disallow literal numbers that lose precision                                        |Precision errors are notoriously hard to debug.                                                                               |
|no-obj-calls             |disallow calling global object properties as functions                              |Things like `Math()` are always errors.                                                                                         |
|no-unsafe-negation       |disallow negating the left operand of relational operators                          |`if (!key in foo)` meaning “check if the key exist in an object” won’t produce the correct result.                             |
|require-atomic-updates   |disallow assignments that can lead to race conditions due to usage of await or yield|                                                                                                                              |
|use-isnan                |require calls to isNaN() when checking for NaN                                      |Comparing against `NaN` is pointless. `isNaN()` function should be used instead.                                                       |
|valid-typeof             |enforce comparing typeof expressions against valid strings                          |                                                                                                                              |
|no-const-assign          |disallow reassigning const variables                                                |                                                                                                                              |
|no-dupe-class-members    |disallow duplicate class members                                                    |                                                                                                                              |
|no-duplicate-imports     |disallow duplicate module imports                                                   |                                                                                                                              |
|no-new-symbol            |disallow new operators with the Symbol object                                       |`new Symbol()` is a counterintuitive error.                                                                                     |
|no-this-before-super     |disallow this / super before calling super() in constructors                        |                                                                                                                              |
