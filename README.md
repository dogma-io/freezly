# freezly

Small utility for deeply freezing objects in JavaScript.

## Installation

**npm**

```bash
npm install freezly
```

**yarn**

```bash
yarn add freezly
```

## Usage

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
