# @hoangcung1804npm/ex-voluptas-minus

![npm version](https://img.shields.io/npm/v/@hoangcung1804npm/ex-voluptas-minus.svg?style=flat)
![Code Size](https://img.shields.io/github/languages/code-size/emranffl/@hoangcung1804npm/ex-voluptas-minus)
![GitHub license](https://img.shields.io/github/license/emranffl/@hoangcung1804npm/ex-voluptas-minus.svg?style=flat)
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)
![Jest Tests](https://img.shields.io/badge/Jest%20Tests-Passed-brightgreen.svg)
![GitHub Actions/CI](https://github.com/hoangcung1804npm/ex-voluptas-minus/workflows/Node.js%20CI/badge.svg)
[![npm downloads](https://img.shields.io/npm/dm/@hoangcung1804npm/ex-voluptas-minus.svg?style=flat)](https://www.npmjs.com/package/@hoangcung1804npm/ex-voluptas-minus)

<!-- ![GitHub search hit counter](https://img.shields.io/github/search/emranffl/@hoangcung1804npm/ex-voluptas-minus/object) -->

## Table of Contents

- [Getting Started](#getting-started)
- [Installation](#installation)
- [Features](#features)
- [Usage](#usage)
- [Examples](#examples)
- [License](#license)

## Getting Started

[deepObjectKeyAlternator](./docs/modules.md) is a versatile utility function that allows you to recursively parse an object or array of objects, applying a key mapping to rename object keys. It's particularly handy when you need to transform the structure of nested objects while preserving the original data.

## Installation

You can install `@hoangcung1804npm/ex-voluptas-minus` using `npm`:

```bash
npm install @hoangcung1804npm/ex-voluptas-minus
```

or `yarn`:

```bash
yarn add @hoangcung1804npm/ex-voluptas-minus
```

or `pnpm`:

```bash
pnpm add @hoangcung1804npm/ex-voluptas-minus
```

## Features

- Recursively parses nested objects.
- Customizable key mapping with intellisense support.
- Supports arrays (without intellisense support).
- Preserves the structure of arrays.

## Usage

Here's how you can use `deepObjectKeyAlternator` in your projects:

### ECMAScript Modules (ESM) Import

```ts
import { deepObjectKeyAlternator } from "@hoangcung1804npm/ex-voluptas-minus"
```

### CommonJS (CJS) Import

```ts
const { deepObjectKeyAlternator } = require("@hoangcung1804npm/ex-voluptas-minus")
```

## Examples

### For Objects (with intellisense support)

```ts
import { deepObjectKeyAlternator } from "@hoangcung1804npm/ex-voluptas-minus"
// or const { deepObjectKeyAlternator } = require("@hoangcung1804npm/ex-voluptas-minus")

// Define your input object
const inputObject = {
  id: 95,
  name: "Your Input Data",
  // ... Your input data ...
}

// Use deepObjectKeyAlternator to parse the object
const parsedObject = deepObjectKeyAlternator(inputObject, {
  id: "customId",
  name: "customName",
  // ... Your key mapping ...
})

console.log(parsedObject)
// {
//   customId: 95,
//   customName: 'Your Input Data',
//   // ... Your input data ...
// }
```

### For Arrays (without intellisense support)

```ts
import { deepObjectKeyAlternator } from "@hoangcung1804npm/ex-voluptas-minus"
// or const { deepObjectKeyAlternator } = require("@hoangcung1804npm/ex-voluptas-minus");

// Define an array of objects
const inputArray = [
  {
    id: 1,
    name: "Item 1",
  },
  {
    id: 2,
    name: "Item 2",
  },
  // ... More items ...
]

// Use deepObjectKeyAlternator to parse the array of objects
const parsedArray = inputArray.map((item) => {
  return deepObjectKeyAlternator(item, {
    id: "customId",
    name: "customName",
    // ... Your key mapping ...
  })
})

console.log(parsedArray)
// [
//   {
//     customId: 1,
//     customName: 'Item 1',
//     // ... Your input data ...
//   },
//   {
//     customId: 2,
//     customName: 'Item 2',
//     // ... Your input data ...
//   },
//   // ... More items ...
// ]
```

## License

This package is licensed under the [MIT License](https://tlo.mit.edu/learn-about-intellectual-property/software-and-open-source-licensing/open-source-licensing) - see the [LICENSE](LICENSE) file for details.
