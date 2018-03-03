# freezly [![NPM][npm-img]][npm-url] [![Coverage][cov-img]][cov-url]

Small utility for deeply freezing objects in JavaScript.

## Table of Contents

*   [Installation](#installation)
*   [Documentation](#documentation)
*   [Code of Conduct](#code-of-conduct)
*   [Contributing](#contributing)
*   [License](#license)

## Installation

**npm**

```bash
npm install freezly
```

**yarn**

```bash
yarn add freezly
```

## Documentation

Below is an example of how to use **freezly**.

```js
import deepFreeze from 'freezly'

const frozenObject = deepFreeze({
  foo: ['bar'],
})

// The following will throw an error as you can't mutate frozen objects
frozenObject.baz = 'spam' // Can't add properties to frozen object
frozenObject.foo.push('baz') // Can't push items to frozen array
```

> Note: Once you freeze an object any attempts to mutate any part of the object will result in an error being thrown.

## Code of Conduct

Please see the [code of conduct](CODE_OF_CONDUCT.md).

## Contributing

Please see the [contributing guide](CONTRIBUTING.md).

## License

[MIT](LICENSE.md)

[cov-img]: https://img.shields.io/codecov/c/github/dogma-io/freezly.svg "Code Coverage"
[cov-url]: https://codecov.io/gh/dogma-io/freezly

[npm-img]: https://img.shields.io/npm/v/freezly.svg "NPM Version"
[npm-url]: https://www.npmjs.com/package/freezly
