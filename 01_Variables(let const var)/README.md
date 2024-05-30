# JavaScript Basics to Advanced

Welcome to the JavaScript Basics to Advanced repository. This repository aims to gather extensive knowledge of JavaScript, starting from the basics and progressing to advanced topics.

## Table of Contents
- [Introduction](#introduction)
- [Variables in JavaScript](#variables-in-javascript)
  - [Variable Declaration](#variable-declaration)
  - [Variable Scope](#variable-scope)
  - [Variable Hoisting](#variable-hoisting)
  - [Constant Variables](#constant-variables)
  - [Implicit Global Variables](#implicit-global-variables)
  - [Examples](#examples)
- [How to Run](#how-to-run)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This repository contains a series of JavaScript examples and explanations to help you understand and master JavaScript. Currently, we are focusing on variables.

## Variables in JavaScript

### Variable Declaration

In JavaScript, variables can be declared using `var`, `let`, or `const`. Each keyword has different properties and behaviors.

- **var**: Declares a variable, optionally initializing it to a value.
- **let**: Declares a block-scoped, local variable, optionally initializing it to a value.
- **const**: Declares a block-scoped, read-only named constant.

### Variable Scope

- **Global Scope**: A variable declared outside any function or block has a global scope.
- **Function Scope**: A variable declared within a function has a local scope, accessible only within that function.
- **Block Scope**: Variables declared with `let` or `const` within a block (a pair of curly braces `{}`) are block-scoped.

### Variable Hoisting

- **var**: Variables declared with `var` are hoisted to the top of their scope and can be used before declaration (though they will be `undefined` until assigned).
- **let** and **const**: Variables declared with `let` and `const` are also hoisted but not initialized. Accessing them before the declaration will result in a `ReferenceError`.

### Constant Variables

Variables declared with `const` are read-only. They cannot be reassigned after their initial assignment. However, if the variable is an object or array, the contents can be modified.

### Implicit Global Variables

When you declare a variable without using `var`, `let`, or `const`, it is implicitly created as a global variable. This can lead to unintended consequences and is generally considered bad practice. Here’s why:

1. **Global Scope**: The variable is added to the global object (e.g., `window` in browsers), which means it can be accessed and modified from anywhere in the code, potentially leading to conflicts and bugs.
2. **No Block Scope**: Unlike `let` and `const`, which are block-scoped, and `var`, which is function-scoped, an implicitly declared variable is globally scoped, which can lead to unpredictable behavior in larger codebases.
3. **Lack of Strict Mode Compliance**: In strict mode (`'use strict';`), this will throw an error, enforcing better coding practices and reducing the likelihood of bugs.

### Examples

Here's an example of variable declaration and reassignment:

```javascript
const accountId = 144553;
let email = "sk.a.hakeem123@gmail.com";
var accountPassword = "12345";
let accountCity = "Jaipur";

// accountId = 2; // not allowed because it's a constant

email = "abc@gmail.com";
accountPassword = "2323432";
accountCity = "Manipur";

console.table([accountId, email, accountPassword, accountCity]);
```


### This script will output a table with the following values:
┌─────────┬─────────────────┐
│ (index) │ Values          │
├─────────┼─────────────────┤
│ 0       │ 144553          │
│ 1       │ 'abc@gmail.com' │
│ 2       │ '2323432'       │
│ 3       │ 'Manipur'       │
└─────────┴─────────────────┘


## How to Run
To run the variables.js file, you need to have Node.js installed. Use the following command:
`node variables.js`


## Contributing
Contributions are welcome! Please create a pull request or open an issue to discuss any changes or improvements.

## License
This project is licensed under the MIT License.

`Feel free to customize or expand upon this template to better suit your project’s needs.`
